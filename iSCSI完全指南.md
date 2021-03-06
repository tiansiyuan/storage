引:在上世纪末、本世纪初，一提到SAN（Storage Area Network），我们立刻就会想到光纤通道（FC，Fiber Channel）技术，也即那时候的SAN多半单指FC而言。一直到iSCSI问世，为了方便区隔，业界才分别以FC-SAN及iSCSI-SAN的称呼加以分辨。

当时与SAN相对应的是在多用户网络环境中，采用文件协议(File Protocol)数据存取方式的NAS(Network Attached Storage，网络附加存储)方案。它的出现，为以太网络的成熟及重要，做了最佳脚注。

日益成熟的因特网进一步成为了IP存储方案成长壮大的最佳腹地及平台，现成的架构、协议、标准、基础设施及管理工具，莫不吸引着寻求最佳存储方案者的目光。此一背景，加上FC SAN“高不可攀”的成本及管理门坎的障碍，另一存储成员iSCSI(Internet SCSI)也来报到了。

iSCSI的出现，标志着低价化SAN方案的问世，也一偿中小企业建置SAN的美梦。

**从IP SAN到iSCSI SAN**

所谓iSCSI亦即透过IP网络，将SCSI块数据转换成网络封包的一种传输标准，它和NAS一样透过IP网络来传输数据，但在数据存取方式上，则采用与NAS不同、却与FC-SAN相同的块协议(Block Protocal)。iSCSI最早是由IBM及Cisco于2001年制定的，两家并且分别推出了支持iSCSI的产品——IBM IP Storage 200i及Cisco SN5420 Router。

事实上，为了解决FC-SAN在价格及管理上的诸多门坎，各家早有不同协议的IP SAN的研究开发。这些IP SAN的架构，其实与iSCSI大同小异，只不过并非走标准化的协议(事实上，在iSCSI标准化之前，也没有什么标准不标准的问题)，而是各家自行研发的协议，所以基本上各家IP SAN是不兼容的。

据NetApp表示，该公司早在2001年年底即推出了自家的IP SAN，它采用的是自行开发的VLD协议(Virtual Local Disk)，存储上属于Block over IP方式。

2003年2月，当IBM早已退出iSCSI之际，NetApp宣称推出了iSCSI正式标准制定之后的全球第一台iSCSI产品。

**两大推波助澜的关键促因**

早先在iSCSI尚未标准化之前，只有少数厂商敢投注心力在IP SAN的开发上，但也因为每一家厂商皆开发专属封闭协议的解决方案，所以这些方案之间并无法完全兼容。而当时的市场上，由于发展iSCSI的厂商很少，所以支持的平台及软硬件等基础设施便相当贫乏，这可说是iSCSI发展之初的最大阻碍及瓶颈。

但接下来的两大事件，却被视为促进iSCSI大行其道的关键因素，那就是iSCSI标准的正式通过，以及微软的正式支持。

在众所期盼的敦促下，SNIA(Storage Networking Industry Associate，存储网络工业协会)终于在2003年2月正式制定通过了iSCSI标准。而业界莫不把此标准化视为iSCSI发展历程中的最关键因素，自此开始，有愈来愈多的厂商开始进一步开发合乎业界标准的相关产品，iSCSI也开始受到业界目光的青睐。

在iSCSI的发展过程中，除了正式标准化具有重大意义外，微软紧接在2003年5月于已上市近1个月的Windows Server 2003 中，正式开始支持iSCSI，并提供iSCSI Initiator驱动程序的下载。微软此项深具推波助澜的作法，带动了整个iSCSI业界的发展。所以接下来，不论各类作业平台或软硬件的支持会愈来愈齐备。

iSCSI之所以被看好的原因不少，首先它根植于IP网络上，所以可以采用现有已非常成熟的管理工具及基础建设，可为企业节省大笔建置、管理及人事成本。更重要的是，懂IP的人才资源非常丰沛，成为助长iSCSI发展的中坚份子。此外，iSCSI在数据传输距离上，几乎没有限制的优点，更紧紧吸引无数企业的目光。

**2005年将是iSCSI出头年**

自从标准化及微软支持解决了iSCSI最大的发展瓶颈之后，iSCSI的全面普及也只是时间早晚的问题而已。但业界对其开始普及的时间点一直莫衷一是。一般调查机构多半认为该时间点应在2006年，但各家厂商却异口同声地认为2005年就有机会看到市场大幅起飞。

