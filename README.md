# Kafka For Beginners

This repository serves as an introduction into the kafka world. It will consist of several small projects demonstrating kafka and its use cases. Note that these projects have been written on a windows machine

These projects include:
* basic-kafka-consumer - A simple Kafka consumer application which will consume records on topic 'first_topic'
* basic-kafka-producer - A simple Kafka producer application which will produce records to topic 'first_topic'
* spring-kafka-consumer - A simple kafka consumer service which consumers of two topics.The first topic expects a Player object value while the other topic expects a Json string value

## Getting Started
Please follow the below steps to setup the solution on your machine. 

### Prerequisites
* [Java 14 jdk](https://www.oracle.com/java/technologies/javase-jdk14-downloads.html)
* [Maven 3.6](https://maven.apache.org/install.html) - Please follow this [guide](https://howtodoinjava.com/maven/how-to-install-maven-on-windows/)
* [IntelliJ IDE](https://www.jetbrains.com/idea/download/#section=windows)
* [Kafka](https://kafka.apache.org/downloads) - Choose the recommended Scala binary and download. I downloaded kafka to my c:\ drive .ie c:\kafka_2.12-2.5.0

### Kafka Setup
#### Zookeeper
* Open the cmd prompt in the location where kafka was extracted
* Start Kafka Zookeeper. Zookeeper is at localhost:2181
```
.\bin\windows\zookeeper-server-start.bat config\zookeeper.properties
```
#### Kafka Server
* Open the cmd prompt in the location where kafka was extracted
* Start Kafka Server. Kafka is at localhost:9092
```
.\bin\windows\kafka-server-start.bat config\server.properties
```
#### Kafka Topic Creation
* Open the cmd prompt in the location where kafka was extracted
* Create Input Topic. It is important that all topics are created before they can be used in the kafka applications. Use the same cmd prompt to create all topics. Topics can be any name
```
.\bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic words-input
.\bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic words-count
```
* Verify the topic has been created
```
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list
```

#### Start Kafka Stream Application
* From Intellj Run the Application
#### Notes
* Do not close any cmd prompts when running kafka
* Kafka has been setup using the default settings
 
## Resources

## Todo
* Lots

## Authors
* Sashen Govender


