---
author: Albert Dávid
neptun code: H1B5EF
date: 2023.05.13.
lecture: 9
---

# Elmélet

## Motivation
- Big Data:
  - How to store any dart as is
  - How to run any query (analytics)
- NoSQL:
  - How to store data so that some queries are fast
  - Limited ad-hoc queries

- Realtime queries:
  - Execute time: milliseconds, seconds
- Non-realtime queries:
  - Execute time: minutes, hours, days


Definition of Big Data: </br>
There is no exact definition of Big Data. <br/>
It deals wit data sets that are too large or complex to be dealt with by traditional data-processing application software. <br/>

Big Data is not about size. <br/>
- Volume:
  - Size of data
- Velocity:
  - Speed of data creation, storage, processing, analysis and visualization
- Variety:
  - Data comes in different formats (90% of the data is unstructured)

</br>

Example: Self driving cars. <br/>
They have all kind of sensors. <br/>
They collect data about the environment. <br/>
This data needs to be processed in real time. <br/>
The data is unstructured. <br/>
</br>
It needs to be collected, stored, processed, analyzed, understanding and visualized. <br/>

</br>

Moving data to processing unit (Traditional approach) or Moving processing unit to the data (Map reduce approach) </br>

</br>

e.g. National election: </br>
Traditional approach: </br>
- Collecting the data from the voting stations
- Moving the data to the algorithm
- National office counts the votes

Distribution approach: </br>
- Collecting the data from the voting stations
- Move the algorithm to the data
- Local offices process their data (map)
- National office summarizes the data (reduce)


## Hadoop
An open source framework for storing and processing big data in a distributed fashion on large clusters of commodity hardware. </br>
- distributed file system (HDFS)
- distributed processing (MapReduce)
- very large data sets
- on computer clusters built from commodity hardware
- optimized for large files

</br>

Distributed computing: </br>
YARN: Yet Another Resource Negotiator </br>
A framework for job scheduling and cluster resource management. </br>
- Resource manager:
  - Maintains a process overview of all the nodes in the cluster
  - Designates a resource manager for each application
  - Scheduling workloads
- Node manager:
  - Tracks resource usage on each node
  - Acts as a slave to the resource manager

</br>

Programming framework: </br>
MapReduce: </br>
A YARN-based system for parallel processing of large data sets. </br>
- Map:
  - Breaks down a query into subqueries
  - Distributes the subqueries to the nodes
  - Each node processes its subquery
- Reduce:
  - Combines the results of the subqueries
  - Returns the result to the client

</br>

Hadoop components: </br>
- HDFS:
  - Hadoop Distributed File System
  - Stores data in a distributed fashion
  - Replicates data across multiple nodes

</br>

HIVE: </br>
SQL interface to Hadoop </br>
Data warehouse software for: </br>
- reading, writing, managing large data sets
- residing in distributed storage
- using SQL syntax

Architecture: </br>
- Hive Metastore:
  - Stores metadata about Hive tables
  - Stores metadata about partitions
  - Stores metadata about columns
- Hive Server:
  - Receives queries from clients
  - Translates queries into MapReduce jobs
  - Sends jobs to Hadoop cluster

Features: </br>
- Supports:
- A large subset of SQL
- Complex data types (arrays, structs, maps)
- Views
- Indexing
- Partitioning
- Bucketing
- User-defined functions
- Sampling
- Explain
- Optimization hints

</br>

- NOT a relational database
- NOT designed for OLTP
- (on-line transaction processing)
- NOT real-time



## Spark
Lightning-fast unified analytics engine for large-scale data processing. </br>
- Analytics engine for large-scale data processing
  - Distributed computing
  - Not a data store - but can integrate with them
  - Not for OLTP
- Lightning-fast:
  - Distributed
  - In-memory
  - On iterative processing
  - High-level optimizations

</br>

Easy to use
- High level operations
- Supports:
  - several programming languages (Java, Scala, Python, R, SQL)
  - Many data stores (HDFS, Hive, HBase, Cassandra, ...)
- Interactive shell
