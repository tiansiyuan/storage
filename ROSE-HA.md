ROSE HA是美国ROSE Datasystem Inc.出品的新一代高可用性软件，它可以将UNIX服务器组成集群系统，并对服务器进行监控、故障检测、故障恢复，保护运行于服务器中的关键性数据服务和网络服务。对于在客户机/服务器环境中的网络及数据库中集成的高可用需求，ROSE HA 提供了非常灵活而且适用的解决方案。

## 定义

ROSE HA是一套提供防止业务主机因不可避免的意外性或计划性宕机问题的高可用性软件。

## 简介

ROSE HA软件同时安装在两台主机上，用于监视系统的状态，协调两台主机的工作，维护系统的可用性。它能侦测应用级系统软件、硬件发生的故障，及时地进行错误隔绝、恢复，以最低成本提供用户几乎不停顿的计算机作业环境。

ROSE HA以其稳定、可靠，在windows NT、windows2000服务器的容错软件中占有绝对的优势，同时也成为国内绝大多数的[磁盘阵列柜](https://baike.baidu.com/item/%E7%A3%81%E7%9B%98%E9%98%B5%E5%88%97%E6%9F%9C)厂家的OEM容错软件。

功能特点

工作模式

主从方式（Active/Standby) 主机工作，从机处于监控准备状态。当主机宕机时，从机接管主机的工作，待主机恢复正常后，按使用者的预定以自动或手动的方式将服务切换到主机上运行。