姑且不论这是否是业界的信心喊话或策略性动作，但他们却认为一开始推展的领域会以中小企业为主，至于较高端的存储市场则比较没有机会。尤其对于中小企业为主干的亚太区市场，架设iSCSI SAN将是最经济的SAN解决方案。有些意识到这点的国际大厂，甚至推出了专为亚太地区用户设计的iSCSI产品，典型的例子便是2004年10月HP发布的IP Storage 500/1500。

**10G以太网会是iSCSI茁壮成长的基石**

对于iSCSI的未来发展，NetApp(Network Appliance)及建联科技(Raidsys)都认为SAN与NAS的整合会是一大趋势，两家也已经有相关产品及解决方案的推出。此外，展望未来，iSCSI厂商莫不期盼新一代10G以太网的到来，因为在10G以太网的带动下，iSCSI的理论带宽将会攀升到10Gb的高水平，那么即使未来FC提升到新一代的4Gb，仍然不是iSCSI的对手。如此截然不同的情势逆转，难怪让不少厂商面露既兴奋又憧憬的表情。其中，NetApp甚至表示，2005年即会开始推出支持10G的iSCSI产品，此无异让10Gb高速美梦成真的可能性提高不少。

但博科(Brocade)通讯系统公司的资深技术顾问却非常怀疑10G以太网推行后，iSCSI性能是否真能获得大幅提升。他表示即使网络带宽达到10G速度，但主机端(Initiator端)及Target端存储装置的I/O，却不一定赶得上这样的速度。如果不能的话，整体效能还是上不来。

在2005年春季IDF上，英特尔公布的I/O 加速技术 (I/O Acceleration Technology)则驳斥了这种怀疑，进一步扫清了iSCSI应用的性能瓶颈。据悉，这一技术能够使网络数据与服务器应用之间的交互速度提高30%。

英特尔I/O 加速技术可弥补现有iSCSI TOE技术的不足。TOE指定一个昂贵的专用芯片来卸载协议计算，但它不能完全解决CPU的两个最大负担――系统操作或内存访问。鉴于此，TOE仅会在处理大型数据包有效负载时才会发挥出最明显的作用。

英特尔通过提高芯片组和网络控制器向内存输入输出数据的响应能力，优化TCP/IP协议，减少处理器介入缓解，从而可以提高iSCSI的性能，并减少了一半服务器处理器的负载。

微软将在未来Windows Server版本中支持英特尔I/O加速技术，新版操作系统还将包括能够有效平衡多内核CPU之间的网络TCP/IP流量的技术。

**iSCSI与各类型存储方案综合评比**

与Fiber Channel（以下简称FC）一样，iSCSI也属于SAN大家庭中的一员，它的问世显然是冲着FC SAN的缺点而来的。长久以来，FC几乎成了SAN的代名词，但由于相关软硬件的建置成本偏高、管理技术及门坎也较高，所以几乎只有中大型企业才有能力做这方面的建置与规划，中小企业限于自身规模，也只有望洋兴叹、徒唤奈何的份。

**无传输距离限制、建置管理成本低是最大特点**

iSCSI最重要的就是能在成本上提出大幅改善的方案，也因此打破了SAN为中大型企业禁脔的藩篱，让中小企业也能享受到SAN所带来的好处及便利。到底是哪些优良特质，让iSCSI成为目前存储业界最热门的话题呢？以下我们做一番简要的归纳及分析：

- 构建成本低廉

  不论是适配卡、 交换机或缆线的购置，iSCSI都比FC便宜许多。其中适配卡部分，只要Host端主机本身内建的一般网络卡或网络芯片，搭配免费下载的iSCSI Initiator驱动程序即可，所以在适配卡方面可以达到完全免费的境界。

- 管理门坎及维护成本更低

  一般来说，FC SAN多半需要特定的工具软件来操作管理，所以需要对人员进行一定时间的教育训练，而且费用不低。但由于iSCSI乃透过IP网络来传输数据及分配存储资源，所以只要使用网络现有的管理功能即可，相较起来，的确可以省下大笔管理人力及训练成本。

- 节省存储资源、做好集中管理

  由于iSCSI与FC同样支持块协议的数据存取模式，所以比采用文件协议(File Protocol)的NAS，更能透过集中管理的方式，有效避免存储资源的浪费，进而节省不必要支出。

- 没有距离的限制

  由于iSCSI是透过无处不在的IP网络来传输数据，所以理论上，传输距离也可达到无限制的境界，这对于异地数据的传输及灾备等应用相当有帮助。

