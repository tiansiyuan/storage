
# SAS 硬盘

SAS, Serial Attached SCSI，即串行连接SCSI，是新一代的 SCSI 技术，和现在流行的 Serial ATA(SATA) 硬盘相同，都是采用串行技术以获得更高的传输速度，并通过缩短连结线改善内部空间等。SAS是并行[SCSI接口](https://baike.baidu.com/item/SCSI%E6%8E%A5%E5%8F%A3)之后开发出的全新接口。此接口的设计是为了改善存储系统的效能、可用性和扩充性，并且提供与[SATA硬盘](https://baike.baidu.com/item/SATA%E7%A1%AC%E7%9B%98)的兼容性。

## 功能特点

SAS的接口技术可以向下兼容SATA。具体来说，二者的兼容性主要体现在[物理层](https://baike.baidu.com/item/%E7%89%A9%E7%90%86%E5%B1%82)和协议层的兼容。在物理层，SAS接口和[SATA接口](https://baike.baidu.com/item/SATA%E6%8E%A5%E5%8F%A3)完全兼容，SATA硬盘可以直接使用在SAS的环境中，从接口标准上而言，SATA是SAS的一个子标准，因此[SAS控制器](https://baike.baidu.com/item/SAS%E6%8E%A7%E5%88%B6%E5%99%A8)可以直接操控SATA硬盘，但是SAS却不能直接使用在SATA的环境中，因为SATA控制器并不能对SAS硬盘进行控制；在协议层，SAS由3种类型协议组成，根据连接的不同设备使用相应的协议进行数据传输。其中串行SCSI协议(SSP)用于传输SCSI命令；SCSI管理协议(SMP)用于对连接设备的维护和管理；SATA通道协议(STP)用于SAS和SATA之间数据的传输。因此在这3种协议的配合下，SAS可以和SATA以及部分SCSI设备无缝结合。

SAS硬盘算是机械硬盘中速度最快的了，首先接口上SAS接口就比SATA和SCSI的机械硬盘快，其次加上转速快，寻道快，所以SAS硬盘都被应用到无盘服务器上做读或写。

SAS系统的背板(Back Panel)既可以连接具有双端口、高性能的SAS[驱动器](https://baike.baidu.com/item/%E9%A9%B1%E5%8A%A8%E5%99%A8)，也可以连接高容量、低成本的SATA驱动器。所以SAS驱动器和SATA驱动器可以同时存在于一个[存储系统](https://baike.baidu.com/item/%E5%AD%98%E5%82%A8%E7%B3%BB%E7%BB%9F)之中。但需要注意的是，SATA系统并不兼容SAS，所以SAS驱动器不能连接到SATA背板上。由于SAS系统的兼容性，使用户能够运用不同接口的硬盘来满足各类应用在容量上或效能上的需求，因此在扩充存储系统时拥有更多的弹性，让存储设备发挥最大的投资效益。

在系统中，每一个SAS端口可以最多可以连接16256个[外部设备](https://baike.baidu.com/item/%E5%A4%96%E9%83%A8%E8%AE%BE%E5%A4%87)，并且SAS采取直接的点到点的串行传输方式，传输的速率高达3Gbps，估计以后会有6Gbps乃至12Gbps的高速接口出现。SAS的接口也做了较大的改进，它同时提供了3.5英寸和2.5英寸的接口，因此能够适合不同服务器环境的需求。SAS依靠SAS扩展器来连接更多的设备，SAS的扩展器以12端口居多，不过根据[板卡](https://baike.baidu.com/item/%E6%9D%BF%E5%8D%A1)厂商产品研发计划显示，未来会有28、36端口的扩展器引入，来连接SAS设备、主机设备或者其他的SAS扩展器。

和传统并行SCSI接口比较起来，SAS不仅在接口速度上得到显著提升(主流Ultra 320 SCSI速度为320MB/sec，而SAS才刚起步速度就达到300MB/sec，未来会达到600MB/sec甚至更多)，而且由于采用了串行线缆，不仅可以实现更长的连接距离，还能够提高抗干扰能力，并且这种细细的线缆还可以显著改善机箱内部的散热情况。[1][ ]()

## 外界评论

SAS 的不足主要有以下方面：

- 硬盘、控制芯片种类少：只有[特科芯](https://baike.baidu.com/item/%E7%89%B9%E7%A7%91%E8%8A%AF)、[希捷](https://baike.baidu.com/item/%E5%B8%8C%E6%8D%B7)、[迈拓](https://baike.baidu.com/item/%E8%BF%88%E6%8B%93)以及[富士通](https://baike.baidu.com/item/%E5%AF%8C%E5%A3%AB%E9%80%9A)等为数不多的硬盘厂商推出了SAS接口硬盘，品种太少，其他厂商的SAS硬盘多数处在产品内部测试阶段。此外周边的SAS控制器芯片或者一些SAS[转接卡](https://baike.baidu.com/item/%E8%BD%AC%E6%8E%A5%E5%8D%A1)的种类更是不多，多数集中在LSI以及Adaptec公司手中。
- 硬盘价格太贵：比起同容量的Ultra 320 SCSI硬盘，SAS硬盘要贵了一倍还多。一直居高不下的价格直接影响了用户的采购数量和渠道的消化数量，而无法形成大批量生产的SAS硬盘，其成本的压力又会反过来促使价格无法下降。如果用户想要做个简单的RAID级别，那么不仅需要购买多块SAS硬盘，还要购买昂贵的RAID卡，价格基本上和硬盘相当。
- 实际传输速度变化不大：SAS硬盘的接口速度并不代表[数据传输速度](https://baike.baidu.com/item/%E6%95%B0%E6%8D%AE%E4%BC%A0%E8%BE%93%E9%80%9F%E5%BA%A6)，受到硬盘机械结构限制，SAS硬盘的机械结构和SCSI硬盘几乎一样。数据传输的瓶颈集中在由硬盘内部机械机构和硬盘存储技术、磁盘转速所决定的硬盘内部数据传输速度，也就是80MBsec左右，SAS硬盘的性能提升不明显。
- 用户追求成熟、稳定的产品：从已经推出的产品来看，SAS硬盘更多的被应用在高端4路服务器上，而4路以上服务器用户并非一味追求高速度的硬盘接口技术，最吸引他们的应该是成熟、稳定的硬件产品，虽然SAS接口服务器和SCSI接口产品在速度、稳定性上差不多，但的技术和产品都还不够成熟。

不过随着[英特尔](https://baike.baidu.com/item/%E8%8B%B1%E7%89%B9%E5%B0%94)等主板[芯片组](https://baike.baidu.com/item/%E8%8A%AF%E7%89%87%E7%BB%84)制造商、[希捷](https://baike.baidu.com/item/%E5%B8%8C%E6%8D%B7)等硬盘制造商以及众多的服务器制造商的大力推动，SAS的相关产品技术会逐步成熟，价格也会逐步滑落，早晚都会成为[服务器硬盘](https://baike.baidu.com/item/%E6%9C%8D%E5%8A%A1%E5%99%A8%E7%A1%AC%E7%9B%98)的主流接口。

现阶段已经成为云服务器服务商的主流接口。