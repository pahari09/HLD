Concepts 
v1: https://www.youtube.com/watch?v=pSoKUfLTe8Y&list=PLTCrU9sGyburBw9wNOHebv9SjlE4Elv5a&index=19&ab_channel=sudoCODE 
v2: https://www.youtube.com/watch?v=kwCFHLbIhak&list=PLTCrU9sGyburBw9wNOHebv9SjlE4Elv5a&index=22&ab_channel=sudoCODE

Article to read: https://medium.com/nerd-for-tech/cap-theorem-with-focus-on-partition-tolerance-1af4403cb35a
                 https://www.enjoyalgorithms.com/blog/cap-theorem-in-system-design/
Definition:
-----------
CAP theorem also known as Brewer’s theorem is a concept used for distributed systems. It says that any distributed system provides only 2 guarantees out of the three (C, A & P) . This theorem is used by System Designers to choose the best architecture when designing distributed systems.
A distributed system is a system with multiple components located on different machines that communicate and coordinate actions in order to appear as a single logical system to the end-user.

Consistency
-----------
Every read receives the most recent write. If there are multiple parallel writes and reads in the system, every read will always return the correct write or the last write done on the system.
So if there are 2 nodes which are being used for read, then both the nodes should be consistent with each other so that the correct value is fetched.

Availability
------------
Availability in a distributed system ensures that the system remains operational 100% of the time. Every request gets a response(non error) regardless of the individual state of the node. This does not guarantee that the response contains the most recent write(Consistency).

Partition Tolerance
-------------------
Partition Tolerance means that as a system your entire application should always work. There could be two nodes in the system losing connection between them. However the nodes will function normally for other tasks; just that the two nodes themselves will not be able to communicate to each other.

Example
-------
The examples are based on Master-Master and Master-Slave architecture. So please read this:

DB Master Master architecture :
-----------------------------
In master-master architecture we can have multiple masters across regions. As we have multiple masters, so the read and write operation can both be done in any of the master nodes.

DB Master Slave architecture :
-----------------------------
In Master Slave architecture, we have only 1 master and all the other nodes are slave. So we choose the master node for all write operations, and the other slave nodes are means to serve the purpose of read operations. It’s the responsibility of master node to notify all slaves of the write operations.

Now to understand Partition Tolerance, we will take the above concepts of master-master and master-slave as examples.

Master-Master
-------------
Say that we have 2 nodes in total. Both are masters. The application is making a read & write operation in both the nodes. Assume, there are other applications using these nodes just for read purposes. Let’s name the nodes as A and B. If the application makes a write operation in A, it is A’s responsibility to notify B about the write operation; and vice versa. What if there’s an issue in connectivity of A and B. The A and B nodes work fine , just that they are not able to communicate in between them. This is what Fault tolerance is. Node A and B will not be able to notify each other about the write operations.

In this case, we can either choose Availability or we can choose Consistency.

Availability — If we let both A and B work, there cannot be consistency as A and B would not know about the changes that are being made to the respective nodes, as there’s no connection between them. However, the nodes A and B will be available. We have availability, not consistency.

Consistency — If we remove one of the master node say A; then the system will be consistent as there’s no need of communication about writes as only a single node is present. However we are compromising on Availability, as only a single node is available now. Hence we have Consistency, but not availability

Master-Slave
------------
This should be clear based on the above explanation.
In this case if we lose a connection between a master and a slave. The slave will never know about the write operations performed on master. Right ? So if we remove the node from the system, then we have consistency but not availability. And if we let the slave node be available despite of the connection not present between the node and master; then we have the availability but not consistency.
