# 10 Data access

This chapter covers

- Storing and retrieving data with Pulsar Functions

- Using Pulsar’s internal state mechanism for data storage and retrieval

- Accessing data from external systems with Pulsar Functions

Thus far all of the information used by our Pulsar Functions has been provided inside the incoming messages. While this is an effective way to exchange information, it is not the most efficient or desirable way for Pulsar Functions to exchange information with one another. The biggest drawback to this approach is that it creates a dependency on the message source to provide your Pulsar function with the information it needs to do its job. This violates the encapsulation principle of object-oriented design, which dictates that the internal logic of a function should not be exposed to the outside world. Currently, any changes to the logic inside one function might require changes to the upstream function that provides the incoming messages.

Consider a use case where you are writing a function that requires a customer’s contact information, including their cell phone number. Rather than passing a message containing all of that information, wouldn’t it be easier to just pass the customer ID, which can then be used by our function to query the database and retrieve the information we need instead? In fact, this is a common access pattern if the information required by the function exists in an external data source, such as a database. This approach enforces encapsulation and prevents changes in one function from directly impacting other functions by relying on each function to gather the information it needs instead of providing it inside the incoming message.

In this chapter, I will walk through several uses cases that need to store and/or retrieve data from an external system and demonstrate how to do so using Pulsar Functions. In doing so, I will cover a variety of different data stores and describe the various criteria used to select one technology over another.


## 子目录

- [10.1 Data sources](<10-data-access/10.1-data-sources.md>)
- [10.2 Data access use cases](<10-data-access/10.2-data-access-use-cases.md>)
- [Summary](<10-data-access/summary.md>)
