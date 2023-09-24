# Apache Cassandra Tutorial 🚀 

_Created by @jl33-ai 👦🏻_ 

## Contents 📇
1. [Introduction](#introduction-🎉)
2. [Installation](#installation-⚙️)
3. [Main Concepts](#main-concepts-🧠)
4. [Data Modeling](#data-modeling-🏗️)
5. [CQL](#cql-🗣️)
6. [Examples](#examples-🔍)
7. [Best Practices](#best-practices-🎯)

---

### Introduction 🎉
Apache Cassandra is a highly-scalable, free and open-source NoSQL database designed to handle large amounts of data across many commodity servers, providing high availability with no single point of failure. 

### Installation ⚙️
The simplest way to install Cassandra is to use the binary tarball files available at the Apache Cassandra Download page. For complete instructions, refer to the Cassandra documentation for your specific Operating System.

### Main Concepts 🧠

- **Keyspace** – This is the outermost container for data in Cassandra. Similar to a database in relational databases.
- **Column Family (Table)** – This is a tuple `(name,value,timestamp)` consisting of a name, value and timestamp. Similar to a table in RDBMS.
- **Row** - Collection of column families identified by a key.
- **Column** - A data element having two parts, name and value.

### Data Modeling 🏗️
In Cassandra, data modeling involves the design of tables and keys. The core steps for data modeling in Cassandra are:

- Designing column families.
- Defining keys and index.
- Modeling data to your application requirements.

### CQL (Cassandra Query Language) 🗣️
The Cassandra Query Language (CQL) is a close relative of SQL. It allows you to interact with Cassandra through your terminal. For example:

```cql
CREATE KEYSPACE tutorialspoint
WITH replication = {'class':'SimpleStrategy', 'replication_factor' : 3};
```

### Examples 🔍

Creating a keyspace in Cassandra:

```cql
CREATE KEYSPACE IF NOT EXISTS sample_keyspace 
WITH REPLICATION = { 'class' : 'SimpleStrategy', 'replication_factor' : 3 };
```

Creating a table:

```cql
CREATE TABLE IF NOT EXISTS sample_keyspace.sample_table (
sample_field1 text PRIMARY KEY,
sample_field2 text,
sample_field3 text
);
```

### Best Practices 🎯
- Always insert/update rows using a consistency level of `Quorum`.
- Don't excessively denormalize your data.
- Use composite keys for multiple queries on tables.

---
```
