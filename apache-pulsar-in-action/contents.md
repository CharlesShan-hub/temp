# contents

foreword

preface

acknowledgments

about this book

about the author

about the cover illustration

Part 1 Getting started with Apache Pulsar

1 Introduction to Apache Pulsar

1.1 Enterprise messaging systems

Key capabilities

1.2 Message consumption patterns

Publish-subscribe messaging

Message queuing

1.3 The evolution of messaging systems

Generic messaging systems

Message-oriented middleware

Enterprise service bus

Distributed messaging systems

1.4 Comparison to Apache Kafka

Multilayered architecture

Message consumption

Data durability

Message acknowledgment

Message retention

1.5 Why do I need Pulsar?

Guaranteed message delivery

Infinite scalability

Resilient to failure

Support for millions of topics

Geo-replication and active failover

1.6 Real-world use cases

Unified messaging systems

Microservices platforms

Connected cars

Fraud detection

2 Pulsar concepts and architecture

2.1 Pulsar’s physical architecture

Pulsar’s layered architecture

Stateless serving layer

Stream storage layer

Metadata storage

2.2 Pulsar’s logical architecture

Tenants, namespaces, and topics

Addressing topics in Pulsar

Producers, consumers, and subscriptions

Subscription types

2.3 Message retention and expiration

Data retention

Backlog quotas

Message expiration

Message backlog vs. message expiration

2.4 Tiered storage

3 Interacting with Pulsar

3.1 Getting started with Pulsar

3.2 Administering Pulsar

Creating a tenant, namespace, and topic

Java Admin API

3.3 Pulsar clients

The Pulsar Java client

The Pulsar Python client

The Pulsar Go client

3.4 Advanced administration

Persistent topic metrics

Message inspection

Part 2 Apache Pulsar development essentials

4 Pulsar functions

4.1 Stream processing

Traditional batching

Micro-batching

Stream native processing

4.2 What is Pulsar Functions?

Programming model

4.3 Developing Pulsar functions

Language native functions

The Pulsar SDK

Stateful functions

4.4 Testing Pulsar functions

Unit testing

Integration testing

4.5 Deploying Pulsar functions

Generating a deployment artifact

Function configuration

Function deployment

The function deployment life cycle

Deployment modes

Pulsar function data flow

5 Pulsar IO connectors

5.1 What are Pulsar IO connectors?

Sink connectors

Source connectors

PushSource connectors

5.2 Developing Pulsar IO connectors

Developing a sink connector

Developing a PushSource connector

5.3 Testing Pulsar IO connectors

Unit testing

Integration testing

Packaging Pulsar IO connectors

5.4 Deploying Pulsar IO connectors

Creating and deleting connectors

Debugging deployed connectors

5.5 Pulsar’s built-in connectors

Launching the MongoDB cluster

Link the Pulsar and MongoDB containers

Configure and create the MongoDB sink

5.6 Administering Pulsar IO connectors

Listing connectors

Monitoring connectors

6 Pulsar security

6.1 Transport encryption

6.2 Authentication

TLS authentication

JSON Web Token authentication

6.3 Authorization

Roles

An example scenario

6.4 Message encryption

7 Schema registry

7.1 Microservice communication

Microservice APIs

The need for a schema registry

7.2 The Pulsar schema registry

Architecture

Schema versioning

Schema compatibility

Schema compatibility check strategies

7.3 Using the schema registry

Modelling the food order event in Avro

Producing food order events

Consuming the food order events

Complete example

7.4 Evolving the schema

Part 3 Hands-on application development with Apache Pulsar

8 Pulsar Functions patterns

8.1 Data pipelines

Procedural programming

DataFlow programming

8.2 Message routing patterns

Splitter

Dynamic router

Content-based router

8.3 Message transformation patterns

Message translator

Content enricher

Content filter

9 Resiliency patterns

9.1 Pulsar Functions resiliency

Adverse events

Fault detection

9.2 Resiliency design patterns

Retry pattern

Circuit breaker

Rate limiter

Time limiter

Cache

Fallback pattern

Credential refresh pattern

9.3 Multiple layers of resiliency

10 Data access

10.1 Data sources

10.2 Data access use cases

Device validation

Driver location data

11 Machine learning in Pulsar

11.1 Deploying ML models

Batch processing

Near real-time

11.2 Near real-time model deployment

11.3 Feature vectors

Feature stores

Feature calculation

11.4 Delivery time estimation

ML model export

Feature vector mapping

Model deployment

11.5 Neural nets

Neural net training

Neural net deployment in Java

12 Edge analytics

12.1 IIoT architecture

The perception and reaction layer

The transportation layer

The data processing layer

12.2 A Pulsar-based processing layer

12.3 Edge analytics

Telemetric data

Univariate and multivariate

12.4 Univariate analysis

Noise reduction

Statistical analysis

Approximation

12.5 Multivariate analysis

Creating a bidirectional messaging mesh

Multivariate dataset construction

12.6 Beyond the book

appendix A Running Pulsar on Kubernetes

appendix B Geo-replication

index
