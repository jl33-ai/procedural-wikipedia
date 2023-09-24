# Apache Kafka

Created by @jl33-ai 👦🏻

Apache Kafka is a popular open-source stream processing platform developed by the Apache Software Foundation written in Scala and Java. Kafka can be used for several purposes:

- Real-time data pipeline processing
- Building real-time streaming applications
- Real-time analytics
- Event sourcing
- Commit logs, etc.

## Table of Contents
1. [Installation](#install)
2. [Apache Kafka Architecture](#architecture)
3. [Apache Kafka Fundamentals](#fundamentals)
4. [Working with Apache Kafka](#working)
5. [Kafka API](#api)
6. [Examples](#examples)
7. [Summary](#summary)

## <a name='install'></a>Installation 📦
Apache Kafka requires Java 8 or higher. To install Apache Kafka, follow these steps:
```shell
tar -xzf kafka_2.11-0.11.0.0.tgz
cd kafka_2.11-0.11.0.0
```
## <a name='architecture'></a>Apache Kafka Architecture 👷
Apache Kafka follows a simple, high performance and distributed design. Here are its main components:

1. **Producer** - Producers publish data to the topics of their choice.

2. **Consumer** - Consumers read data from the topics.

3. **Broker** - Brokers are simple system handling failover for consumers and distributing load. 

4. **Zookeeper** - Zookeeper is used for managing and coordinating Kafka brokers.

5. **Topic** - A stream of messages belonging to a particular category is a topic.

## <a name='fundamentals'></a>Apache Kafka Fundamentals 📚
Here are some great features of Apache Kafka:

1. **High-throughput** - Kafka is able to handle high volume of data and enables the passage of messages.

2. **Fault-Tolerant** - It’s able to replicate data to prevent loss of data and handle failures.

3. **Low latency** - Kafka has real-time handling capabilities.

4. **Durability** - Kafka uses Distributed commit logs ensuring message persistence.

## <a name='working'></a>Working with Apache Kafka 🛠
Start the server:
```shell
bin/kafka-server-start.sh config/server.properties
```
Create a topic:
```shell
bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic Test-Topic
```
Send some messages:
```shell
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic Test-Topic
```
Start a consumer:
```shell
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic Test-Topic --from-beginning
```

## <a name='api'></a>Kafka API 🖥
Kafka has four core APIs:

1. **Producer API** - This API allows an application to publish streams of records to one or more Kafka topics.

2. **Consumer API** - This API allows an application to subscribe to one or more topics and process the stream of records.

3. **Streams API** - This API allows an application to act as a stream processor.

4. **Connector API** - This API allows building and running reusable producers or consumers that connect Kafka topics to existing applications.

## <a name='examples'></a>Examples 👨‍💻
Here is a basic example of creating a producer in Java:

```java
import org.apache.kafka.clients.producer.*;
import java.util.*;

public class FirstAppProducer {
    public static void main(String[] args) {
        String topicName = "SimpleProducerTopic";
        String key = "Key1";
        String value = "Value1-1";

        Properties props = new Properties();
        props.put("bootstrap.servers", "localhost:9092,localhost:9093");
        props.put("key.serializer","org.apache.kafka.common.serialization.StringSerializer");         
        props.put("value.serializer", "org.apache.kafka.common.serialization.StringSerializer");
        
        Producer<String, String> producer = new KafkaProducer<>(props);
        
        ProducerRecord<String, String> record = new ProducerRecord<>(topicName,key,value);
        producer.send(record);        
        producer.close();
        
        System.out.println("SimpleProducer Completed.");
    }
}
```
## <a name='summary'></a>Summary 📝
Apache Kafka is a powerful, open-source stream processing platform that provides real-time data feeds. It's designed to be fast, scalable, durable, and fault-tolerant.

## References 🔖
1. [Apache Kafka Official Documentation](https://kafka.apache.org/documentation/)

## Tags 🏷