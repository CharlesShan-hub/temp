# Part 3 Hands-on application development with Apache Pulsar

In this part, we move beyond the theory and simplistic examples and dive into the use of Pulsar Functions as a development framework for microservices applications by walking through a much more realistic use case based on a fictional food delivery service called GottaEat. This section demonstrates how to implement common design patterns from both the enterprise integration world and the microservices world, highlighting the usage of various patterns, such as content-based routing and filtering, resiliency, and data access within a real-world scenario.

Chapter 8 demonstrates how to implement common messaging routing patterns, such as message splitting, content-based routing, and filtering. It also shows how to implement various message transformation patterns, such as value extraction and message translation.

Chapter 9 stresses the importance of having resiliency built into your microservices and demonstrates how to implement this inside your Java-based Pulsar functions with the help of the resiliency4j library. It covers various scenarios that can occur in an event-based program and the patterns you can use to insulate your microservices from these failure scenarios to maximize your application uptime.

Chapter 10 focuses on how you can access data from a variety of external systems from inside your Pulsar functions. It demonstrates different methods of acquiring information within your microservices and considerations you should take in terms of latency.

Chapter 11 walks you through the process of deploying different machine learning model types inside of a Pulsar function, using various ML frameworks. It also covers the very important aspect of how to feed the necessary information into the model to get an accurate prediction

Finally, chapter 12 covers the use of Pulsar Functions within an edge computing environment to perform real-time analytics on IoT data. It starts with a detailed description of what an edge computing environment looks like and describes the various layers of the architecture before showing how to leverage Pulsar Functions to process the information on the edge and only forward summaries, rather than the entire dataset.
