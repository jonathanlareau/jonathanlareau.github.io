---
layout: default
title:  "Kafka in Windows"
date:   2020-02-01 11:11:11 -1111
categories: notes
permalink: /kafka-win/
---
# Kafka installation in windows

## Official documentation
[https://kafka.apache.org/quickstart](https://kafka.apache.org/quickstart)

### Download kafka and zookeeper bundle
- https://www.apache.org/dyn/closer.cgi?path=/kafka/2.4.0/kafka_2.12-2.4.0.tgz

### Run
- zookeeper

C:\kafka_2.13-2.4.0\bin\windows/zookeeper-server-start.bat C:\kafka_2.13-2.4.0\config/zookeeper.properties
- kafka

C:\kafka_2.13-2.4.0\bin\windows/kafka-server-start.bat C:\kafka_2.13-2.4.0\config/server.properties

### Tests
- C:\kafka_2.13-2.4.0\bin\windows/kafka-topics.bat --create --zookeeper kafka-zookeeper:2181 --replication-factor 1 --partitions 1 --topic test
- C:\kafka_2.13-2.4.0\bin\windows/kafka-topics.bat --list --zookeeper kafka-zookeeper:2181
- C:\kafka_2.13-2.4.0\bin\windows/kafka-console-producer.bat --broker-list kafka-zookeeper:9092 --topic test
- C:\kafka_2.13-2.4.0\bin\windows/kafka-console-consumer.bat --bootstrap-server kafka-zookeeper:9092 --topic test --from-beginning

