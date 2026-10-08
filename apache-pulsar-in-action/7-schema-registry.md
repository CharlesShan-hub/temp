# 7 Schema registry

This chapter covers

- Using the Pulsar schema to simplify your microservice development

- Understanding the different schema compatibility types

- Using the LocalRunner class to run and debug your functions inside your IDE

- Evolving a schema without impacting existing consumers

Traditional databases employ a process referred to as schema-on-write, where the table’s columns, rows, and types are all defined before any data can be written into the table. This ensures that the data conforms to a predetermined specification and the consuming clients can access the schema information directly from the database itself, which enables them to determine the basic structure of the records they are processing.

Apache Pulsar messages are stored as unstructured byte arrays, and the structure is applied to this data only when it’s read. This approach is referred to as schema-on-read and was first popularized by Hadoop and NoSQL databases. While the schema-on-read approach makes it easier to ingest and process new and dynamic data sources on the fly, it does have some drawbacks, including the lack of a metastore that clients can access to determine the schema for the Pulsar topic they are consuming from.

Pulsar clients just see a stream of individual records that can be of any type and need an efficient way to determine how to interpret each arriving record. This is where the Pulsar schema registry comes into play. It is a critical component of the Pulsar technology stack that tracks the schema of all the topics inside of Pulsar.

As we saw in the last chapter, the development team for the food delivery service company GottaEat has decided to embrace the microservice architectural style in which applications are comprised of a collection of loosely coupled, independently developed services. In such an architecture, different microservices will need to collaborate on the same data, and in order to do that, they will need to know the basic structure of the event, including the fields and their associated types. Otherwise, the event consumers will not be able to perform any meaningful calculations on the event data. In this chapter, I will demonstrate how Pulsar’s schema registry can be used to greatly simplify the sharing of this information across the application teams at GottaEat.


## 子目录

- [7.1 Microservice communication](<7-schema-registry/7.1-microservice-communication.md>)
- [7.2 The Pulsar schema registry](<7-schema-registry/7.2-the-pulsar-schema-registry.md>)
- [7.3 Using the schema registry](<7-schema-registry/7.3-using-the-schema-registry.md>)
- [7.4 Evolving the schema](<7-schema-registry/7.4-evolving-the-schema.md>)
- [Summary](<7-schema-registry/summary.md>)
