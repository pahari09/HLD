=================================================================================================================
Video: 

Concepts:

DataBase basics
https://www.youtube.com/watch?v=r9HyjDALRQE&list=PLrk5tgtnMN6RvXrfflstJWgcPFQ_vTOV9&index=9&ab_channel=CodingNinjas

NoSql with respect to system design:
https://www.youtube.com/watch?v=GGIsONA1Kog&list=PLrk5tgtnMN6RvXrfflstJWgcPFQ_vTOV9&index=13&ab_channel=CodingNinjas
https://www.youtube.com/watch?v=O_c7lzNbcKo&list=PLTCrU9sGyburBw9wNOHebv9SjlE4Elv5a&index=7&ab_channel=sudoCODE


What is a NoSQL in general well explained with example:
https://www.youtube.com/watch?v=B3gJT3t8g4Q&ab_channel=ITkFunde
======================================================================================================================
Article to Read:

A Quick Overview of Different Types of Databases
https://www.astera.com/type/blog/a-quick-overview-of-different-types-of-databases/

Different Types of Databases
https://www.bitdegree.org/tutorials/types-of-databases/

ACID vs BASE

ACID => https://geeksforgeeks.org/acid-model-vs-base-model-for-database/
BASE => https://phoenixnap.com/kb/acid-vs-base
========================================================================================================================
SQL : Structure query language. structure set of data. 

Advantage of sql:

*Managing large data
*consistency
*ACID compliant
*well structured schema
*reduced chances of error

Disadvantage of sql:
* Not able to horizontally scale it
*data need to abide schema. If we want to add a coloumn to the existing schema . Its a bit costly.

when to use sql?
*Strict schema structure
*Data needs to be accurate
*Many to Many relationship

ACID for SQL:

A= Atomicity . Single amount of work.
C=Consistency. Data should be consistent. Multiple read to same row should be same.
I=Isolation . One transaction should be isolated from other.
D=Durability. Should be presisted on disk.
 

SQL db currently available?
PostGres, Mysql
=======================================================================================================================

NOSql:
Non Relational Database => Store data in document, key-value or in different representation but not in rows or coloumn.

BASE for NoSQL

*Basically Available – Rather than enforcing immediate consistency, BASE-modelled NoSQL databases will ensure availability of data by spreading and replicating it across the nodes of the database cluster.
*Soft State – Due to the lack of immediate consistency, data values may change over time. The BASE model breaks off with the concept of a database which enforces its own consistency, delegating that responsibility to developers.
*Eventually Consistent – The fact that BASE does not enforce immediate consistency does not mean that it never achieves it. However, until it does, data reads are still possible (even though they might not reflect the reality).

Advantage:
*Schema Free
*Not to complex to handle 
*Scalable
*Highly Available(horizontally scaling)
*schema is easily changeable

Disadvantage:
*Not relying data
*relationship between object is bit difficult
*not built for update
*Not ACID compliant
*Read times are bit slower

when to use?

========================================================================================================================
Categories of Nosql:


1> Key value based: 
eg 
Redis

Concepts of Redis:
https://www.youtube.com/watch?v=OqCK95AS-YE&ab_channel=TechWorldwithNana

Practical of Redis:
https://www.youtube.com/watch?v=OqCK95AS-YE&ab_channel=TechWorldwithNana


2>Wide column based:
Cassandra DB

Concepts of Cassandra
https://www.youtube.com/watch?v=KZsVSfQVU4I&list=PL8hP5HjAnJ38Kh_tx_dazYue1xK97rSej&ab_channel=CodewithIrtiza

Practical of Cassandra (see the video in the same sequence as listed below)
https://www.youtube.com/watch?v=VsQ4OuH-K1I&ab_channel=Telusko
https://www.youtube.com/watch?v=HTuSgkDlbSA&list=PLsyeobzWxl7r0bn6dzVA8bQNxcx7DRl5F&index=3&ab_channel=Telusko
https://www.youtube.com/watch?v=Y-vY49lDeKY&list=PLsyeobzWxl7r0bn6dzVA8bQNxcx7DRl5F&index=5&ab_channel=Telusko

3>Document based:
MongoDB
Concept for MongoDB: 
https://www.youtube.com/watch?v=a8Ojk6Fnt6I&ab_channel=ITkFunde

Practical of MongoDB
https://www.youtube.com/watch?v=ofme2o29ngU&ab_channel=WebDevSimplified

4>Search Engine:
elastic search

Concept of Elastic search:
https://www.youtube.com/watch?v=Hqn5p67uev4&ab_channel=CodingExplained

Practical of Elastic(see the video in the same sequence as listed below)
https://www.youtube.com/watch?v=bcsII2dGnDU&list=PLA3GkZPtsafYd5m2BXmkL9pjsBKy0FQ2X&ab_channel=EngineeringDigest
https://www.youtube.com/watch?v=Bdt8M_RwHVs&ab_channel=EngineeringDigest
https://www.youtube.com/watch?v=6Sz5rtL1oOk&list=PLA3GkZPtsafYd5m2BXmkL9pjsBKy0FQ2X&index=6&ab_channel=EngineeringDigest