双工方式（Active/Active） 两台[主机](https://baike.baidu.com/item/%E4%B8%BB%E6%9C%BA)同时运行各自的服务工作，且相互监测对方的情况。当一台主机宕机时，另外一台主机立即接管它的工作，保证工作不间断。

特 点

⊙当一台活动服务器宕机时，其[IP地址](https://baike.baidu.com/item/IP%E5%9C%B0%E5%9D%80/150859)、[服务器名称](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8%E5%90%8D%E7%A7%B0)及运行的作业会自动转移至另一台服务器，客户端软件不需要重新设定，只要重新连结至原来的IP地址及服务器名称即可继续作业；

⊙两台服务器的信息交换可通过：RS232、[TCP/IP](https://baike.baidu.com/item/TCP%2FIP/214077)

⊙ROSE HA采取高可靠的错误检测和故障恢复机制减少系统宕机，停机时间并防范错误，提供故障警告；

⊙ROSE HA可设定故障排除后自动或手动回复（switch back）；

⊙ROSE HA安装时不需要修改操作系统的核心、更改应用软件，也无需特殊的硬件；

⊙ROSEHA 提供基于GUI的监控中心，管理员能查看ROSE HA的状态、检查错误信息和警告、修改系统参数及从远程工作站管理ROSE HA系统；

⊙与数据库无关，可以支持各种数据库，包括ORACLE、[Sybase](https://baike.baidu.com/item/Sybase/2138155)、[Informix](https://baike.baidu.com/item/Informix/269954)等

Private Net 私用网络

两台服务器通过私用网络心跳（HeartBeat）信号，使两台服务器能够相互了解对方的运行情况。为了避免不必要的失效切换，最好建立两条独立的物理路径作为通讯路径。

⊙RS-232 Socket Private Net:配置服务器空闲的串口作为一条通讯路径。

⊙TCP/IP Socket Private Net:两台服务器的网卡用反线（back to back)直接或通过LAN建立一条通讯路径。

如果所有的私用网均失效，服务器仍然可以用公用侦测对方服务器的可用性。如果对方服务器仍然可用，不触发接管动作；如果对方服务器不可用，立即接管动作。

Public Net [公用网络](https://baike.baidu.com/item/%E5%85%AC%E7%94%A8%E7%BD%91%E7%BB%9C/12752077)

客户端通过此网络与服务器通信，当两台服务器互为备份。对于不同的服务，可以用不同的公用网连接到两台服务器。ROSE HA支持[TCP/IP协议](https://baike.baidu.com/item/TCP%2FIP%E5%8D%8F%E8%AE%AE/212915)，可以在EthernetFastEthernet、FDDI和ATM网上运行。

管理工具

⊙友好、直观、易于操作的GUI界面

⊙有关ROSE HA的配置都可以在GUI中完成，支持动态配置和实时同步

⊙网卡的状态，磁盘的状态都可在GUI中显示出来

⊙用户可通过第三方Web浏览器进行远程管理

监控的对象资源

⊙Volume

⊙[IP地址](https://baike.baidu.com/item/IP%E5%9C%B0%E5%9D%80/150859)

⊙计算机别名

⊙共享文件

⊙NT服务

⊙用户自定义

rose 硬件热备方式简介

ROSE HA 是一个提供防止关键业务主机因不可避免的意外性或计划性宕机问题的[高可用性](https://baike.baidu.com/item/%E9%AB%98%E5%8F%AF%E7%94%A8%E6%80%A7/909038)软件。 ROSE HA 软件同时安装在两台主机上，用于监视系统的状态、协调两台主机的工作和维护系统的可用性。它能侦测应用级系统软件、硬件发生的故障，并及时的进行错误隔绝和恢复，以最低成本提供用户近乎不停顿的计算机作业环境。

用户为何需要我们的软件？

· 用户的服务器中运行着整个公司的重要信息。

· 系统宕机是不可避免的，它将给用户的业务带来极大的损失。

· 用户需要一个可靠的、易操作的、高可用的解决方案，将不可避免的宕机次数减少到最小。

· 当一台服务器发生问题时，必须在最短时间内自动切换到备份服务器。对用户来说，整个操作必须是 无需人工干预的。

也就是说， ROSE HA 软件可以实现：假设用户有两台服务器正在运行着某个关键性应用，当其中一台服务器发生故障时，另一台服务器则自动接管原先由故障服务器运行的服务。

| **特性与优势** |
| --------- |
|           |

| 特性                                       | 优势                                       |
| ---------------------------------------- | ---------------------------------------- |
| [高可用性](https://baike.baidu.com/item/%E9%AB%98%E5%8F%AF%E7%94%A8%E6%80%A7/909038)管理 | ROSE HA 采取高可靠度与高效率机制减少系统宕机，并能够提供故障警告。内置的代理程序可以监测服务器、网卡、磁盘以及 NT 服务的可用性，以减少宕机时间。 |
| 灵活配置                                     | 集群中两台服务器无需相同。用户可以将一台设置为工作主机（ Active Server ），一台设置为备援主机（ Hot Standby Backup Server ）；也可将两台都设置为工作主机，相互备援。 |
| 高可靠性                                     | ROSE HA 可防止错误，提供故障安全防护和零故障操作系统。          |
| 支持自动及手工切换                                | 当一台服务器出现故障时，事先指定的备份服务器将接管其上的服务。当故障服务器恢复时，可以设置采用手工或自动方式将服务切换回已恢复的服务器。 |
| 配置和管理简便                                  | 采用直观、友好的 Windows GUI 界面，使用户可以实现远程或本地管理。  |

**Windows **

Windows NT4.0 Server Sp6a
　　Windows Server 2000 各发行版本
　　Windows Server 2003 各发行版本
　　Windows Server 2008 各发行版本
　　Windows Server 2012 各发行版本

**Linux **

RedHat Enterprise Linux 2.1/3/4/5/6
　　SUSE Linux Enterprise Server 8/9/10/11
　　Asianux 1/2/3
　　Red Flag Linux 4.0/5.0

**SCO**

SCO OpenServer 5.0.x/UnixWare 7.x.x

**Sun**

Sun Sparc Solaris 2.5.1/2.6/7/8/9/10
　　Sun x86 Solaris 10

RoseHA 支持多种应用的数据复制和应用切换，并能与重要的应用如数据库： Microsoft SQL Sever 、 Exchange 2000/2003 、 Oracle 、文件服务器等紧密配合。

RoseHA 支持的应用包括：

数据库：Oracle、[MSSQL](https://baike.baidu.com/item/MSSQL/2259472)、[Sybase](https://baike.baidu.com/item/Sybase/2138155)、[DB2](https://baike.baidu.com/item/DB2/7034285)、MySQL、[Informix](https://baike.baidu.com/item/Informix/269954)等

[邮件服务器](https://baike.baidu.com/item/%E9%82%AE%E4%BB%B6%E6%9C%8D%E5%8A%A1%E5%99%A8/985736)：Sendmail、[Postfix](https://baike.baidu.com/item/Postfix/10077421)、[Domino](https://baike.baidu.com/item/Domino/17833)等
　　[Web服务器](https://baike.baidu.com/item/Web%E6%9C%8D%E5%8A%A1%E5%99%A8/8390210)：[IIS](https://baike.baidu.com/item/IIS/99720)、[Tomcat](https://baike.baidu.com/item/Tomcat/255751)、[Apache](https://baike.baidu.com/item/Apache/8512995)等
　　文件服务器：Samba、FTP、NFS等
　　中间件应用：WebLogic、WebSphere等

********

****SCSI/IPSAN/FCSAN/SAS等

随着服务器硬件的发展，服务器性能及内部存储容量等都有个人了大幅提升。服务器在应对主流业务方面提供了强大的能力，为了保证业务数据的连续性及提高客户[投资回报率](https://baike.baidu.com/item/%E6%8A%95%E8%B5%84%E5%9B%9E%E6%8A%A5%E7%8E%87/89993)，RoseMirrorHA 提供了基于服务器的纯软[高可用性](https://baike.baidu.com/item/%E9%AB%98%E5%8F%AF%E7%94%A8%E6%80%A7/909038)软件，实现了应用高可用及数据[镜像](https://baike.baidu.com/item/%E9%95%9C%E5%83%8F)的低成本、高效率解决方案。

RoseMirrorHA 是在实时数据镜像基础上，实现了不需要共享存储的纯软高可用性系统。在传统高可用性系统中需要通过共享存储来实现数据的共享提升性能，但这也增加了可用性系统的成本。RoseMirrorHA 通过现有的以太网络基础环境，通过 [TCP/IP](https://baike.baidu.com/item/TCP%2FIP/214077) 协议，在两台[主机](https://baike.baidu.com/item/%E4%B8%BB%E6%9C%BA)之间实现了数据的实时镜像，不需要额外的硬件投资。在充分利用已有资源的基础上，通过先进的软件技术，实现纯软的[高可用性](https://baike.baidu.com/item/%E9%AB%98%E5%8F%AF%E7%94%A8%E6%80%A7/909038)系统。

RoseMirrorHA 高可用性系统，可以对主机的 IP 、应用程序、数据等而下之进行监控和保护，当应用程序或主机发生故障后， RoseMirrorHA 将自动、快速的切换应用到备机，确保应用服务持续和可用性，保证公司业务的持续运行。

RoseMirrorHA 支持 Active/Standby 和 Active/Active 两种模式。在 Active/Standby 的方式中，其中一台主机作为 Active 主机，运行重要的应用程序，向客户端提供各种应用服务，另一台主机作为备机，实时监控 Active 主机运行情况，只有当 Active 主机发生故障后，备机才接管 Active 主机上的应用服务。在 Active/Active 配置方式中，每台主机上运行各自的应用程序。服务器在运行自身的应用服务时，同时也是另一台主机的备机，即两台主机互为备机。

RoseMirrorHA 通过网络在两台[主机](https://baike.baidu.com/item/%E4%B8%BB%E6%9C%BA)之间进行实时的数据复制。当 Active 主机发生故障时， RoseMirrorHA 将自动将服务迅速的切换到备机。并在备机镜像数据打基础上，继续为客户端提供业务报务。

RoseMirrorHA 主要功能特点 :

**· ****无缝集成到既有系统环境**

RoseMirrorHA 支持客户既有的环境，充分利用客户既有的资源。充分保护用户的投资，保护用户既有的应用和数据。最大限度适应已有的软件和硬件环境，无需专门的设备和其它额外成本投入。

**· ****高效成熟的多种镜像方式**

支持完全[镜像](https://baike.baidu.com/item/%E9%95%9C%E5%83%8F)、差分镜像

完全镜像：将 Active 主机的数据无条件重新传输到 Standby 主机，不论 Standby 主机是否已经存在该文件，可以确保数据的完整和一致性。通常在初始化的时候，需要采用完全镜像的方式。

差分镜像：只传输 Standby 和 Active 不同的部分，而不必传送相同部分的数据，可以减少对网络等资源的使用。减少不必要的网络传输，提高数据镜像的效率。

· 按需复制性能资源最佳化

支持自定义复制数据集

RoseMirrorHA 支持复制数据集的定义，用户可以选择定制需要复制的目录、文件。RoseMirrorHA 的数据镜像是基于文件系统之上的，仅仅复制文件变化的部分。 RoseMirrorHA 通过自身的驱动程序来监控用户指定数据集。获取变化内容进行传输处理。这种以[字节](https://baike.baidu.com/item/%E5%AD%97%E8%8A%82)为单位的按需复制，充分保证了系统性能和效率的最佳化。

· 支持在线备份数据或维护

· 支持目标写入暂停

当需要对备机上复制的数据进行[备份](https://baike.baidu.com/item/%E5%A4%87%E4%BB%BD)、查看的操作，不希望新的数据写入时，可骑使用该功能暂停备机写入，暂停后数据仍将发送备机，备机将暂停后的[数据缓存](https://baike.baidu.com/item/%E6%95%B0%E6%8D%AE%E7%BC%93%E5%AD%98)起来，等待暂停恢复后写入。

· 支持 Active 主机传输暂停

RoseMirrorHA 允许对 Active 主机复制的数据暂停发送，暂停后变化的数据仍将被获取，变化的数据将被存入 pagefile ，等待传输暂停恢复后发送。

· 消除[备份窗口](https://baike.baidu.com/item/%E5%A4%87%E4%BB%BD%E7%AA%97%E5%8F%A3)

过备机写入暂停或主机传输暂停，可骑在确保[主机](https://baike.baidu.com/item/%E4%B8%BB%E6%9C%BA)应用在线持续运行的情况下，通过备机对数据进行备份到[磁带库](https://baike.baidu.com/item/%E7%A3%81%E5%B8%A6%E5%BA%93)等操作。即保证了业务的持续运行，性能不受影响，闲时又可以对数据进行更多方式，更加灵活的备份保护。同时备份操作的作业时间也有了很大的灵活性，不必等到晚上或是周末再进行。

