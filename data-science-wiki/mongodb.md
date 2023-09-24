
### Created by @jl33-ai 👦🏻

-------

## Table of Contents 📚

- [Introduction](#introduction)
- [Installation](#installation)
- [Basic Commands](#basic-commands)
- [Data types](#data-types)
- [CRUD Operations](#crud-operations)
- [Indexing](#indexing)
- [Aggregation](#aggregation)
- [Backup and Restore](#backup-and-restore)

-------

<a name="introduction"></a>
## Introduction 👋

- MongoDB is a **source-available** cross-platform **document-oriented database** program.
- It is classified as a **NoSQL database** program, which avoids the traditional table-based relational database structure. 
- Instead, MongoDB uses **JSON-like documents with optional schemas**.
```sh
{
  id: 100,
  username: "jl33-ai",
  email: "jl33@ai.com"
}
```

<a name="installation"></a>
## Installation 📦

You can find MongoDB installation guides for each specific operating system on the official MongoDB website under the following link: [MongoDB Installation](https://docs.mongodb.com/manual/installation/)

<a name="basic-commands"></a>
## Basic Commands 🔤

- remember that everything in MongoDB is case sensitive.

- **show dbs**: list databases.
- **use database_name**: switch to a database (if it doesn't exist, MongoDB creates one).
- **show collections**: list all collections in the current database.

<a name="data-types"></a>
## Data Types 💾

- String 
- Integer
- Boolean
- Double 
- Array 
- Object
- Null 

<a name="crud-operations"></a>
## CRUD Operations 👷

- **Create**: Use the `insertOne()` or `insertMany()` method.
```sh
db.collection.insertOne({
 name: "jl33-ai",
 age: 20,
})
```
- **Read**: Use the `find()` method.
```sh
db.collection.find()
```
- **Update**: Use the `updateOne()` or `updateMany()` method.
```sh
db.collection.updateOne({name: "jl33-ai"}, {$set: {age: 22}})
```
- **Delete**: Use the `deleteOne()` or `deleteMany()` method.
```sh
db.collection.deleteOne({name: "jl33-ai"})
```

<a name="indexing"></a>
## Indexing 📍

- Indexing in MongoDB works in the same way as indexing in other database systems. 
- MongoDB uses indexing to improve search efficiency.
```sh
db.collection.createIndex({name: 1})
```

<a name="aggregation"></a>
## Aggregation ⏳

- The aggregate function allows the users to perform calculations on the grouped data.
- The aggregate function groups the records in the mongodb collections, and then processes the data and returns the computed results.
```sh
db.collection.aggregate([{ $group : { _id : "$name", total : { $sum : 1 }}}])
```

<a name="backup-and-restore"></a>
## Backup and Restore 🛠️

### Backup
- **mongodump** is a utility for creating backups of our databases.
```sh
mongodump --db yourDB --out /data/backup/
```
### Restore
- **mongorestore** is a utility for restoring backups.
```sh
mongorestore /data/backup/yourDB/
```

---
