# Storage Options

All applications and services running on the cloud need one or another type of storage solution. In Google Cloud, there are various storage solution depending on the use case. You can choice for persistent disks, cloud storage which is object storage as well as databases like SQL and NoSQL databases depending on your application workloads.

## Cloud Storage

This is Google Cloud's object storage solution which is highly scalable, large capacity, highly durable. Objects can be of any type of file or binary large objects. It's not a block storage like a normal file system like a persistent disk which can be attached to VMs although cloud storage is accessible from VMs and other google cloud services. The objects in Cloud storage are organized in buckets. This storage is great for static content, backups, datalakes. It's usually treated as a single units of data, that is you cannot retrieve only part of the data.

Based on the location of the data, these can be regional, multi-regional or Dual-regional.
- Regional Storage keeps copies of objects in a single Cloud region. It copies the data across multiple zones in a single region, so this type of objects can tolerate single zone failure.
- Dual Region: The data is copied to two separate regions for better redundancy and high availability.
- Multi-Regional Storage is large geographic area whch contains two or more geographic places. It provides highest level of availability.

The cloud storage is also classified based on access and pricing. There are four storage classes for cloud storage buckets. These classes determine the cost storage and data retrieval. You can check brief overview of each class below.
- Standard: This has maximum availability with no limitations. However, this costs more. This is used for hot data or data that is frequently accessed.
- Nearline: This storage class is suitable for data which is accessed once or less than once a month. This is cost effective solution for older data which is not frequently accessed.
- Coldline: This storage class is good for data which is accessed less than once a quarter. If we access data more frequently, there is more cost associated with data retrieval and the bills may go up.
- Archive: This has the lowest storage costs in cloud storage. This is good only for storing data for compliance or legal requirements of the business. This storage class should be used for data that's accessed less than once a year.

You can set objet lifecycle policies to move objects from one storage class to another storage class automatically based on their life, specific date or number of versions. This is one of the ways to reduce cloud costs.

## Persistent Disk

This is a storage service that are attached to VMs in Compute Engine or Kubernetes Engine. It's a durable, blocks storage option in Google cloud platform. This is suitable for block storage where data can be accessed in blocks and a block can be updated or deleted efficiently. It's suitable for OS level operations like normal file system. Persistent disks can be HDDs or SSDs where SSDs provide lower latency, higher IOPs and overall faster storage system compared to HDD disks. There are four types of disks: Balanced persistent disks, Performance persistent disks, Standard persistent disks and Extreme persistent disks. Also, in terms of locations, they can be either zonal or regional disks.

## Cloud FileStore

This is Google cloud's fully managed NFS file storage which can be easily mount as shared filesystem on virtual machines. This can be attached to network and can be shared with developers. It can also provide shared file systems for compute engine and kubernetes engine. This can provide high IOPs along with variable storage capacity which is easy to upgrade.

## Databases

Google Cloud has several database options. There are choices in terms of SQL vs NoSQL databases as well as options for availability across zones or at global scale. The choice of which database option to choose depends on the application requirements.

### Cloud SQL

Cloud SQL is Google Cloud's fully managed database service which allows users to set up MySQL, PostgreSQL and Microsoft SQL Server databases on virtual machines. It's a managed service, so administration tasks are offloaded to Google Cloud platform for back up, patching and updates etc. This service is suitable for databases upto 64TB capacity and it can only scale vertically. It also provides options for replication of database to another server with automatic failover option.

### Cloud Spanner

This is yet another SQL database offering on Google cloud with very high availability. It is a globally distributed relational database with strong consistency, transactions and replication across regions in GCP. Cloud spanner also scales horizontally like NoSQL databases. It's well suited for enterprise-grade applications which require large scale, distributed relational database.

### Bigtable

Cloud Bigtable is a wide-column, petabyte-scale, fully managed scalable NoSQL database. It provides high throughput for writes and reads for large data. Bigtable is suitable for low-latency applications which require high read and write throughputs. Bigtable also provides support for HBase API, thus it's a natural choice for migrating on-premise HBase applications to Google Cloud. It also provides support for cluster resizing without down time.

### Datastore

Cloud Datastore is a highly scalable, managed, serverless NoSQL database from GCP. It's useful for mobile, IoT and web application use cases. Firestore is considered next generation of Datastore.

### FireStore

This is NoSQL, serverless, real-time database from Google Cloud. The data is stored as key-value pairs. It supports JSON structure data with ACID transactions, indexes like relational databases but also provides flexibility in schema of the data you want to store. This is optimized for offline use as well as supports live synchronization. So, it's ideal for mobile backends, IoT, real-time tracking, product catalogs, user profiles, etc. It also supports automatic multi-region replication with strong consistency and high durability.

Firestore supports Datastore mode which is for backward compatibility with Cloud Datastore and Native mode which is good for mobile and web client libraries with real-time and offline features.

### Memory Store

Cloud Memorystore is highly available in-memory cache service offering which supports Redis and Memcached caching. Caches are used to reduce the latency to read data into an application. This also helps reduce reads from backend database systems. Memorystore is a managed service ensuring high availability, patching and automaticc failover so users don't have to manage these administrative tasks.
