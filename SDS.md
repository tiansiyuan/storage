Software-defined storage (SDS) is a computer program that manages data storage resources and functionality and has no dependencies on the underlying physical storage hardware.

Purists argue that any data storage product could be described as software-defined, since all storage products require software to manage the underlying hardware and control storage-related tasks. However, the marketing term software-defined storage is most often associated with software products designed to run on commodity server hardware with Intel x86 processors and to enable cost savings over traditional storage area network (SAN) and network-attached storage (NAS) systems that tightly couple software and hardware.

Unlike monolithic SAN and NAS systems, software-defined storage products enable users to upgrade the software separately from the hardware. Common characteristics of SDS products include the ability to aggregate storage resources, scale out the system across a server cluster, manage the shared storage pool and storage services through a single administrative interface, and set policies to control storage features and functionality.

Factors contributing to the increase in SDS products include the explosive growth of unstructured data, creating a greater need for a scale-out storage architecture; the availability of high-performance server hardware with multicore processors; the general acceptance of virtualization in servers, desktops, applications and networking; and the popularity of cloud technologies.

Use cases for software-defined storage vary by product type. For instance, common use cases for scale-out object and file SDS include applications that generate significant amounts of unstructured data, such as data analytics, genomics and internet of things. Scale-out block SDS may target higher performance workloads such as databases. Many types of SDS may hold appeal for DevOps environments that require flexible storage provisioning for new applications.

Software-defined storage is part of a larger industry trend that also includes software-defined networking (SDN), software-defined infrastructure and software-defined data centers.

## Types of software-defined storage products and major vendors

Software-defined storage can be difficult to categorize due to the lack of a standard definition. Some SDS products support block, file and object storage interfaces, although they may tend to prioritize one or two interfaces. Others are accessible through one or two storage protocols. For instance, some SDS products that started as object storage have added support file protocols, and some distributed file systems support the offload of data to object storage.

Many SDS products are able to run on the server operating system (OS) and in a virtual machine (VM), whether on premises or in a public cloud. Other SDS products run only in a server hypervisor kernel or VM. Some SDS products can run in a container to conserve server resources and facilitate the consistent management of container-based applications and storage services through a single container orchestration tool.

SDS vendors generally provide lists of certified hardware options. Some software-defined storage vendors sell products that package software with standard server hardware to ease procurement and deployment for customers. Many SDS products enable users to scale compute and storage resources separately. Hyper-converged options scale storage, compute, virtualization and networking in the same physical hardware. Vendors selling hyper-converged infrastructure software packaged with standard hardware include Hewlett Packard Enterprise, Nutanix and Pivot3.

Several major storage vendors have released software versions of storage products that were previously tied to specific hardware. Examples include Dell EMC's UnityVSA from its Unity storage array and IsilonSD Edge from the Isilon scale-out NAS system; IBM Spectrum Accelerate from the vendor's XIV storage; and NetApp's OnTap Select, a software-only version of the OS that powers the company's storage arrays.

Open source software-defined storage is freely available through community development projects. Prominent examples of open source SDS include Ceph, FreeNAS, Gluster and OpenStack Swift. Commercially supported distributions of open source SDS are available from various vendors.

From: http://searchstorage.techtarget.com/definition/software-defined-storage