- 传输速度够快

  拜GbE网络之赐，理论上，iSCSI的速度可达1Gb，虽然速度仍比不上FC SAN的2Gb，但效能上已超越大部分的NAS。更重要的是，一旦10Gb以太网络普及的时候，iSCSI就可能以10Gb的高速狂飙，甚至比FC SAN的新一代版本——4Gb还要快。

- 人才较多

  随着因特网的日益兴盛，造就了取之不尽、用之不竭的TCP/IP网络人才，比起门坎较高的FC SAN来说，专走IP网络的iSCSI可谓占尽优势。
 
**数据碰撞及支持性低等问题成为推展阻力**

天底下没有十全十美的事物，虽然iSCSI的优点不少，而且十分抢眼，但仍有许多待解决的缺点，以下就让我们一起分析看看iSCSI到底有哪些缺陷：

1. 扰人的噪声碰撞问题

   由于iSCSI走的是IP网络，其中当然充斥着来自全球各地的庞大数据及噪声，所以碰撞情形也就在所难免了，如此一来，在数据传输的过程中，就很容易导致延迟的情形发生，大大影响了传输的效能，甚至数据的正确性。针对这类问题，不少厂商专研解决之道，其中像是乔鼎信息(Promise)即宣称，该产品提供的Data Digest功能，可有效解决噪声问题。

2. 仍有改进空间的效能瓶颈

   这方面可分成下列几项来讨论。

   (1) 传输带宽问题：前文已提到，目前的1Gb带宽，尚不及FC的2Gb，这方面待要等到10Gb以太网络普及之后，才有可能赶上。但就目前企业的网络状况来看，GbE以太网络的普及率都有待加强了，所以10Gb何时来临，还是未定之数。

   (2) 流量控制问题：这方面也没有FC来得好。

   (3) I/O端的速度限制：Brocade指出在Host主机及Target存储设备两处的I/O端速度一直不上来，所以即使10Gb以太网络真的普及，I/O端的速度瓶颈仍然会拖跨这个传输效能。

   (4) 软件iSCSI Initiator效能不佳：其乃透过软件仿真来执行SCSI指令，所以会耗费掉大量的CPU资源，造成整体效能的低落。这个问题虽然可以透过安装频率较高的CPU来解决，喽缘乇慊嵊卸钔獾某杀局С觥?lt;/P>


3. 硬件iSCSI适配卡较贵

   如果想要让整体效能有好的表现，那么就必须添置较贵的iSCSI HBA卡或稍贵的TOE(TCP Offload Engine，TCP卸载引擎)HBA卡，整体成本会因而大幅攀升。据Brocade指出，不论是FC HBA卡或FC交换机的价格都在逐步调降中，同时该公司会推出价格颇为低廉的FC交换机，如此一来，在寻求高效能的前提下，iSCSI的成本优势会相对减少。

4. 支持的平台及软硬件仍少

   虽然目前Windows、Linux、UNIX、Netware都已陆续推出软硬件的Initiator，但数量及完备性仍不足，尤其是版本特多的Linux，目前只有SuSE及Redhat有解决方案；其中，SuSE只有软件、Redhat只有硬件。此外，HP-UX及Novell Netware只有软件，SUN Solaris则只有硬件，而且一些平台上的设置十分复杂困难。换句话说，目前只有微软Windows平台具备最完备的支持性。但是目前业界及政府机构的数据中心，有相当数量是采用非Windows操作系统，再加上也有不少公司内部系统是属于多种操作系统环境，所以各平台解决方案的提出，仍是iSCSI急待解决的重要课题。

5. 令人质疑的安全性

   IP网络环境复杂，再加上懂IP的人相对的多，所以安全性也相对地令人质疑。

6. 无法兼顾效能及跨平台性

   前面已提到iSCSI Initiator可分为三种，亦即软件Initiator驱动程序、硬件的TOE HBA卡及iSCSI HBA卡。就效能而言，Initiator驱动程序最差、TOE居中、iSCSI HBA卡最佳。但是iSCSI HBA只能走iSCSI协议，而无法透过NFS(Network File System，SUN制定)或CIFS(Common Internet File System，微软制定)等档案系统协议与应用服务器沟通。但Initiator驱动程序及TOE则同时支持iSCSI、NFS及CIFS三种协议。

**iSCSI、SAN及NAS大比拼**

一般来说，企业在面临iSCSI SAN存储解决方案时，多半喜欢拿FC SAN及NAS与其做一番比较。在此先就FC与iSCSI做一比较，基本两者同属走块协议的SAN架构，只不过前者透过FC，后者藉由IP传输数据罢了，而两者在管理及应用上也大同小异，其间只不过优劣好坏的差异。

