# The Comprehensive Guide to Hadoop 📘✨

*Created by @jl33-ai 👦🏻*

-----

![Hadoop Logo](https://hadoop.apache.org/images/hadoop-logo.jpg)

Hadoop is an open-source platform that provides excellent data management provisioning. It is a framework that allows for the distributed processing of large data sets across clusters of computers using simple programming models. 

_Have a wander through the world of Hadoop and explore! 😉_

## Table of Contents   
1. [Introduction to Hadoop 🚀](#introduction) 
2. [Key Features 🧐](#key-features) 
3. [Hadoop Ecosystem 🦀](#hadoop-ecosystem) 
4. [Hadoop Architecture ⛩](#hadoop-architecture) 
5. [Install Hadoop 🗂](#install-hadoop) 
6. [Running a Simple Hadoop Program 💻](#running-program) 

-----

<a name="introduction"></a>

## Introduction to Hadoop 🚀

Hadoop is a highly scalable storage platform, because it can store and distribute very large data sets across hundreds of inexpensive servers that operate in parallel. It provides a cost-effective storage solution for large data volumes.

:bulb: Unlike traditional relational databases, Hadoop enables multiple types of analytic workloads to run on the same data, at the same time.

-----

<a name="key-features"></a>

## Key Features 🧐

- **Storage and Processing**: Hadoop provides a distributed filesystem (HDFS) that can store data across thousands of servers, and a means of running workloads (MapReduce) across those machines.

- **High Degree of Flexibility**: Unlike traditional relational databases, you aren’t forced to preprocess data before storing it.

- **Fault Tolerant**: Data is protected against hardware failure. If a node goes down, jobs are automatically redirected to other nodes to ensure the distributed computing does not fail.

- **Open Source**: The open-source framework is free and uses commodity hardware to store large quantities of data.

-----

<a name="hadoop-ecosystem"></a>

## Hadoop Ecosystem 🦀

The Hadoop ecosystem includes related software and utilities, including Apache Hive, Apache HBase, Spark, Kafka, and many others.

- **Hadoop Common**: Contains libraries and utilities needed by other modules

- **Hadoop Distributed File System (HDFS)**: Permits high-speed data access

- **Hadoop YARN**: Manages resources of the systems storing the data and running the analysis

- **Hadoop MapReduce**: A YARN-based model for parallel processing

-----

<a name="hadoop-architecture"></a>

## Hadoop Architecture ⛩

Hadoop MapReduce is a software framework for easily writing applications which process vast amounts of data (multi-terabyte data-sets) in-parallel across large clusters (nodes) of commodity hardware in a reliable, fault-tolerant manner. 

The framework includes:
- JobTracker: each Hadoop cluster has a single JobTracker which arranges and allocates tasks to the nodes.
- TaskTrackers: each node has a TaskTracker which reports the progress back to the JobTracker.

-----

<a name="install-hadoop"></a>

## Install Hadoop 🗂

### _Step 1_: Prerequisites
- Java 1.7 or later
- SSH 

### _Step 2_: Download Hadoop 
```sh
wget https://archive.apache.org/dist/hadoop/common/hadoop-2.8.5/hadoop-2.8.5.tar.gz
```

### _Step 3_: Install Hadoop
```sh
tar -xvf /path/to/hadoop-2.8.5.tar.gz
```

-----

<a name="running-program"></a>

## Running a Simple Hadoop Program 💻

Here is an example of how to run a simple Hadoop MapReduce program.

```sh
cd /usr/local/hadoop
bin/hadoop jar share/hadoop/mapreduce/hadoop-mapreduce-examples-2.8.0.jar grep input output 'dfs[a-z.]+'
```

:clap: Congratulations! You have deployed your first Hadoop MapReduce program!

Happy Hadooping! 👨‍💻 👩‍💻