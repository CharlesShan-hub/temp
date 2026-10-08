## How this book is organized: A roadmap

This book consists of 12 chapters that are spread across three different parts. Part 1 starts with a basic introduction to Apache Pulsar and where it fits in the 40-year evolution of messaging systems by comparing it to and contrasting it with the various messaging platforms that have come before it:

- Chapter 1 provides a historical perspective on messaging systems and where Apache Pulsar fits into the 40-year evolution of messaging technology. It also previews some of Pulsar’s architectural advantages over other systems and why you should consider using it as your single messaging platform of choice.

- Chapter 2 covers the details of Pulsar’s multi-tiered architecture, which allows you to dynamically scale up the storage or serving layers independently. It also describes some of the common message consumption patterns, how they are different from one another, and how Pulsar supports them all.

- Chapter 3 demonstrates how to interact with Apache Pulsar from both the command line as well as by using its programming API. After completing this chapter, you should be comfortable running a local instance of Apache Pulsar and interacting with it.

Part 2 covers some of the more basic usage and features of Pulsar, including how to perform basic messaging and how to secure your Pulsar cluster, along with more advanced features such as the schema registry. It also introduces the Pulsar Functions framework, including how to build, deploy, and test functions:

- Chapter 4 introduces Pulsar’s stream native computing framework called Pulsar Functions, provides some background on its design and configuration, and show you how to develop, test, and deploy functions.

- Chapter 5 introduces Pulsar’s connector framework that is designed to move between Apache Pulsar and external storage systems, such as relational databases, key-value stores, and blob storage such as S3. It teaches you how to develop a connector in a step-by-step fashion.

- Chapter 6 provides step-by-step details on how to secure your Pulsar cluster to ensure that your data is secured while it is in transit and while it is at rest.

- Chapter 7 covers Pulsar’s built-in schema registry, why it is necessary, and how it can help simplify microservice development. We also cover the schema evolution process and how to update the schemas used inside your Pulsar Functions.

Part 3 focuses on the use of Pulsar Functions to implement microservices and demonstrates how to implement various common microservice design patterns within Pulsar Functions. This section focuses on the development of a food delivery application to make the examples more realistic and addresses more-complex use cases including resiliency, data access, and how to use Pulsar Functions to deploy machine learning models that can run against real-time data:

- Chapter 8 demonstrates how to implement common messaging routing patterns such as message splitting, content-based routing, and filtering. It also shows how to implement various message transformation patterns such as value extraction and message translation.

- Chapter 9 stresses the importance of having resiliency built into your microservices and demonstrates how to implement this inside your Java-based Pulsar Functions with the help of the resiliency4j library. It covers various events that can occur in an event-based program and the different patterns you can use to insulate your services from these failure scenarios to maximize your application uptime.

- Chapter 10 focuses on how you can access data from a variety of external systems from inside your Pulsar functions. It demonstrates various ways of acquiring information within your microservices and considerations you should take into account in terms of latency.

- Chapter 11 walks you through the process of deploying different machine learning model types inside of a Pulsar function using various ML frameworks. It also covers the very important topic of how to feed the necessary information into the model to get an accurate prediction

- Chapter 12 covers the use of Pulsar Functions within an edge computing environment to perform real-time analytics on IoT data. It starts with a detailed description of what an edge computing environment looks like and describes the various layers of the architecture before showing how to leverage Pulsar Functions to process the information on the edge and only forward summaries rather than the entire dataset.

Finally, two appendices demonstrate more advanced operational scenarios including deployment within a Kubernetes environment and geo-replication:

- Appendix A walks you through the steps necessary to deploy Pulsar into a Kubernetes environment using the Helm charts that are provided as part of the open source project. It also covers how to modify these charts to suit your environment.

- Appendix B describes Pulsar’s built-in geo-replication mechanism and some of the common replication patterns that are used in production today. It then walks you through the process of implementing one of these geo-replication patterns in Pulsar.
