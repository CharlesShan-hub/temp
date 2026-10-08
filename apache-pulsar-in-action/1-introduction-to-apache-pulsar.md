# 1 Introduction to Apache Pulsar

This chapter covers

- The evolution of the enterprise messaging system

- A comparison of Apache Pulsar to existing enterprise messaging systems

- How Pulsar’s segment-centric storage differs from the partition-centric storage model used in Apache Kafka

- Real-world use cases where Pulsar is used for stream processing, and why you should consider using Apache Pulsar

Developed by Yahoo! in 2013, Pulsar was first open sourced in 2016, and only 15 months after joining the Apache Software Foundation’s incubation program, it graduated to top-level project status. Apache Pulsar was designed from the ground up to address the gaps in current open source messaging systems, such as multi-tenancy, geo-replication, and strong durability guarantees.

The Apache Pulsar site describes it as a distributed pub-sub messaging system that provides very low publish and end-to-end latency, guaranteed message delivery, zero data loss, and a serverless, lightweight computing framework for stream data processing. Apache Pulsar provides three key capabilities for processing large data sets:

- *Real-time messaging* —Enables geographically distributed applications and systems to communicate with one another in an asynchronous manner by exchanging messages. Pulsar’s goal is to provide this capability to the broadest audience of clients via support for multiple programming languages and binary messaging protocols.

- *Real-time compute* —Provides the ability to perform user-defined computations on these messages inside of Pulsar itself and without the need for an external computational system to perform basic transformational operations, such as data enrichment, filtering, and aggregations.

- *Scalable storage* —Pulsar’s independent storage layer and support for tiered storage enable the retention of your message data for as long as you need. There is no physical limitation on the amount of data that can be retained and accessed by Pulsar.


## 子目录

- [1.1 Enterprise messaging systems](<1-introduction-to-apache-pulsar/1.1-enterprise-messaging-systems.md>)
- [1.2 Message consumption patterns](<1-introduction-to-apache-pulsar/1.2-message-consumption-patterns.md>)
- [1.3 The evolution of messaging systems](<1-introduction-to-apache-pulsar/1.3-the-evolution-of-messaging-systems.md>)
- [1.4 Comparison to Apache Kafka](<1-introduction-to-apache-pulsar/1.4-comparison-to-apache-kafka.md>)
- [1.5 Why do I need Pulsar?](<1-introduction-to-apache-pulsar/1.5-why-do-i-need-pulsar_.md>)
- [1.6 Real-world use cases](<1-introduction-to-apache-pulsar/1.6-real-world-use-cases.md>)
- [Additional resources](<1-introduction-to-apache-pulsar/additional-resources.md>)
- [Summary](<1-introduction-to-apache-pulsar/summary.md>)
