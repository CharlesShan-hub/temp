# 5 Pulsar IO connectors

This chapter covers

- An introduction to the Pulsar IO framework

- Configuring, deploying, and monitoring Pulsar IO connectors

- Writing your own Pulsar IO connector in Java

Messaging systems are much more useful when you can easily use them to move data into and out of other external systems, such as databases, local and distributed filesystems, or other messaging systems. Consider the scenario where you want to ingest log data from external sources, such as applications, platforms, and cloud-based services, and publish it to a search engine for analysis. This could easily be accomplished with a pair of Pulsar IO connectors; the first would be a Pulsar source that collects the application logs, and the second would be a Pulsar sink that writes the formatted records to Elasticsearch.

Pulsar provides a collection of pre-built connectors that can be used to interact with external systems, such as Apache Cassandra, Elasticsearch, and HDFS, just to name a few. The Pulsar IO framework is also extensible, which allows you to develop your own connectors to support new or legacy systems as needed.


## 子目录

- [5.1 What are Pulsar IO connectors?](<5-pulsar-io-connectors/5.1-what-are-pulsar-io-connectors_.md>)
- [5.2 Developing Pulsar IO connectors](<5-pulsar-io-connectors/5.2-developing-pulsar-io-connectors.md>)
- [5.3 Testing Pulsar IO connectors](<5-pulsar-io-connectors/5.3-testing-pulsar-io-connectors.md>)
- [5.4 Deploying Pulsar IO connectors](<5-pulsar-io-connectors/5.4-deploying-pulsar-io-connectors.md>)
- [5.5 Pulsar’s built-in connectors](<5-pulsar-io-connectors/5.5-pulsar’s-built-in-connectors.md>)
- [5.6 Administering Pulsar IO connectors](<5-pulsar-io-connectors/5.6-administering-pulsar-io-connectors.md>)
- [Summary](<5-pulsar-io-connectors/summary.md>)
