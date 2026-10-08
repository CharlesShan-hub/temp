## Summary

- The Pulsar Functions framework is a distributed processing framework that is well suited for Dataflow programming, where the data is processed in stages that can be executed in parallel like an assembly line.

- Applications based on Pulsar Functions can be modelled as data pipelines, where the functions perform the computations and direct data, using the input/out topics.

- When designing your message-passing microservice application, it is often to use existing design patterns, such as those found in Gregor Hohpe and Bobby Woolf’s book *Enterprise Integration Patterns* and other sources.

- Well-established messaging patterns can be implemented using Pulsar Functions, which allows you to use time-tested solutions inside your applications.
