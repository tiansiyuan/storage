# 大话存储 II 笔记

国内存储厂商

- 爱数软件
- 星火高科
- 中科蓝鲸
- 华赛

"连找发"

CHS：柱面、磁头、扇区

LBA (Logical Block Address) 线性地址

交叉因子

SCSI 接口协议

排队

无序传输，旋转延迟

磁头扫描方式

- FCFS
- SSTF
- SCAN
- C-SCAN
- LOOK/C-Look

ATA - IDE
ATA - SATA
SCSI - SCSI
SCSI - SAS
SCSI - SSA
SCSI - FCP

PIO
DMA
Ultra DMA

LVD - Low Voltge Differential

LUN - Ligical Unit Number

IOPS

SSD - Solid State Drive: Flash/DRAM chip

NAND flash

page -> block -> plane

SSD 的 IO 最小单位为 1 个 page。

TRIM - 定时清理垃圾。

AST -  Automatic Storage Tiering

## 七种 RAID

RAID 0：条带 stripee

RAID 1: 镜像

RAID 2：专用，已淘汰。1b。

RAID 3：改进2。提高数据传输率，不能并发。

RAID 4：可并发，唯有NetApp 的 WAFL 支持，面临淘汰。校验盘征用。

RAID 5：高盲并发。整条写，重构写，读改写。打散校验盘到每块磁盘。

RAID 6：增加5 的保险系数，多了一块校验盘。可以容忍两块盘损坏。

## 第五章，RAID、虚拟磁盘、卷和文件系统

软件 RAID。

RAID 卡。

中高端 RAID 卡一般有 256MB RAM 作为缓存。

初始化，磁盘清零。

RAID 组合， X0。

## 第六章，磁盘阵列

JBOD - Just a Bunch of Disks

LUN，是 SCSI 协议中的名词，是比 SCSI-ID 更细一级的寻址 ID，每个可对应一个虚拟磁盘。

后来，在硬件层面生成的虚拟磁盘称为 LUN，软件层面的称为卷。

双控制器，Active-Standby，Dual-Active, Split Brain

SAN - Storage Area Network

## 第七章，OSI

## 第八章，Fibre Channel

FC 协议。

网络拓扑：FC-AL(环)，Fabric(网)。

WWNN - World Wide Node Name

WWPN - World Wide Port Name

比以太网复杂得多。

物理介质不仅是光纤。

FCP，SCSI over FC。代替SCSI 并行总线传输模块，下四层；保留上三层。

## 第九章，

后端 FC。

FC-AL，一半数（~60）节点，性能最佳。

SAS, Serial Attached SCSI

全交换式架构

挑战 FC。

## 第十章，DAS，SAN 和 NAS

网络文件系统

CIFS，NFS

RPC FS

WAFL - Write Anywhere Filesystem Layout

## 第十一章

以太网和TCP/IP。

CSMA/CD - 载波监听/冲突检测

## 第十二章

IP SAN：以ISCSI 为代表的以TCP/IP作为传输方式的网络存储系统。

CO - Checksum Offload

LSO - Large Send Offload

TO - TCP/IP Offload = TOE - TO Engine card

SO - Security Offload：TO + IPSEC

IO - ISCSI Offload

FC SAN 节节败退

- 成本

- 可扩展性

- 易用性

- 兼容性

## 第十三章， IP 与 FC 融合

Protocol over Protocol

ARP, 将一种网络地址映射为另一种网络地址。

以太局域网内，NetBEUI 比TCP/IP的性能高很多。

网络通信协议的四级结构：

- Payload 层
- 信息表示层
- *交互逻辑层*， 协议涉及思想
- 寻址层

协议融合方式：

- Use
- Tunnel
- Map

## 第十四章，虚拟化

VFS

带内虚拟化

带外虚拟化：IBM SanFS

VTL, Virtual Tape Library

## 第十五章，存储集群

HAC, Avalibility

LBC, Load Balance

HPC, Performance

LVS, TCP

- 基于Block协议访问的传统存储集群
- 基于NAS协议访问的存储集群

SMP

NUMA（Non Uniform Memory Access Architecture）

MPP

写即作废（Invalidate on Write）

Scale Up

Scale Out

OSS/OSD, Object Storage Device.

IO三大件：目标、起始地址、长度

共享与非共享存储集群

CAP

NWR

## 第十六章，数据保护和备份

Redirect on first write

Copy on first write

CDP，Continuous Data Protect

## 第十七章，数据容灾

## 第十八章，数据前处理与后处理

数据存储

数据管理

Thin Provision/Over Allocation

HSM, 分层存储管理

Dedup

## 地十九章，系统IO路径及优化

