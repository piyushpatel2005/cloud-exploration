# Storage Services

AWS provides various storage options like Amazon S3, Amazon EBS, Amazon EFS, Amazon FSx and Amazon FSx for Lustre. When migrating your storage from on premises to cloud, you first have to assess your existing storage solutions. Moving storage from on-premises to AWS provides following benefits.

- Increased Agility: When you're on-premises, you have to spend a considerable amount of time and resources to setup and maintain your storage solutions. It can take several weeks for approval, provisioning and configurations. On the cloud, you virtually have unlimited storage capacity when you need it. You can increase or reduce the capacity at any time.
- Security: On-premises storage and network are often not uniformly secured from external or internal access. Security concerns range from physical security to storage systems, encryption for data at rest and in transit, access control, etc. On the cloud, cloud providers are responsible for bulk of these work. You can easily set up encryption at rest and in transit.
- Cost Benefits: With cloud, you do not have to purchase hardware or spend time on maintenance. You can even scale down if you don't need those additional storage capacity. Thus, resulting in better cost savings. This also reduces capital investment. AWS billing also uses billing increments to each second of usage. So, if you're using storage for only a few hours, you don't have to pay for the entire day.

## Type of Storage

There are three primary types of storage. These are block, file and object storage.

### 1. Block Storage
Block storage is a raw storage in which the hardware storage is formatted and attached to the compute system. The storage is formatted into continuous segments on the storage device and these segments are called blocks. The storage devices can be hard disk drives (HDD) or solid state drives (SSD). This storage dveice is used by the OS or an application. AWS pprovides several options for this type of storage which includes Amazon EBS, Amazon EC2 instance store, Amazon FSx.

### 2. Object Storage
Object storage is built on the block storage. This type of storage is used for storing the data within a binary object. That's why the name object storage. An object is made up of a larger set of formatted blocks organized into a contiguous set by using a predetermined object size. Cloud object storage systems distribute the data across multiple physical devices. This is called object replication. AWS provides Amazon S3 with different storage classes to serve different use cases.

### 3. File Storage
It is also built on top of block storage and is used for file share or file servers. The primary use of this storage is to store files with directory hierarchy. The two most common storage protocols for file storage are Server Message Block (SMB) and Network File System (NFS). The operating system manages the storage protocol and the operations of the file system. The file system can be Windows Server, Linux or other operating systems. AWs provides Amazon EFS that uses NFS access protocol, FSx for Lustre, FSx for Windows, etc for file storage.

AWS also provides various services to provide hybrid cloud solutions for storage. This basically allows you to connect your on-premises storage to AWS cloud. On top of this, AWS also provides services to migrate your storage from on-premises to AWS which you can use to migrate your on-premises storage footprint to AWS cloud seamlessly.
