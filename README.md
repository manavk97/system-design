# system-design

This repository aims to provide high-quality materials and resources related to system design. It serves as a comprehensive collection of information, examples, and best practices to help developers, architects, and engineers learn and improve their system design skills.

## Table of Contents
1. [Distributed System Design Patterns](#1-distributed-system-design-patterns)
    1. [Data Management Patterns](#11-data-management-patterns)
    2. [Design and Implementation Patterns](#12-design-and-implementation-patterns)
    3. [Messaging Patterns](#13-messaging-patterns)
2. [Design Patterns (OOP)](#2-design-patterns-oop)
    1. [Creational Patterns](#21-creational-patterns)
    2. [Structural Patterns](#22-structural-patterns)
    3. [Behavioral Patterns](#23-behavioral-patterns)
3. [Real World System Design Case Studies](#3-real-world-system-design-case-studies)
4. [System Concepts](#4-system-concepts)
    1. [Protocols](#41-protocols)
    2. [Deployment Patterns](#42-deployment-patterns)
    3. [Load Balancing Patterns](#43-load-balancing-patterns)
5. [System Components](#5-system-components)

## System Design Concepts

### 1. Distributed System Design Patterns

Distributed system design patterns are reusable solutions to common problems encountered when designing large-scale, distributed systems. These patterns help in creating scalable, reliable, and efficient systems.

#### 1.1. [Data Management Patterns](#11-data-management-patterns)

| Pattern | Description |
|---------|-------------|
| [Cache-Aside](https://learn.microsoft.com/en-us/azure/architecture/patterns/cache-aside) | Load data on demand into a cache from a data store |
| [CQRS](https://learn.microsoft.com/en-us/azure/architecture/patterns/cqrs) | Segregate operations that read data from operations that update data by using separate interfaces |
| [Event Sourcing](https://learn.microsoft.com/en-us/azure/architecture/patterns/event-sourcing) | Use an append-only store to record the full series of events that describe actions taken on data in a domain |
| [Index Table](https://learn.microsoft.com/en-us/azure/architecture/patterns/index-table) | Create indexes over the fields in data stores that are frequently referenced by queries |
| [Materialized View](https://learn.microsoft.com/en-us/azure/architecture/patterns/materialized-view) | Generate prepopulated views over the data in one or more data stores when the data isn't ideally formatted for required query operations |
| [Sharding](https://learn.microsoft.com/en-us/azure/architecture/patterns/sharding) | Divide a data store into a set of horizontal partitions or shards |
| [Static Content Hosting](https://learn.microsoft.com/en-us/azure/architecture/patterns/static-content-hosting) | Deploy static content to a cloud-based storage service that can deliver them directly to the client |
| [Valet Key](https://learn.microsoft.com/en-us/azure/architecture/patterns/valet-key) | Use a token or key that provides clients with restricted direct access to a specific resource or service |

#### 1.2. [Design and Implementation Patterns](#12-design-and-implementation-patterns)

| Pattern | Description |
|---------|-------------|
| [Ambassador](https://learn.microsoft.com/en-us/azure/architecture/patterns/ambassador) | Create helper services that send network requests on behalf of a consumer service or application. |
| [Anti-Corruption Layer](https://learn.microsoft.com/en-us/azure/architecture/patterns/anti-corruption-layer) | Implement a façade or adapter layer between a modern application and a legacy system. |
| [Backends for Frontends](https://learn.microsoft.com/en-us/azure/architecture/patterns/backends-for-frontends) | Create separate backend services to be consumed by specific frontend applications or interfaces. |
| [CQRS](https://learn.microsoft.com/en-us/azure/architecture/patterns/cqrs) | Segregate operations that read data from operations that update data by using separate interfaces. |
| [Compute Resource Consolidation](https://learn.microsoft.com/en-us/azure/architecture/patterns/compute-resource-consolidation) | Consolidate multiple tasks or operations into a single computational unit |
| [Edge Workload Configuration](https://learn.microsoft.com/en-us/azure/architecture/patterns/edge-workload-configuration) | The great variety of systems and devices on the shop floor can make workload configuration a difficult problem. |
| External Configuration Store | Move configuration information out of the application deployment package to a centralized location. |
| [Gateway Aggregation](https://learn.microsoft.com/en-us/azure/architecture/patterns/gateway-aggregation) | Use a gateway to aggregate multiple individual requests into a single request. |
| [Gateway Offloading](https://learn.microsoft.com/en-us/azure/architecture/patterns/gateway-offloading) | Offload shared or specialized service functionality to a gateway proxy. |
| [Gateway Routing](https://learn.microsoft.com/en-us/azure/architecture/patterns/gateway-routing) | Route requests to multiple services using a single endpoint. |
| [Leader Election](https://learn.microsoft.com/en-us/azure/architecture/patterns/leader-election) | Coordinate the actions performed by a collection of collaborating task instances in a distributed application by electing one instance as the leader that assumes responsibility for managing the other instances. |
| [Pipes and Filters](https://learn.microsoft.com/en-us/azure/architecture/patterns/pipes-and-filters) | Break down a task that performs complex processing into a series of separate elements that can be reused. |
| [Sidecar](https://learn.microsoft.com/en-us/azure/architecture/patterns/sidecar) | Deploy components of an application into a separate process or container to provide isolation and encapsulation. |
| [Static Content Hosting](https://learn.microsoft.com/en-us/azure/architecture/patterns/static-content-hosting) | Deploy static content to a cloud-based storage service that can deliver them directly to the client. |
| [Strangler Fig](https://learn.microsoft.com/en-us/azure/architecture/patterns/strangler-fig) | Incrementally migrate a legacy system by gradually replacing specific pieces of functionality with new applications and services. |

#### 1.3. [Messaging Patterns](#13-messaging-patterns)

| Pattern | Description |
|---------|-------------|
| [Asynchronous Request-Reply](https://learn.microsoft.com/en-us/azure/architecture/patterns/async-request-reply) | Decouple backend processing from a frontend host, where backend processing needs to be asynchronous, but the frontend still needs a clear response. |
| [Claim Check](https://learn.microsoft.com/en-us/azure/architecture/patterns/claim-check) | Split a large message into a claim check and a payload to avoid overwhelming a message bus. |
| [Choreography](https://learn.microsoft.com/en-us/azure/architecture/patterns/choreography) | Have each component of the system participate in the decision-making process about the workflow of a business transaction, instead of relying on a central point of control. |
| [Competing Consumers](https://learn.microsoft.com/en-us/azure/architecture/patterns/competing-consumers) | Enable multiple concurrent consumers to process messages received on the same messaging channel. |
| [Pipes and Filters](https://learn.microsoft.com/en-us/azure/architecture/patterns/pipes-and-filters) | Break down a task that performs complex processing into a series of separate elements that can be reused. |
| [Priority Queue](https://learn.microsoft.com/en-us/azure/architecture/patterns/priority-queue) | Prioritize requests sent to services so that requests with a higher priority are received and processed more quickly than those with a lower priority. |
| [Publisher-Subscriber](https://learn.microsoft.com/en-us/azure/architecture/patterns/publisher-subscriber) | Enable an application to announce events to multiple interested consumers asynchronously, without coupling the senders to the receivers. |
| [Queue-Based Load Leveling](https://learn.microsoft.com/en-us/azure/architecture/patterns/queue-based-load-leveling) | Use a queue that acts as a buffer between a task and a service that it invokes in order to smooth intermittent heavy loads. |
| [Saga](https://learn.microsoft.com/en-us/azure/architecture/patterns/saga) | Manage data consistency across microservices in distributed transaction scenarios. A saga is a sequence of transactions that updates each service and publishes a message or event to trigger the next transaction step. |
| [Scheduler Agent Supervisor](https://learn.microsoft.com/en-us/azure/architecture/patterns/scheduler-agent-supervisor) | Coordinate a set of actions across a distributed set of services and other remote resources. |
| [Sequential Convoy](https://learn.microsoft.com/en-us/azure/architecture/patterns/sequential-convoy) | Process a set of related messages in a defined order, without blocking processing of other groups of messages |
| [Actor Model](https://newsletter.systemdesign.one/p/actor-model) | A computational model for concurrent computation where actors are the universal primitives of computation. |

### 2. Design Patterns (OOP)

#### 2.1 [Creational Patterns](#21-creational-patterns)

These patterns provide various object creation mechanisms, which increase flexibility and reuse of existing code.

| Pattern | Description |
|---------|-------------|
| [Factory Method](https://refactoring.guru/design-patterns/factory-method) | Defines an interface for creating an object, but lets subclasses decide which class to instantiate |
| [Abstract Factory](https://refactoring.guru/design-patterns/abstract-factory) | Provides an interface for creating families of related or dependent objects without specifying their concrete classes |
| [Builder](https://refactoring.guru/design-patterns/builder) | Separates the construction of a complex object from its representation, allowing the same construction process to create various representations |
| [Prototype](https://refactoring.guru/design-patterns/prototype) | Creates new objects by copying an existing object, known as the prototype |
| [Singleton](https://refactoring.guru/design-patterns/singleton) | Ensures a class has only one instance and provides a global point of access to it |

#### 2.2. [Structural Patterns](#22-structural-patterns)

These patterns explain how to assemble objects and classes into larger structures while keeping these structures flexible and efficient.

| Pattern | Description |
|---------|-------------|
| [Adapter](https://refactoring.guru/design-patterns/adapter) | Allows objects with incompatible interfaces to collaborate |
| [Bridge](https://refactoring.guru/design-patterns/bridge) | Separates an object's abstraction from its implementation so that the two can vary independently |
| [Composite](https://refactoring.guru/design-patterns/composite) | Composes objects into tree structures to represent part-whole hierarchies |
| [Decorator](https://refactoring.guru/design-patterns/decorator) | Attaches additional responsibilities to an object dynamically |
| [Facade](https://refactoring.guru/design-patterns/facade) | Provides a simplified interface to a library, a framework, or any other complex set of classes |
| [Flyweight](https://refactoring.guru/design-patterns/flyweight) | Uses sharing to support large numbers of fine-grained objects efficiently |
| [Proxy](https://refactoring.guru/design-patterns/proxy) | Provides a surrogate or placeholder for another object to control access to it |

#### 2.3. [Behavioral Patterns](#23-behavioral-patterns)

These patterns are concerned with algorithms and the assignment of responsibilities between objects.

| Pattern | Description |
|---------|-------------|
| Chain of Responsibility | Passes requests along a chain of handlers. Upon receiving a request, each handler decides either to process the request or to pass it to the next handler in the chain |
| [Command](https://refactoring.guru/design-patterns/command) | Turns a request into a stand-alone object that contains all information about the request |
| [Iterator](https://refactoring.guru/design-patterns/iterator) | Lets you traverse elements of a collection without exposing its underlying representation |
| [Mediator](https://refactoring.guru/design-patterns/mediator) | Reduces chaotic dependencies between objects by restricting direct communications between the objects and forcing them to collaborate only via a mediator object |
| [Memento](https://refactoring.guru/design-patterns/memento) | Lets you save and restore the previous state of an object without revealing the details of its implementation |
| [Observer](https://refactoring.guru/design-patterns/observer) | Defines a subscription mechanism to notify multiple objects about any events that happen to the object they're observing |
| [State](https://refactoring.guru/design-patterns/state) | Lets an object alter its behavior when its internal state changes |
| [Strategy](https://refactoring.guru/design-patterns/strategy) | Lets you define a family of algorithms, put each of them into a separate class, and make their objects interchangeable |
| [Template Method](https://refactoring.guru/design-patterns/template-method) | Defines the skeleton of an algorithm in the superclass but lets subclasses override specific steps of the algorithm without changing its structure |
| [Visitor](https://refactoring.guru/design-patterns/visitor) | Lets you separate algorithms from the objects on which they operate |

### 3. Real World System Design Case Studies

| System | Reference Links |
|--------|-----------------|
| Facebook Priority Queue | [Engineering Blog Post](https://engineering.fb.com/2021/02/22/production-engineering/foqs-scaling-a-distributed-priority-queue/) |
| Google File System | [Research Paper](https://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf)<br>[YouTube Video](https://www.youtube.com/watch?v=LXhgFAZroG8) |
| Memcache |[Research Paper](https://research.facebook.com/publications/scaling-memcache-at-facebook/) |
| Kafka | [Notes on Kafka](https://notes.stephenholiday.com/Kafka.pdf) |
| Shard Manager | [Engineering Blog Post](https://engineering.fb.com/2020/08/24/production-engineering/scaling-services-with-shard-manager/)<br>[Research Paper](https://research.facebook.com/publications/shard-manager-a-generic-shard-management-framework-for-geo-distributed-applications/)<br>[YouTube Video](https://www.youtube.com/watch?v=OMI52r-thFA&t=43s) |
| AWS S3 | [YouTube Video 1](https://www.youtube.com/watch?v=v3HfUNQ0JOE)<br>[YouTube Video 2](https://www.youtube.com/watch?v=qJoATSh5CZY) |
| AWS Lambda | [YouTube Video](https://www.youtube.com/watch?v=0_jfH6qijVY) |

### 4. System Concepts

#### 4.1. [Protocols](#41-protocols)

#### 4.2. [Deployment Patterns](#42-deployment-patterns)

#### 4.3. [Load Balancing Patterns](#43-load-balancing-patterns)

### 5. System Components

---

## References

This repository compiles information from various authoritative sources in the field of system design. Key references include:

1. Microsoft Azure Architecture Center. (n.d.). Cloud Design Patterns. https://learn.microsoft.com/en-us/azure/architecture/patterns/

2. Shvets, A. (n.d.). Design Patterns. Refactoring.Guru. https://refactoring.guru/design-patterns

3. Facebook Engineering. (n.d.). Engineering Blog. https://engineering.fb.com/

4. Google Research. (n.d.). Publications. https://research.google/pubs/

5. Amazon Web Services. (n.d.). AWS Architecture Blog. https://aws.amazon.com/blogs/architecture/

6. Martin, R. C. (2000). Design Principles and Design Patterns. ObjectMentor.

7. Kleppmann, M. (2017). Designing Data-Intensive Applications. O'Reilly Media.

8. Fowler, M. (2002). Patterns of Enterprise Application Architecture. Addison-Wesley.

This list is not exhaustive, and we acknowledge all the researchers, authors, and organizations that have contributed to the field of system design. For specific attributions or additional references, please refer to the individual sections or open an issue.
