# HBASE

Created by @jl33-ai 👦🏻

## Table of Contents:

- [1. Introduction](#1-introduction-)
- [2. Installation](#2-installation-)
- [3. Core Concepts](#3-core-concepts-)
- [4. HBase Shell](#4-hbase-shell-)
- [5. HBase Operations](#5-hbase-operations-)
- [6. HBase versus Traditional RDBMS](#6-hbase-versus-traditional-rdbms-)

## 1. Introduction 🚀

HBase is a column-oriented database management system that runs on top of Hadoop Distributed File System (HDFS). It is designed for wide-table, sparse data sets, and is used to host very large tables with billions of rows and millions of columns.

## 2. Installation 💻

HBase can be installed in standalone mode, pseudo-distributed mode, or fully distributed mode. 

Please download the latest version of HBase from the [Apache HBase Official Website](http://hbase.apache.org/).

## 3. Core Concepts 💡

1. **Table**
   An HBase table is a NxN table containing row key, column key, and a cell. 

2. **Row**
   In HBase, a row is the smallest unit of a table that contains data (like Key/ Value pairs).

3. **Column**
   HBase organizes data into columns where each column corresponds to a certain type, source, or category of data.

4. **Column Family**
   Column families are key design decisions when designing an HBase schema. Each column family can be stored together and tuned separately according to use cases.

5. **Cell**
   A cell is a unique combination of row key, column key, and version key in HBase table.

## 4. HBase Shell 🐚

HBase shell is a ruby-based API for managing HBase. 

Here are a few basic commands:

```
# Create a new table 
create 'tablename', 'columnfamily'

# List all tables
list

# Enable a table
enable 'tablename'

# Disable a table
disable 'tablename'

# Describe table structure
describe 'tablename'
```

## 5. HBase Operations 💼

You can perform operations like insert, update, delete on tables in HBase. Here is one example:

```hbase
# Put operation to insert data into HBase table. 
put 'table1', 'row1', 'cf:c1', 'val1'

# Get operation to retrieve a row from table. 
get 'table1', 'row1'
```

## 6. HBase versus Traditional RDBMS 💥

- **Scalability**: Unlike traditional RDBMS which does not scale out linearly, HBase can be linearly scaled. 
- **Performance**: For random read/write access, HBase performs much better than traditional RDBMS. 
- **Flexibility**: HBase schemas are more flexible and changes do not require downtime. 
- **Transactions**: Traditional RDBMS supports ACID transactions, while HBase does not.

## Conclusion 🏁

HBase provides a robust and high-performance environment for real-time read/write access to big data. It's a cornerstone technology for anyone working in the big data space. 