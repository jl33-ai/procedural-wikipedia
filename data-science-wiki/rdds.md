>Created by @jl33-ai 👦🏻
***
#Table of Contents
- [Introduction](#introduction)
- [Creating RDDs](#creating-rdds)
- [Transformation and Actions](#transform-actions)
- [Caching](#caching)
- [Handling Faults](#handling-faults)
- [Examples](#examples)

#Introduction <a name='introduction'></a>
Resilient Distributed Datasets (RDDs) 📚 are a fundamental data structure in Spark. They are an immutable distributed collection of objects. Each dataset in RDD is divided into logical partitions, which may be computed on different nodes of the cluster.

Key Features of RDDs:
- Distributed Collection: Data resides at multiple nodes in a cluster.
- Resilience: Ability to withstand failures.
- Immutability: Once created, the data cannot be changed.
- Lazy Evaluations: Tasks are not executed immediately upon command.

#Creating RDDs <a name='creating-rdds'></a>
There are two ways to create RDDs in Spark.

1. Parallelizing already existing collection in driver program.
```
    val data = Array(1, 2, 3, 4, 5)
    val distData = sc.parallelize(data)
```
2. Referencing a dataset in an external storage system (like HDFS, HBase, shared file system).
```
    val distFile = sc.textFile("data.txt")
```

#Transformation and Actions <a name='transform-actions'></a>
RDDs support two types of operations, transformations which create a new dataset from an existing one and actions which return a value after running a computation on the dataset.

Transformations include `map`, `filter`, `union`, and `distinct`.  Actions include `reduce`, `collect`, `first`, and `take`.

#Caching <a name='caching'></a>

Spark keeps your data in memory by default. However, you can control their storage using `persist()` or `unpersist()`. Caching can significantly improve the performance of your Spark jobs by keeping the frequently accessed data in memory.

```
    val cacheRDD = sc.parallelize(Array(1, 2, 3, 4, 5)).cache()
```

#Handling Faults <a name='handling-faults'></a>
RDDs are characterized by their ability to recover automatically. This makes it a handy tool for iterative and interactive applications. When a partition of a dataset is lost, the RDD rebuilds that specific partition so that the computations can go along smoothly.

#Examples <a name='examples'></a>
Let's walk through a simple word count example:
```
    val textFile = sc.textFile("hdfs://...")
    val counts = textFile.flatMap(line => line.split(" "))
                 .map(word => (word, 1))
                 .reduceByKey(_ + _)
    counts.saveAsTextFile("hdfs://...")
```