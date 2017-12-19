# GlusterFS

**Gluster**是一个大尺度文件系统。它是各种不同的存储[服务器](https://zh.wikipedia.org/wiki/%E6%9C%8D%E5%8A%A1%E5%99%A8)之上的组合，这些服务器由以太网或无限带宽技术[Infiniband](http://en.wikipedia.org/wiki/Infiniband)以及远程直接内存访问[RDMA](http://en.wikipedia.org/wiki/Remote_direct_memory_access)互相融汇，最终所形成的一个大的并行文件系统网络。它有包括[云计算](https://zh.wikipedia.org/wiki/%E4%BA%91%E8%AE%A1%E7%AE%97)在内的多重应用，诸如：[生物医药](https://zh.wikipedia.org/w/index.php?title=%E7%94%9F%E7%89%A9%E5%8C%BB%E8%8D%AF&action=edit&redlink=1)科学，文档存储。Gluster是由GNU托管的自由软件，证书是[AGPL](http://en.wikipedia.org/wiki/Affero_General_Public_License)。[Gluster公司](https://zh.wikipedia.org/w/index.php?title=Gluster%E5%85%AC%E5%8F%B8&action=edit&redlink=1)是Gluster的首要商业赞助商，且提供商业产品以及基于Gluster的解决方案。

## 设计

GlusterFS 是 Client/Server 架构。服务器典型的布置在存储砖上，每一台服务器运行一个名为 glusterfsd 的守护进程，将本地文件系统作为卷进行输出。GlusterFS 的客户端进程通过 TCP/IP, InfiniBand 或 SDP 一类客户协议连接到服务器，将远端卷组成一个大的所谓折叠式翻译器。最终的卷通过一种叫做 [FUSE](http://en.wikipedia.org/wiki/Filesystem_in_Userspace) 的用户空间文件机制机载到客户机。有大量文件应用的 I/O 同样可以用 libglusterfs 客户端库来直接连接服务器并内在的运行翻译器，而无需经过文件系统以及 FUSE。大多数 GlusterFS 功能被实现为翻译器，包括了：

- 基于文件的[镜像](http://en.wikipedia.org/wiki/Mirror_(computing))与[赋值](http://en.wikipedia.org/wiki/Replication_(computer_science))技术
- 基于文件的数据存储计算领域的[数据带](http://en.wikipedia.org/wiki/Data_striping)技术
- 基于文件的[负载平衡](http://en.wikipedia.org/wiki/Load_balancing_(computing))技术
- 卷的[双机备份](http://en.wikipedia.org/wiki/Failover)技术
- [磁盘高速缓存](http://en.wikipedia.org/wiki/Cache#Disk_cache)技术以及[排产](http://en.wikipedia.org/wiki/I/O_scheduling)技术
- [存储分配技术](http://en.wikipedia.org/wiki/Disk_quota)

GlusterFS 的设计遵循奥卡姆剃刀原则的简单性：尽管它导出一已存在，但是构建存储的决定权在于客户端翻译器。客户端自身都是没有状态的，互相之间没有交互。但是期望相互间的翻译器配置是一致的。这会引发[内存一致性模型](https://zh.wikipedia.org/wiki/%E5%86%85%E5%AD%98%E4%B8%80%E8%87%B4%E6%80%A7%E6%A8%A1%E5%9E%8B)问题，但这种设计允许Gluster用商用硬件在规模上能达到数个[P字节](https://zh.wikipedia.org/wiki/Petabyte)，避免了通常影响分布式文件系统的紧内聚松耦合瓶颈。