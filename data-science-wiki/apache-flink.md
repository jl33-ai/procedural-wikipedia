# Apache Flink 🚀

> Created by @jl33-ai 👦🏻 

Apache Flink is an open-source stream processing framework for high-performance, scalable, and accurate real-time applications.

## Table of Contents
- [Introduction](#Introduction)
- [Installation](#Installation)
- [Features](#Features)
- [Quick Example](#Quick-Example)
- [Advantages](#Advantages)
- [Further Reading](#Further-Reading)

## Introduction
Apache Flink is a framework and distributed processing engine for stateful computations over unbounded and bounded data streams. It's designed to run in all common cluster environments and can perform computations at in-memory speed.

## Installation 💻

1. Download the binary:
    ```bash
    wget https://www.apache.org/dyn/closer.lua/flink/flink-1.11.2/flink-1.11.2-bin-scala_2.11.tgz
    tar xvf flink-1.11.2-bin-scala_2.11.tgz
    cd flink-1.11.2-bin-scala_2.11
    ```
2. Run the start script:
    ```bash
    ./bin/start-cluster.sh
    ```
And you have your Flink cluster running!

## Features 🎯

- **Event Time**: Flink explicitly supports three different notions of time: event time, ingestion time, and processing time.

- **State & Fault Tolerance**: Flink is renowned for its superb state handling and fault tolerance abilities.

- **Throughput and Latency**: It excels at processing high-throughput, low-latency data streams.

- **Functions and Operators**: Flink provides various APIs for transformations on datasets - maps, filters, windows, aggregations, etc.

- **Memory Management**: Flink provides its own memory management system that operates independently of Java's garbage collector.

- **Libraries**: Flink's ecosystem includes libraries for complex event processing (CEP), machine learning, and graph processing.

## Quick Example 🎓

Here is a simple stream processing example implemented in Apache Flink:

```java
DataStream<String> text = env.socketTextStream("<hostname>", <port>);

DataStream<WordWithCount> counts = text
    .flatMap(new Tokenizer())
    .keyBy("word")
    .timeWindow(Time.seconds(5))
    .reduce(new ReduceFunction<WordWithCount>() {
        public WordWithCount reduce(WordWithCount a, WordWithCount b) {
            return new WordWithCount(a.word, a.count + b.count);
        }
    });

counts.print().setParallelism(1);

env.execute("Socket Window WordCount");
```

It connects to a socket, tokenize the input into words, groups by word, window for 5 seconds, summing the occurrences and then prints the results.

## Advantages 🏅

- Apache Flink provides high-throughput and low-latency, enabling faster decision-making capabilities.

- Its processing model supports both stream (real-time) and batch processing.

- Scalability - it can efficiently process large scale data.

- Highly available and failure-tolerant, with built-in exactly-once processing semantics.

- Variety of libraries and integrations.

## Further Reading 📚

To get started with Apache Flink, visit:

- [Official Apache Flink Documentation](https://flink.apache.org/)

- [Apache Flink GitHub Repo](https://github.com/apache/flink)

- [Apache Flink Examples](https://github.com/apache/flink/tree/master/flink-examples)