至于SAN与NAS的差异而言，许多iSCSI厂商都认为SAN与NAS是完全不同架构的存储方案，前者支持块协议，后者则支持文件协议，所以拿两个完全不同协议及架构的标准相比，是不太适宜的。

如果硬要从中做个区别的话，精业公司倒提出了一个简单易懂的区别方法，那就是SAN的精髓在于分享存储设备(Sharing Storages)；NAS则在于分享数据(Sharing Data)。总而言之，NAS与SAN因为架构及应用领域的不同，所以不会相互取代，而会共存于企业存储网络之中。

无论如何，为了让读者进一步了解iSCSI、FC及NAS的差异，在此还是尽量做一番归纳整理，以供读者参考：

接口技术：iSCSI和NAS一样透过IP网络来传输数据，FC则不一样，数据是透过光纤通道(Fibre Channel)来传递。

数据传输方式：同为SAN的iSCSI及FC都采用块协议方式，而NAS则采用文件协议。

传输速度：就目前的传输速度而言是FC(2Gb)最快、iSCSI(1Gb)次之，NAS居末。基本上，FC及iSCSI的块协议会比NAS的文件协议来得快，这是因为在操作系统的管理上，前者是一个“本地磁盘”，后者则会以“网络磁盘”的名义显示。所以在大量数据的传输上，iSCSI 绝对会比NAS快得多。

资源共享：iSCSI和NAS共享的是存储资源，NAS共享的是数据。

管理门坎：iSCSI和NAS都采用IP网络的现有成熟架构。所以可延用既有成熟的网络管理机制，不论是建置、管理或维护上，都非常方便及容易。而FC则完全独立于一般网络系统架构，所以需由FC供货商分别提供专属管理工具软件。

管理架构：透过网络交换机，iSCSI及FC可有效集中控管多台主机对存储资源的存取及利用，善用资源的调配及分享，同时速度上也快于网络磁盘的NAS。

成本：比起FC而言，以太网络是个十分成熟的架构，而熟悉的人才甚多，所以同样采用IP网络架构的iSCSI及NAS，构建成本低廉、管理容易而维护方便。至于与FC在构建成本上的进一步比较，可见表1。

传输距离：原则上，三者都支持长距离的数据传输。FC的理论值可达100公里。透过IP网络的NAS及iSCSI理论上都没有距离上的限制，但NAS适合长距小文件的传输，iSCSI则可以进行长距大量资料的传递。

系统支持：相较起来，iSCSI仍然比较少。FC主要是由适配卡供货商提供驱动程序和简单的管理程序。
iSCSI市场现状剖析

所幸SNIA协会在2003年2月正式通过了iSCSI标准， iSCSI厂商终于可以开发出彼此兼容的软硬件方案及产品。

虽然iSCSI已正式标准化，但不一定代表从此就能开花结果，毕竟iSCSI是否能在企业存储市场站稳脚步，仍需看厂商本身的参与态度及开发意愿。没有厂商会对未知的领域投下无谓的投资及心力，而这也是厂商面对iSCSI时驻足观望的原因。

**WinTel的重量级支援**

若这个时候一些大厂愿意站出来登高一呼的话，厂商里足观望的僵局就能被打破。在iSCSI正式标准化之后不久，微软十分看好iSCSI的发展，毅然决然地挺身扮演推动者的关键角色，在2003年2月间，也就是几乎在SNIA协会通过iSCSI标准的同时，便提供iSCSI Beta版驱动程序的在线下载服务。

接着同年5月，微软在发布Windows Server 2003时对外正式宣称会对iSCSI加以支持。到了7月，微软果然没有食言，紧接推出了支持iSCSI标准的Windows操作系统更新程序，该程序完全免费下载，可同时支持Windows 2000/XP与Windows Server 2003等不同操作系统。此外，微软还推出了代号Chimney的TCP/IP Offload架构，并得到了Alacritech和Adaptec等iSCSI HBA供应商的支持。

微软坚决支持iSCSI似乎没有停竭之势，2003年11月，在标志着微软积极跨入企业存储市场的重头产品——Windows Storage Server 2003(WSS 2003)之中继续大力支持iSCSI。而2004年4月发表的Microsoft Exchange Server 2003也同时对iSCSI 及NAS加以支持。

在上述一连串的动作中，微软从个人端的WinXP，到企业服务器的Windows Server 2003，到E-mail Server，再到中小企业Storage Server，全都加以支持，如此巨细靡遗的动作，可以看出微软对iSCSI前景的看好，同时也显露该公司对中小企业存储市场的野心。

