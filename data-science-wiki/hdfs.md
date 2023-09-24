Created by @jl33-ai 👦🏻

The Hadoop Distributed File System (HDFS) is a distributed file system designed to operate on large data sets, providing high throughput for data access. Below, we will review various aspects of HDFS.

## Table of Contents 💼
1. [Introduction](#introduction)
2. [Architecture](#architecture)
3. [Features](#features)
4. [Basic Commands](#basic-commands)
5. [Applications](#applications)
6. [Conclusion](#conclusion)

<a name="introduction"></a>
## Introduction 🚀

HDFS is part of the [Apache Hadoop](https://hadoop.apache.org/) project and facilitates storing a large amount of data in a distributed environment, allowing processing in parallel. This ensures data is reliable, even in the case of hardware failure. 

Here's a basic example to visualize HDFS 📊:
```sh
hadoop fs -ls /
```
This command will list out all the directories that are immediate children of the file system.

<a name="architecture"></a>
## Architecture 🏗

HDFS follows a master/slave architecture, including the following components:

* NameNode (Master): It manages the file system namespace and client access to files.
* DataNode (Slave): It is responsible for storing and retrieving data blocks when told to by clients or the NameNode.

<a name="features"></a>
## Features 🌟

* **Fault tolerance**: Data stored in HDFS is automatically replicated at multiple nodes, allowing the recovery of data in case of failure.   
* **Scalability**: HDFS can store extensive data sets and support thousands of nodes in a single cluster.
* **Data locality**: When it comes to big data processing tasks, HDFS moves computation to the data instead of the other way around, reducing network congestion.
* **Easy to use**: With simple file system semantics, HDFS is convenient to use.

<a name="basic-commands"></a>
## Basic Commands ✍ 

Some basic HDFS commands:

* `hadoop fs -mkdir /user/test` Creates a new directory.
* `hadoop fs -put localfile /user/test` Puts a local file into HDFS.
* `hadoop fs -cat /user/test/localfile` Prints the content of the file on stdout.
* `hadoop fs -rmr /user/test` Removes the specified directory along with its content.

<a name="applications"></a>
## Applications 👁

HDFS is used primarily with Apache Hadoop projects like MapReduce, Hive, and Pig for data analysis. It can also be used for storing data from different source systems, data processing, and data lake.

<a name="conclusion"></a>
## Conclusion 🏁

HDFS is a robust and reliable system, capable of storing immense volumes of data and handling enterprise level workloads. Mastering HDFS is pivotal to traverse in the field of big data.
