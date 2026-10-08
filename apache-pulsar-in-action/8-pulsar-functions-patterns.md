# 8 Pulsar Functions patterns

This chapter covers

- Designing an application based on Pulsar Functions

- Implementing well-established messaging patterns using Pulsar Functions

In the previous chapter, I introduced a hypothetical food delivery service named GottaEat and outlined the basic order entry use case in which customers place orders with the company’s mobile application. As you may recall, the first microservice in that process was the OrderValidationService, which is responsible for ensuring that the order is valid before forwarding the order to the drivers for delivery if it is valid or notifying the customer of any errors with the order.

However, the term *validate* is a bit more complicated than merely ensuring all of the fields are of the proper type and format. In this particular scenario, an order is only considered valid if the method of payment provided by the customer is approved, the funds from the bank are authorized, there is at least one restaurant open and willing to provide all of the requested food items, and, most importantly, the delivery address provided by the customer can be resolved to both a latitude-longitude pair and a street address. If we are unable to confirm all of these, then the order is considered invalid, and the customer must be notified accordingly. Consequently, the OrderValidationService is not a simple microservice that can make all of these decisions on its own, but instead, it must coordinate with other systems. It is, therefore, a good example of how a Pulsar application can be composed of several smaller functions and services.

The OrderValidationService must integrate with several other microservices and external systems to perform the payment processing, geo-encoding, and food order placement required to fully validate an order. Therefore, it is best to look for existing solutions to these types of challenges rather than reinvent the wheel, and the catalog of patterns contained within the book *Enterprise Integration Patterns, by Gregor Hohpe and Bobby Woolf (Addison-Wesley Professional, 2003),* serves as a great reference in this regard. It contains several technology-agnostic, time-tested patterns to solve common integration challenges. These patterns are categorized according to the type of problem they address and are applicable to most message-based integration platforms. In the next sections, I will demonstrate how these patterns can be implemented using Pulsar Functions.


## 子目录

- [8.1 Data pipelines](<8-pulsar-functions-patterns/8.1-data-pipelines.md>)
- [8.2 Message routing patterns](<8-pulsar-functions-patterns/8.2-message-routing-patterns.md>)
- [8.3 Message transformation patterns](<8-pulsar-functions-patterns/8.3-message-transformation-patterns.md>)
- [Summary](<8-pulsar-functions-patterns/summary.md>)