另一个重量级的大厂，也就是身为WinTel王国的另一支柱Intel，也早在2003年2月即推出型号为PRO/1000T IP的TOE(TCE Offload Engine)HBA适配卡。比起微软或其它操作系统厂商提供的iSCSI Initiator软件，Intel PRO/1000T IP适配卡提供了TCP卸载(Offload)的功能，可有效降低CPU的占用率，从而使整体效能有所提升。总而言之，iSCSI有了WinTel两大支柱的重量级支持，势必会带动整个业界的正面回响，并在中小企业存储市场蔚成一股新兴势力。


**支持尚未全面 普及仍需努力**
　　
不过，精业公司却认为，目前市面上的信息中心及各企业的网管单位所采用的操作系统，并非完全局限于Windows系统，反而是充斥着Unix、Linux、SUN Solaris等林林总总的各种操作系统，换句话说，Windows只不过是众多操作系统中的一个罢了。更重要的是，其它操作系统对iSCSI的支持，并没有像Windows如此完备，其中不是只有软件驱动程序，就是只有硬件适配卡的提供，甚至也有完全没任何解决方案的平台。所以虽然微软全面支持iSCSI，但不表示整个市场都已有iSCSI解决方案。
　　
就整体趋势而言，市场上对iSCSI的支持是不断地在增加之中的。其中，在Linux方面，已有支持RedHat的适配卡，而SuSE也已有Initiator软件的支持。在Unix方面，除了IBM AIX早有支持外，HP-UX也有Initiator软件。至于Sun Solaris则软硬件的支持皆有，Novell Netware 6.5也已提供Initiator软件。最近，Cisco也推出了针对SUN专用的Initiator软件，接下来不久，该公司也会推出支持HP的Initiator软件。
　　
**代表性厂商及代表性方案**
　　
目前市面上，除了各类操作系统的Initiator软件之外，市面上已有愈来愈多厂商推出各种各类的iSCSI相关产品。以下就以iSCSI SAN网络中的组成要件——iSCSI适配卡、iSCSI交换机、iSCSI 存储服务器、iSCSI存储设备、iSCSI 桥接器及iSCSI网关来做逐一的剖析及介绍。
　　
1. iSCSI适配卡
　　
iSCSI适配卡大致分成两类，一为TOE HBA卡，一为iSCSI HBA卡，前者价格较便宜，后者效能极佳，但价格非常昂贵。代表性的厂商有Adaptec、Alacritech、Intel、LSI、Qlogic等，其中Intel专注于TOE HBA卡的开发。

Alacritech iSCSI HBA SES 1001.jpg

2. iSCSI交换机

一般来说，在iSCSI SAN的网络架构中，只要用一般Gigabit以太网络交换机就可以运作。但目前已有全新iSCSI交换机的推出，代表性厂商有Cisco、McData、Sanrad(V-Switch)等。其中，Cisco更是这方面的先驱，早在2001年之际，该公司即联合IBM共同推出全球最早的iSCSI解决方案，当时Cisco即推出iSCSI路由器——SN5420。

3. iSCSI存储服务器

在iSCSI 存储服务器方面，不但历史最久远，而且代表性的厂商颇多，较具代表性的有IBM、NetApp、EMC、微软、飞康国际及DataCore(SANmelody)等。这方面的开山祖师当推IBM莫属，早在2001年，IBM即推出全球第一台的iSCSI存储服务器——IP Storage 200i，但由于当时的iSCSI尚未标准化，所以业界对该产品及标准的支持性及接受度都非常低，事情发展到最后，就是这只一向飞得太快、太远的大飞象，不得不黯然暂离iSCSI的市场。不过如今，IBM又重回iSCSI的怀抱，并推出了全新产品——TotalStorage DS300。

向以NAS方案著称于世的NetApp(Network Appliance)早在2003年，iSCSI标准通过之际，即推出支持iSCSI的文件服务器，目前NetApp的代表性产品为F800系列及FAS900系列Server。此外，EMC也在Symmetrix DMX系列方案及新款EMC CELERRA NAS系统中开始支持iSCSI标准。
　≈劣谖⑷碓谡夥矫妫浠瓤伤滴奕四艿校С值牟妨绽怕浚╓SS 2003及Exchange Server 2003。其中WSS 2003同时支持NAS及iSCSI，不少厂商藉此与微软合作，推出基于WSS 2003的存储服务器，例如飞康国际(FalconStor)、技嘉及广达等公司都有这方面的iSCSI产品推出。

