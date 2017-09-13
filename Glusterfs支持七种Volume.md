## 基本卷：

- (1)  distribute volume：分布式卷
    
    文件通过hash算法分布到所有brick server上，这种卷是glusterfs的基础和最大特点；实只是扩大的磁盘空间，如果有一个磁盘坏了，对应的数据也丢失，文件级RAID 0，不具有容错能力。
    
- (2)  stripe volume：条带卷

    类似RAID0，文件分成数据块以Round Robin方式分布到brick server上，并发粒度是数据块，支持超大文件，大文件性能高。
    
- (3)  replica volume：复制卷

    文件同步复制到多个brick上，文件级RAID 1，具有容错能力，写性能下降，读性能提升。

## 复合卷：

- (4)  distribute stripe volume：分布式条带卷

    brickserver数量是条带数的倍数，兼具distribute和stripe卷的特点。
    
- (5) distribute replica volume：分布式复制卷

    brickserver数量是镜像数的倍数，兼具distribute和replica卷的特点,可以在2个或多个节点之间复制数据。

- (6) stripe replica volume：条带复制卷

    类似RAID 10，同时具有条带卷和复制卷的特点。

- (7) distribute stripe replica volume：分布式条带复制卷

    三种基本卷的复合卷，通常用于类Map Reduce应用。
