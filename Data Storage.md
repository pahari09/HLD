storage type:
------------
block vs file vs object
Concept: https://www.youtube.com/watch?v=0NM1OmGQhWQ&ab_channel=AnalogiesCloud

*file storage
-------------
Concepts:
https://www.ibm.com/topics/file-storage

File storage—also called file-level or file-based storage—is a hierarchical storage methodology used to organize and store data on a computer hard drive or on network-attached storage (NAS) device. In file storage, data is stored in files, the files are organized in folders, and the folders are organized under a hierarchy of directories and subdirectories. To locate a file, all you or your computer system need is the path—from directory to subdirectory to folder to file.

Hierarchical file storage works well with easily organized amounts of structured data. But, as the number of files grows, the file retrieval process can become cumbersome and time-consuming. Scaling requires adding more hardware devices or continually replacing these with higher-capacity devices, both of which can get expensive.


Note: for windows we will use SMB protcol and for Linux we will use NFS based protocol.

=use-case:
File storage is a good solution for a wide variety of data needs, including the following:

Local file sharing: If your data storage needs are generally consistent and straightforward, such as storing and sharing files with team members in the office, consider the simplicity of file-level storage.

Centralized file collaboration: If you upload, store, and share files in a centralized library—located on-site, off-site, or in the cloud—you can easily collaborate on files with internal and external users or with invited guests outside of your network.

Archiving/storage: You can cost-effectively archive files on NAS devices in a small data center environment or subscribe to a cloud-based file storage service to store and archive your data.

Backup/disaster recovery: You can store backups securely on separate, LAN-connected storage devices. Or you can subscribe to a cloud-based file storage service to replicate your data files across multiple, geographically-dispersed data centers and gain the additional data protection of distance and redundancy.
------------------------------------------------------------------------------------------------------------------------
*block storage
---------------
Concepts:
https://www.purestorage.com/knowledge/what-is-block-storage.html#:~:text=Block%20storage%20is%20a%20type,that%20is%20stored%20in%20blocks.

Block storage is a type of data storage that uses raw storage volumes called “blocks” to store data. Commonly used in SAN, iSCSI, and local disk environments, each of these blocks can function as a stand-alone hard drive.

A block file is a type of file that is stored in blocks. Companies usually use block files when they require speedy, accurate, and efficient data transfer, such as when retrieving information from a database. Operating systems such as Linux and Windows can access the blocks via Fibre Channel over Ethernet (FCoE), Fibre Channel, or iSCSI protocols.

How Does Block Storage Work?
With block storage, each block contains a specific amount of data, typically 256KB to 4MB. Each block represents a portion of a file that isn’t organized in any specific hierarchical order. In fact, the data on blocks sitting beside neighboring blocks may be completely unrelated to each other.

Each block has its own unique identifier to differentiate it from other blocks. When a file needs to be retrieved, an application will send a request, and the blocks will be located and assembled.

Besides the identifier, the blocks don’t contain any metadata. Because of the lack of metadata, block storage is very efficient since almost all the block’s storage capacity stores the actual data. There’s no wasted space. This makes block storage ideal for workloads that require rapid scale-up and fast read/write performance.
------------------------------------------------------------------------------------------------------------------------

*object storage
---------------
//Concepts:
https://www.ibm.com/topics/object-storage\

Object storage, often referred to as object-based storage, is a data storage architecture for handling large amounts of unstructured data. This is data that does not conform to, or cannot be organized easily into, a traditional relational database with rows and columns. Today’s Internet communications data is largely unstructured. This includes email, videos, photos, web pages, audio files, sensor data, and other types of media and web content (textual or non-textual). This content streams continuously from social media, search engines, mobile, and “smart” devices.

How it works?
Objects are discrete units of data that are stored in a structurally flat data environment. There are no folders, directories, or complex hierarchies as in a file-based system. Each object is a simple, self-contained repository that includes the data, metadata (descriptive information associated with an object), and a unique identifying ID number (instead of a file name and file path). This information enables an application to locate and access the object. You can aggregate object storage devices into larger storage pools and distribute these storage pools across locations. This allows for unlimited scale, as well as improved data resiliency and disaster recovery.

Object storage removes the complexity and scalability challenges of a hierarchical file system with folders and directories. Objects can be stored locally, but most often reside on cloud servers, with accessibility from anywhere in the world.

Objects (data) in an object-storage system are accessed via Application Programming Interfaces (APIs). The native API for object storage is an HTTP-based RESTful API (also known as a RESTful Web service). These APIs query an object’s metadata to locate the desired object (data) via the Internet from anywhere, on any device. RESTful APIs use HTTP commands like “PUT” or “POST” to upload an object, “GET” to retrieve an object, and “DELETE” to remove it. (HTTP stands for Hypertext Transfer Protocol and is the set of rules for transferring text, graphic images, sound, video, and other multimedia files on the Internet).

You can store any number of static files on an object storage instance to be called by an API. Additional RESTful API standards are emerging that go beyond creating, retrieving, updating, and deleting objects. These allow applications to manage the object storage, its containers, accounts, multi-tenancy, security, billing, and more.

For example, suppose you want to store all the books in a very large library system on a single platform. You will need to store the contents of the books (data), but also the associated information like the author, publication date, publisher, subject, copyrights, and other details (metadata). You could store all of this data and metadata in a relational database, organized in folders under a hierarchy of directories and subdirectories.