4. iSCSI存储设备

目前最常见的iSCSI存储设备首推磁盘阵列及磁带库。前者的代表性厂商有Adaptec(iSA1500)、HDS(Thunder 9500)、乔鼎信息(Promise VTrak 15200)、建联科技(Raidsys 15200)及普安科技等。

至于iSCSI磁带库的厂商则有ADIC(Scalar i2000)、SpectraLogic、Quantum、耐特普罗(NetPro Virtual Tape Library)、Overland等。


图：Adaptec iSA1500


图：HDS Thunder 9500磁盘阵列

Dell EMC AX100i

5. iSCSI桥接器

也就是将一般的SCSI设备对iSCSI的转换器，其代表性厂商为ATTO，目前的产品为iPBridge 2500。

6. iSCSI网关

iSCSI网关可做为光纤通道协议与iSCSI协议之间的桥梁，目前代表性厂商为博科通讯(Brocade)和McDATA。

 对于有意构建iSCSI SAN的企业来说，面对市面上林林总总的各式iSCSI产品，往往会有无所适从的感觉，而在心中浮现许多待解的问题：例如到底要购买哪些配备？而每个配备在iSCSI SAN中扮演的角色为何？企业内部的旧有配备是否可以融合到iSCSI SAN之中？这些问题关系到了成本、效益、需求及兼容性等层面及环节，接下来笔者会以范例方案的方式，来逐一解决上述的疑问，并希望藉此能给读者们有用的参考信息。

就一个完整的iSCSI SAN来说，其构成要件大致如下：

A. iSCSI适配卡(a.Gigabit网络卡)

B. iSCSI交换机(b.Gigabit交换机)

C. iSCSI存储服务器

D. iSCSI存储设备(d.SCSI存储设备)

E. iSCSI桥接器

F. iSCSI网关

理论上iSCSI接口的组件大概有上述六种，在此并以大写字母来表示，至于括号内小写字母的组件，则是可以取而代之的非iSCSI接口组件，这些组件通常也是企业内常见的既有设备。

在此要强调的是，并非以上所有的iSCSI接口组件都要购齐，才能建置iSCSI SAN，而应该是对企业自身的现阶段需求、预算成本、现有环境及配备做综合性的搭配考虑。接下来仅就成本、效能及新旧搭配等因素提供几种方案，供读者们参考。

**方案一 a+b+d + E(超经济方案)**

优点：这应该是最经济实惠的iSCSI-SAN方案，因为只要买iSCSI 桥接器就好。值得一提的是公司只要用既有的网卡及交换机即可，完全不用再添购任何配备，就可以构建一个iSCSI-SAN。

缺点：比起硬件式的iSCSI适配卡，iSCSI Initiator驱动程序在性能上会比较差。

先决条件：公司内部必须要有SCSI接口的存储设备，如SCSI 磁盘阵列或SCSI磁带库。另外要有Gigabit网卡及Gigabit交换机，千万不要用10/100 Base的网卡及交换机，因为性能会非常差，根本没有实用性可言。另外要提醒的是，为求性能，Initiator端主机的CPU要超过1GHz。

注意事项:：必须要下载免费的iSCSI Initiator驱动程序，才可以将一般Gigabit网卡仿真成iSCSI Initiator。然后再透过iSCSI桥接器将一般SCSI接口的存储配备仿真成iSCSI Target，如此就形成一个iSCSI-SAN。

**方案二 a+b+C+D(次经济方案)**

优点：网络卡及交换机皆可用现成的，只要购买iSCSI存储服务器及iSCSI存储设备即可，而市面上多半都将iSCSI存储服务器及存储设备搭成一个方案销售。例如技嘉、广达推出的WSS 2003存储服务器，Promise VTrak 15200搭配DataCore SANmelody的方案都是常见的销售模式。

缺点：与方案1一样，性能上会比较差。如果主机CPU超过1GHz不会差到那里，但如果是1GHz以下，那就只能忍受性能的低下了，再不然就要另外花费做升级CPU的动作。

先决条件：要有Gigabit网卡及Gigabit交换机。此外，Initiator端主机的CPU要超过1GHz。

注意事项:：必须要下载免费的iSCSI Initiator驱动程序。

**方案三 A+b+C+D(高性能方案)**

优点：性能好，由于采用iSCSI适配卡，所以性能远比iSCSI Initiator驱动程序来得好。

缺点：比起完全免费的iSCSI Initiator驱动程序，iSCSI适配卡远比较贵。

先决条件：要有Gigabit交换机。

