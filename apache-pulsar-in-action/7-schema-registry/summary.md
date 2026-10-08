## Summary

- We discussed the different microservice communication styles and why Pulsar is a perfect fit for asynchronous publish/subscribe-based interservice communication.

- The Pulsar schema registry enables message producers and consumers to coordinate on the structure of the data at the topic level and enforces schema compatibility for message producers.

- The Pulsar schema registry supports eight different compatibility strategies, including forward, backward, and full, and each of the compatibility checks are from the consumer’s perspective.

- The Avro’s interface definition language (IDL) is a great way to model events consumed within Pulsar because it allows you to modularize your types and share them across services easily.

- The Pulsar schema registry can be configured to enforce forward and/or backward schema compatibility for a Pulsar topic by ensuring that the connecting producer or consumer are using a schema that is compatible with all existing clients.