But with millions of books, the search and retrieval process will become cumbersome and time-consuming. An object storage system works well here since the data is static or fixed. In this example, the contents of the book will not change. The objects (data, metadata, and ID) are stored as “packages” in a flat structure and easily located and retrieved with a single API call. Further, as the number of books continues to grow, you can aggregate storage devices into larger storage pools, and distribute these storage pools for unlimited scale.
-----------------------------------------------------------------------------------------------------------------------
*RAID

Concepts:
https://www.youtube.com/watch?v=-6sA9nHlZDc&t=868s&ab_channel=GateSmashers

Article for concepts:
https://cloud.ibm.com/docs/bare-metal?topic=bare-metal-bm-raid-levels

RAID (Redundant Array of Independent Disks) creates a single usable data disk, where several physical disks are combined into an array for better speed and fault tolerance. Following are the three key concepts in RAID:

Mirroring: copying data to more than one disk
Striping: splitting data across more than one disk
Error correction (fault tolerance): redundant data is stored to allow problems to be detected and possibly fixed.

------------------------------------------------------------------------------------------------------------------------

Architecture
*DAS: 
.Direct attach storage
.DAS is a connection between storage and a server without a storage network device.
.Block storage
.Storage is managed or accessed by a single host at any given time.
.Fast data transfer
.eg hard disk

*SAN
Concepts:
https://www.purestorage.com/uk/knowledge/what-is-storage-area-network.html

.storage area network
.A storage area network (SAN) is a dedicated network of storage devices used to provide a pool of shared storage that multiple computers and servers can access. Storing data in centralized shared storage architecture like SANs allows organisations to manage storage from a collective place and apply consistent policies for security, data protection, and disaster recovery.
.it is  a high speed network that provides multiple server access to consolidated pools of shared , block level storage.
.it consist of host ,switches, storage elements and storage devices that are interconnected using a variety of technologies,topology and protocols
.it represents a storage device to a host such that the storage appear to be a locally attached.
.Improve application availability, enhance application performance and it support heavy read/write.

*NAS
Concept:
https://www.purestorage.com/knowledge/what-is-nas.html

.Networked Attached Storage (NAS) is a dedicated file storage system that allows multiple users and devices on the local area network (LAN) to access data from a centralized storage area on the network. Users can access NAS using a standard ethernet connection via a router or a network switch.
.NAS is an easy-to-use storage system with high storage capacity and low costs. Network-attached storage systems are flexible and scalable, allowing you to add additional storage when necessary.
.It is a storage device that connects to a network and provide file access service to a computer systems in LAN(TCP/IP)
.these devices generally consist of an engine that implements the file services and or more devices, on which data is stored
.NAS uses file access protocol such as NFS(Linux based) or SMB(Windows)
.Simplified solution 



}

Specialised Storage Paradigms{

special types of storage:
//https://www.youtube.com/watch?v=ftEWQPDlTDA&ab_channel=ByteMonk

*BLOB
------
.Blob means binary large object. It’s a collection of raw binary data. Therefore, it consists of zeros and ones.
While blobs could be structured or semi-structured data, they are often large unstructured data. Examples of blobs include media files such as audio and video files, PDFs, log files, emails, images, etc.
.Eg : Amazon S3, Google cloud storage
Article for concepts:
https://www.baeldung.com/cs/blob-storage
----------------------------------------------------------------------------------------------------------------------

*HDFS 
-----
Concepts:
https://www.youtube.com/watch?v=VavRifvVwIo&ab_channel=GateSmashers
s3(Blob) vs HDFS 
https://www.youtube.com/watch?v=rqCJjanWMQ4&ab_channel=MelvinL
eg Amazon EBS
It provides one of the most reliable filesystems. HDFS (Hadoop Distributed File System) is a unique design that provides storage for extremely large files with streaming data access pattern and it runs on commodity hardware. Let’s elaborate the terms:  
Extremely large files: Here we are talking about the data in range of petabytes(1000 TB).
Streaming Data Access Pattern: HDFS is designed on principle of write-once and read-many-times. Once data is written large portions of dataset can be processed any number times.
Commodity hardware: Hardware that is inexpensive and easily available in the market. This is one of feature which specially distinguishes HDFS from other file system.

Nodes: Master-slave nodes typically forms the HDFS cluster. 

Two main components:
NameNode(MasterNode):
.It record the metadata of all the file store in the cluster. eg The location of blocks stored,the size of files,permission hierarchy etc. These are the two files associated with the metadata:
.FsImage: It contains the complete state of the file system name space Since the start of the nameNode
.EditLogs: It contains all the recent modification made to the file system with respect to the most recent fsImgae.
.It regularly receives the heartbeat and a block report from all the datanode in the cluster to ensure that the datanodes are live.

DataNode(slave):
.The actual data is stored in dataNode.
.The dataNode perform the low-level read and write request from the file system client.

----------------------------------------------------------------------------------------------------------------------
*time series - influxDB (use to store data related to timestamp. Eg crypto currency data)
*RDBMS - see above sql vs Nosql
*NO-Sql DB - see above sql vs Nosql

*Graph-DB - neo4j
-----------------
Concepts:
https://www.youtube.com/watch?v=3C48rm9H4DI&ab_channel=TechPrimers
Practical of GraphDB
https://www.youtube.com/watch?v=NvjKXwt7n48&ab_channel=CodeWithHarry

.A graph database (GDB) is a database that uses graph structures to store data. 
 It uses nodes, edges, and properties instead of tables or documents. The edges represent relationships between the nodes. This helps in retrieving data more easily

When do we need Graph Database?
.It solves Many-To-Many relationship problems
.When relationships between data elements are more important
.Low latency with large scale data