注意事项:：iSCSI适配卡分为较便宜性能也稍逊的TOE HBA卡，以及高效能但较贵的iSCSI HBA卡，但后者却只能走iSCSI协议，而无法透过NFS或CIFS等文件系统协议与应用服务器沟通。反而TOE HBA卡iSCSI、NFS及CIFS协议都支持，所以公司需视自身的需求及成本等因素来加以选择。

**方案四 A+B+C+D(超高性能方案)**

优点：性能最佳，同时市面上一些iSCSI交换机还可同时内建FC、Gigabit Ethernet、iSCSI等多种接口端口，应用上还提供了存储虚拟化等高端功能。所以不论是性能、功能及应用上都颇有看头。

缺点：前面已提到iSCSI适配卡很贵，而支持多种接口及高端存储功能的iSCSI交换机更是身价非凡。

先决条件：有同时整合FC、Gigabit Ethernet配备及网络的需求者。

注意事项：同上。

**方案五 Only F(iSCSI + FC SAN整合方案)**

优点：可以连结iSCSI及FC两个不同协议的SAN孤岛。也可以透过iSCSI协议，让两个距离很远的FC SAN孤岛相互连结，让FC SAN也可以享受超远距传输的功能，而勿需建置更为昂贵的FCIP连结方案。

先决条件：有整合iSCSI SAN及FC SAN的需求，以及让两个以上的FC SAN孤岛远距传输的需求者。

备注：基本上，方案5不能视为初次构建iSCSI SAN的参考案例，而只是透过iSCSI技术，解决公司既有iSCSI SAN及FC SAN的互连及整合需求。
在谈过了iSCSI的技术趋势、优缺点特性、业界支持状况及构建方案等议题后，本单元将与读者一同探讨采购iSCSI配备所应注意的环节及重点，以俾提供读者采购iSCSI配备及建置iSCSI SAN的一个参考依据。以下兹分成效能及成本、安全性、可扩充性、兼容性、应用及功能等5大基本采购原则来做讨论。

**性能及成本**

就目前而言，iSCSI SAN在性能及成本上的高低与否，最主要的关键就在于ASIC芯片上。相对于便宜又大碗的Initiator驱动程序而言，价格不便宜的iSCSI ASIC却最能符合性能及速度上的需求，例如制造业或金融业的数据库，就需要较高的速度来运作，这时候采用内建ASIC芯片的iSCSI适配卡会是最佳选择。

一般来说，随着ASIC芯片的有无，以及等级的高低，目前iSCSI Initiator可分为以下三种：

**1. iSCSI HBA卡：**

所谓iSCSI HBA卡就是采用内建SCSI指令及TOE引擎的ASIC芯片的适配卡，在三种iSCSI Initiator中，价格最贵，但性能最佳。目前价格已由一开始的1000美金，下降跌至500美元。对于有高效能应用需求的企业，或是公司内部主机CPU在1GHz以下者，最好采用iSCSI HBA卡，如此才能获得最好的性能。

NetApp专家特别强调，SCSI HBA只能走iSCSI协议，而无法透过NFS或CIFS等文件系统协议与应用服务器沟通。

**2. iSCSI TOE卡：**

亦即只有内建TOE引擎的ASIC芯片适配卡，由于SCSI指令仍以软件方式运作，所以仍会吃掉些许的CPU资源。在三种iSCSI Initiator中，价格比iSCSI HBA便宜，但比Initiator 驱动程序贵，性能也居于两者之间。目前市面上Intel的TOE HBA仍要价高达150美金。

但在各协议的支持上，TOE HBA卡可以同时支持iSCSI、NFS及CIFS协议

**3. iSCSI Initiator 驱动程序**

目前不论是Microsoft Windows、IBM AIX、HP-UX、Linux、Novell Netware等各家操作系统，皆已陆续提供这方面的服务，其中以微软最为积极，也最全面。在价格上，比起前两种方案，远为低廉，甚至完全免费(例如微软)。但由于Initiator驱动程序工作时会耗费大量的CPU使用率及系统资源，所以性能最差。

在此建议，最好是采用1GHz以上CPU的主机，如此才能获得较佳的效能表现，如果公司主机CPU在1GHz以下，那么最好不要采用。至于在各类协议的支持上，Initiator驱动程序可以同时支持iSCSI、NFS及CIFS协议。
　　
由于现阶段iSCSI的管理软件仍然不多，所以比起FC SAN，所能提供的应用及功能相对地较不完备，一旦应用及功能增加，管理性能自然大大提升。微软的存储管理平台——Windows Storage Server 2003似乎成为了众所期望的解决之道。未来，在微软提供的标准平台之下，可以包容各家不同应用功能的管理软件，如此一来，不但对iSCSI应用层面的推广有极大的帮助，同时集中化的控管、On Demand的需求调整等功能也可以有效降低管理维护成本，并促进管理效能的提升。
　　
**安全性**

