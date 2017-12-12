# 深入浅出 Swarm

Posted on [January 25, 2015](http://blog.daocloud.io/swarm_analysis_part1/) by [孙宏亮](http://blog.daocloud.io/author/allen-sundaocloud-io/)

# **1.Swarm 简介**

Docker 自诞生以来，其容器特性以及镜像特性给 DevOps 爱好者带来了诸多方便。然而在很长的一段时间内，Docker 只能在单 host 上运行，其跨 host 的部署、运行与管理能力颇受外界诟病。跨 host 能力的薄弱，直接导致 Docker 容器与 host 的紧耦合，这种情况下，Docke r容器的灵活性很难令人满意，容器的迁移、分组等都成为很难实现的功能点。

Swarm 是 Docker 公司在2014年12月初新发布的容器管理工具。和 Swarm 一起发布的 Docker 管理工具还有 Machine 以及 Compose。

Swarm 是一套较为简单的工具，用以管理 Docker 集群，使得 Docker 集群暴露给用户时相当于一个虚拟的整体。Swarm 使用标准的 Docker API 接口作为其前端访问入口，换言之，各种形式的 Docker Client(dockerclient in go, docker_py, docker 等)均可以直接与 Swarm 通信。Swarm 几乎全部用 Go 语言来完成开发，并且还处于一个 Alpha 版本，目前在 github 上发布的版本仅有 v0.1.0-rc1。然而 Swarm 的发展十分快速，功能和特性的变更迭代还非常频繁。因此，可以说 Swarm 还不推荐被用于生产环境中，但可以肯定的 是Swarm 是一项很有前途的技术。
Swarm 的设计和其他 Docker 项目一样，遵循 “batteries included but removable” 原则。笔者对该原则的理解是：batteries included 代表设计 Swarm 时，为了完全体现分布式容器集群部署、运行与管理功能的完整性，Swarm 和 Docker 协同工作，Swarm 内部包含了一个较为简易的调度模块，以达到对 Docker 集群调度管理的效果；“but removable” 意味着 Swarm 与 Docker 并非紧耦合，同时 Swarm 中的调度模块同样可以定制化，用户可以按照自己的需求，将其替换为更为强大的调度模块，如 Mesos 等。另外，这套管理引擎并未侵入 Docker 的使用，这套机制也为其他容器技术的集群部署、运行与管理方式提供了思路。

本文将从以下两点分析 Swarm：

- Swarm 架构
- Swarm 命令

# **2.Swarm 架构**

Swarm 作为一个管理 Docker 集群的工具，首先需要将其部署起来，可以单独将 Swarm 部署于一个节点。另外，自然需要一个 Docker 集群，集群上每一个节点均安装有 Docker。具体的 Swarm 架构图可以参照下图：

![](swarmarchitecture.jpg)

<center>图2.1 Swarm 架构图</center>

# **3.Swarm 命令**

Swarm 架构图可以让大家对 Swarm 有一个初步的认识，比如 Swarm 的具体工作流程：Docker Client 发送请求给 Swarm；Swarm 处理请求并发送至相应的 Docker Node；Docker Node 执行相应的操作并返回响应。除此之外，Swarm 的工作原理依然还不够明了。

深入理解 Swarm 的工作原理，可以先从 Swarm 提供的命令入手。Swarm 支持的命令主要有4个：swarm create、swarm manage、swarm join、swarm list。当然还有一个 swarm help 命令，该命令用于指导大家如何正确使用 swarm 命令，本文不再赘述。

## **3.1 swarm create**

Swarm中 swarm create 命令用于创建一个集群标志，用于 Swarm 管理 Docker 集群时，Docker Node 的节点发现功能。

发起该命令之后，Swarm 会前往 Docker Hub 上内建的发现服务中获取一个全球唯一的 token，用以唯一的标识 Swarm 管理的 Docker 集群。

注：Swarm 的运行需要使用服务发现，目前该服务内建于 Docker Hub，该服务发现机制目前还在 alpha 版本，站点为：http://discovery-stage.hub/docker.com 。

## **3.2 swarm manage**

Swarm 中 swarm manage 是最为重要的管理命令。一旦 swarm manage 命令在 Swarm 节点上被触发，则说明用户需要 swarm 开始管理 Docker 集群。从运行流程的角度来讲，swarm 经历的阶段主要有两点：启动 swarm、接收并处理 Docker 集群管理请求。

Swarm 启动的过程包含三个步骤：

1. 发现 Docker 集群中的各个节点，收集节点状态、角色信息，并监视节点状态的变化；
2. 初始化内部调度（scheduler）模块；
3. 创建并启动 API 监听服务模块；

第一个步骤，Swarm 发现 Docker 集群中的节点。发现（discovery）是 Swarm 中用于维护 Docker 集群状态的机制。既然涉及到发现（discovery），那在这之前必须先有注册（register）。Swarm 中有专门负责发现（discovery）的模块，而关于注册（register）部分，不同的 discovery 模式下，注册（register）也会有不同的形式。

目前，Swarm 中提供了 5 种不同的发现（discovery）机制：Node Discovery、File Discovery、Consul Discovery、EtcD Discovery 和 Zookeeper Discovery。

第二个步骤，Swarm 内部的调度（scheduler）模块被初始化。swarm 通过发现机制发现所有注册的 Docker Node，并收集到所有 Docker Node 的状态以及具体信息。此后，一旦 Swarm 接收到具体的 Docker 管理请求，Swarm 需要对请求进行处理，并通过所有 Docker Node 的状态以及具体信息，来筛选（filter）决策到底哪些Docker Node 满足要求，并通过一定的策略（strategy）将请求转发至具体的一个 Docker Node。

第三个步骤，Swarm 创建并初始化 API 监听服务模块。从功能的角度来讲，可以将该模块抽象为 Swarm Server。需要说明的是：虽然 Swarm Server 完全兼容 Docker 的 API，但是有不少 Docker 的命令目前是不支持的，毕竟管理 Docker 集群与管理单独的 Docker 会有一些区别。当 Swarm Server 被初始化并完成监听之后，用户即可以通过 Docker Client 向 Swarm 发送 Docker 集群的管理请求。

Swarm 的 swarm manage 接收并处理 Docker 集群的管理请求，即是 Swarm 内部多个模块协同合作的结果。请求入口为 Swarm Server，处理引擎为 Scheduler，节点信息依靠 Disocovery。

## **3.3 swarm join**

Swarm 的 swarm join 命令用于将 Docker Nod e添加至 Swarm 管理的 Docker 集群中。从这点也可以看出 swarm join 命令的执行位于 Docker Node，因此在 Docker Node 上运行该命令，首先需要在 Docker Node 上安装 Swarm，由于该 Swarm 只会执行 swarm join 命令，故可以将其当成 Docker Node 上用于注册的 agent 模块。

功能而言，swarm join 可以认为是完成 Docker Node 在 Swarm 节点处的注册（register）工作，以便 Swarm 在执行 swarm manage 时可以发现该 Docker Node。然而，上文提及的 5 种 discovery 模式中，并非每种模式都支持 swarm join 命令。不支持的 discovery 的模式有 Node Discovery 与 File Discovery。

Docker Node 上 swarm join 执行之后，标志着 Docker Node 向 Swarm 注册，请求加入 Swarm 管理的 Docker 集群中。Swarm 通过注册信息，发现 Docker Node，并获取 Docker Node 的状态以及具体信息，以便处理 Docker 请求时作为调度依据。

## **3.4 swarm list**

Swarm 中的 swarm list 命令用以列举 Docker 集群中的 Docker Node。

Docker Node 的信息均来源于 Swarm 节点上注册的 Docker Node。而一个 Docker Node 在 Swarm 节点上注册，仅仅是注册了 Docker Node 的 IP 地址以及 Docker 监听的端口号。

使用swarm list命令时，需要指定discovery的类型，类型包括：token、etcd、file、zk以及<ip>。而 swarm list 并未罗列 Docker 集群的动态信息，比如 Docker Node 真实的运行状态，或者 Docker Node 在 Docker 集群中扮演的角色信息。

# **4.总结**

Swarm 的架构以及命令并没有很复杂，同时也为希望管理 Docker 集群的 Docker 爱好者降低了学习和使用门槛。

俗话说得好，没有一种一劳永逸的工具，有效的管理 Docker 集群同样也是如此。缺乏场景来谈论Swarm 的价值，意义并不会很大。相反，探索和挖掘 Swarm 的特点与功能，并为 Docker 集群的管理提供一种可选的方案，是 Docker 爱好者更应该参与的事。

本文初步介绍 Swarm，并涉及架构与命令，下期将带来 Swarm的具体使用，以及 Swarm 的架构剖析。

# **5.作者介绍**

孙宏亮，**DaoCloud **初创团队成员，软件工程师，浙江大学 VLIS 实验室应届研究生。读研期间活跃在 PaaS 和 Docker 开源社区，对 Cloud Foundry 有深入研究和丰富实践，擅长底层平台代码分析，对分布式平台的架构有一定经验，撰写了大量有深度的技术博客。2014 年末以合伙人身份加入 DaoCloud 团队，致力于传播以 Docker 为主的容器技术，推动互联网应用的容器化步伐。邮箱：allen.sun@daocloud.io

# **6.参考文献**

1.http://github.com/docker/swarm
2.http://technolo-g.com/intro-to-docker-swarm-pt1-overview/
3.http://technolo-g.com/intro-to-docker-swarm-pt2-config-options-requirements/