# Apache Storm

> **Created by @jl33-ai 👦🏻**

---

## Introduction 📖

Apache Storm is a distributed real-time computation system, similar to Hadoop but optimized for real-time operations. Apache Storm does for real-time processing what Hadoop does for batch processing. 

---

## Table of Contents 📍

- [Components of Apache Storm](#components-of-apache-storm-)
- [Installation and Setup of Apache Storm](#installation-and-setup-of-apache-storm)
- [Creating Topologies in Apache Storm](#creating-topologies-in-apache-storm-🔨)
- [Examples of Apache Storm Applications](#examples-of-apache-storm-applications-example)

---

## Components of Apache Storm ⚙️

### Nimbus

- Nimbus is the central piece of the Apache Storm system and serves as the master node that distributes code across worker nodes.
- It determines how to distribute data and assignments across worker nodes and also monitors their performance and failures.

### Supervisor

- Supervisor nodes are the worker nodes responsible for executing tasks as delegated by the Nimbus.

### Topologies
 
- Unlike in Hadoop where work is characterized by jobs, in Storm, work is encapsulated by 'topologies'. 

### Streams 

- The input data flow are called `streams`, and processes which receive the stream to output more streams are called `spouts` and `bolts`.

---

## Installation and Setup of Apache Storm ⚙️📥

To install Apache Storm, JAVA and Python needs to be installed and PATH setup needs to be done.

**Step 1**: First, download the required Storm version from the Apache website. 

```bash
wget -c http://www.apache.org/dist/storm/apache-storm-1.2.3/apache-storm-1.2.3.tar.gz -P ~/Downloads
```

**Step 2**: Extract the tar file to your preferred location.

```bash
tar -xvf ~/Downloads/apache-storm-1.2.3.tar.gz -C /usr/local/storm
```

**Step 3**: Setup PATH by adding following lines in `~/.bashrc` file.

```bash
export STORM_HOME=/usr/local/storm/apache-storm-1.2.3 
export PATH=$PATH:$STORM_HOME/bin
```

---

## Creating Topologies in Apache Storm 🔨

```java
TopologyBuilder builder = new TopologyBuilder(); 
  
builder.setSpout("words", new TestWordSpout(), 10);          
builder.setBolt("exclaim", new ExclamationBolt(), 3).shuffleGrouping("words"); 
  
StormSubmitter.submitTopologyWithProgressBar(args[0], config, builder.createTopology()); 
```

---

## Examples of Apache Storm Applications 💡

- Apache Storm can be used in Real-Time Analytics platforms like Twitter to deliver search queries results and identify trends instantaneously.
- Continuous computation systems use Apache Storm to continuously profile and update ML models.
- Apache Storm is also useful in transforming and funneling a stream of logs in log processing systems and collecting Real-Time Business Intelligence.

--- 

## Conclusion 🏁

Understanding and leveraging the capabilities of Apache Storm is essential in today's real-time data processing needs. The distributed processing power it provides allows for rapid computations, which can power smart and fast decision-making applications.

---

Don't forget to star ⭐ this repo if you find it useful and want to track updates!

> Feel free to use this repository for your understanding and reference for Apache Storm. If you have a great suggestion on how to improve this or want to maintain, please feel free to reach out to me at `@jl33-ai` !