在安全性方面，目前iSCSI已支持HA(High Available，高可用性)及冗余等功能，不但可以避免因为单调故障所导致的系统停机，可以在不关机、视需求(On Demand)的情况下调整指派存储空间。更重要的是，还提供不同等级的系统停机时间(Down-Time)，此即业界俗称的几个9安全标准，藉由不同等级严格要求一年停机时不超过一定时间(如一年不超过1小时，或以99.999%等数字来划分等级)，当然等级愈高，价格也愈贵。此外，在数据保护机制上，也要注意产品是否提供快照、远距备份及灾难复原等功能。

**可扩充性**

另一个要注意的重点就是，存储应用管理软件或存储配备的可扩充性，包括存储配备的容量是否可以在不关机的条件下，机动调整扩充，以及iSCSI相关硬件的扩充性，例如配备上的接口，是否支持由Giga升级到10G的预设功能。

**兼容性**

所谓兼容性，就是指现有环境是否可以与iSCSI标准及配备兼容，这可以分成现有操作系统、外围设备及网络来探讨。

首先企业必须确定现有操作系统是否支持iSCSI标准。换句话说，如果企业想利用现成的Gigabit网卡来仿真成iSCSI Initiator的话，那么必须先要确定公司采用的操作系统是否提供iSCSI Initiator驱动程序的下载服务，毕竟不是所有的操作系统都有提供这方面的服务。

如果基于性能的考虑，不想用上述的方案，而改用iSCSI适配卡也可，但是仍需确定操作系统的版本，因为仍有许多操作系统(Linux SuSE、Novell Netware)尚未支持iSCSI适配卡，所以这些都是在考虑建构iSCSI SAN时，特别要注意的地方。

如果在构建iSCSI SAN之前，公司内部已有其它SCSI存储设备、NAS或FC SAN，也必须考虑iSCSI与这些既有配备的整合，以扩充应用的层面及整体效益。就公司既有SCSI存储配备，可通过iSCSI桥接器来做整合；就NAS而言，如今市面上已有许多NAS及iSCSI的整合方案(例如NetApp)；在iSCSI与FC SAN的整合上，可以透过iSCSI网关(如Brocade或McDATA产品)来完成。

**应用及功能**

至于iSCSI SAN的应用及功能，通常要视管理软件所提供的应用功能而定。通常管理软件可分为一般存储配备所附的管理软件及架构性管理软件，前者提供较简单、阳春的存储功能；后者则能提供许多强大进阶的存储应用功能。

而微软WSS 2003所提供的存储标准平台，可以加入市面上各类型及功能的存储管理软件，提供了更丰富的远程异地备份等应用功能，不但可解决长久以来iSCSI应用缺乏的问题，更可促使管理软件价格的下降，对于整体管理效能的提升，以及成本支出的降低会有重大帮助。

就应用层面而言，业界对iSCSI最大特点的普遍看法是，十分适合于具连续性、且较大文件的高速传输及备份应用。由于iSCSI具有无限距离的传输特性，所以在远程备份上最受青睐。也因为如此，目前iSCSI最常见的应用不外乎异地备份及灾难恢复(Disaster Recovery，DR) 为主，同时iSCSI也已支持快照(SnapShot)等高阶功能，可以快速地备份或灾备，达到数据保护的目的。

建联科技认为，目前公司内部至少有三种不可或缺的服务器，那就是Web Server、Mail Server及File Server(亦即数据库)，其中，数据库及邮件最适合采用iSCSI SAN，例如NetApp即表示，由于ERP数据库系统采用块协议，所以非常适合建置在iSCSI SAN上。基于这方面的考虑，目前有许多厂商皆主张将NAS及SAN做一整合，以符合上述种种需求。

目前有许多厂商积极开发iSCSI to SATA的磁盘阵列解决方案，他们一致认为两者是低成本、高容量的最佳结合，可存储一些非立即性的数据，但在运用及时性上又远比磁带库好得多。尤其受目前存储行业甚为风行的信息生命周期管理(Information Lifecycle Management，ILM)观念的影响，iSCSI to SATA的磁盘阵列的青睐度及影响性与日俱增，甚至有侵蚀、乃至取代磁带库的声势。
