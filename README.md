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
    4. [API Strategy](#44-api-strategy)
    5. [Real Used System Algorithm](#45-real-used-system-algorithm)
    6. [Rate Limit strategy](#46-rate-limit-strategy)
    7. [Caching Strategy](#47-caching-strategy)
    8. [Deployment Strategy](#48-deployment-strategy)
    9. [System Problems](#49-system-problems)
    10. [Concurrency](#410-concurrency)

5. [System Components](#5-system-components)
    1. [Databases](#51-databases)
    2. [Queues](#52-queues)
    3. [Cache](#53-cache)
    4. [Load Balancers](#54-load-balancers)
    5. [File Systems](#55-file-systems)
    6. [Data Processing](#56-data-processing)

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

### 4. Various System Concepts

#### 4.1. [Protocols](#41-protocols)

| Protocol/Technology | Definition | Pros | Cons |
|---------------------|------------|------|------|
| HTTP | Hypertext Transfer Protocol, the foundation of data communication on the web. | - Simple and widely adopted<br>- Stateless, improving scalability | - Limited performance optimizations<br>- Each request is independent, leading to potential inefficiencies |
| HTTP/1.1 | An improved version of HTTP that supports persistent connections and chunked transfer. | - Supports multiple requests over a single connection<br>- Enhanced caching mechanisms | - Still suffers from head-of-line blocking<br>- Text-based, leading to larger message sizes |
| HTTP/2 | A binary protocol designed to improve performance with features like multiplexing and server push. | - Reduces latency with multiplexing<br>- Header compression reduces overhead<br>- Server push improves load times | - More complex implementation<br>- Not universally supported by all browsers and servers |
| HTTPS | HTTP over SSL/TLS, providing secure communication over a computer network. | - Encrypts data for security<br>- Widely trusted and accepted standard for secure communication | - Slightly increased overhead due to encryption<br>- Requires SSL/TLS certificates |
| HLS (HTTP Live Streaming) | A streaming protocol that delivers content in small chunks over HTTP. | - Adaptive bitrate streaming adjusts quality based on network conditions<br>- Wide compatibility with devices | - Higher latency compared to other streaming protocols<br>- Requires HTTP server support |
| DASH (Dynamic Adaptive Streaming over HTTP) | A streaming protocol similar to HLS but standardized by MPEG. | - Supports adaptive bitrate streaming<br>- Can work with any HTTP server | - Complexity in implementation<br>- May require more sophisticated client-side handling |
| ABR (Adaptive Bit Rate) | A technique that adjusts the quality of a video stream in real-time based on the user's bandwidth. | - Provides optimal viewing experience regardless of network conditions<br>- Reduces buffering | - Requires robust encoding and streaming infrastructure<br>- Can lead to quality fluctuations |
| TLS / SSL | Protocols for securing communications over a computer network. | - Provides confidentiality, integrity, and authentication<br>- Essential for secure web transactions | - Increased processing overhead<br>- Complexity in certificate management |
| SSE (Server-Sent Events) | A standard allowing servers to push updates to the client over HTTP. | - Simple to implement<br>- Automatic reconnection and event-driven model | - Unidirectional (server to client only)<br>- Limited browser support compared to WebSockets |

#### 4.2. [Deployment Patterns](#42-deployment-patterns)

#### 4.3. [Load Balancing Patterns](#43-load-balancing-patterns)

| Strategy Name | Definition | Pros | Cons |
|---------------|------------|------|------|
| Active/Active | Multiple servers actively handle requests simultaneously, distributing the load across all. | - Maximizes resource utilization.<br>- Provides redundancy and fault tolerance.<br>- Enhances performance for high-traffic applications. | - More complex to manage.<br>- Requires careful synchronization of session states. |
| Active/Passive | One server handles requests while others remain on standby, taking over if the active server fails. | - Simpler to implement than active/active.<br>- Easier to manage session states. | - Underutilizes resources during normal operation.<br>- Failover can introduce latency. |
| Round Robin | Requests are distributed sequentially across available servers in a circular manner. | - Simple to implement.<br>- Ensures even distribution of requests. | - Does not account for server load differences.<br>- May not be effective for uneven workloads. |
| Weighted Round Robin | Similar to round robin but assigns weights to servers based on their capacity. | - Optimizes resource utilization by directing more requests to powerful servers. | - Requires careful weight management.<br>- Complexity increases with more servers. |
| Least Connections | Directs requests to the server with the fewest active connections. | - Adapts to real-time server load.<br>- Prevents overloading of any single server. | - May not be ideal for long-lived connections.<br>- Assumes connection count reflects load. |
| Least Response Time | Routes requests to the server with the quickest response time. | - Minimizes latency for end users.<br>- Improves user experience in latency-sensitive applications. | - Requires continuous monitoring of response times.<br>- May lead to uneven load distribution. |
| IP Hash | Uses the client's IP address to determine which server will handle the request. | - Ensures session persistence for clients.<br>- Simple to implement for session-based applications. | - Distribution quality depends on client IP diversity.<br>- Does not adapt to server load changes. |
| Content-Based Routing | Routes requests based on the content of the request, such as URL or request type. | - Allows for tailored routing based on application needs.<br>- Can optimize resource usage. | - More complex to implement.<br>- Requires understanding of request content. |

#### 4.4. [API Strategy](#44-api-strategy)

| Strategy Name | Definition | Pros | Cons |
|---------------|------------|------|------|
| Short Polling | The client repeatedly sends requests to the server at regular intervals. | - Simple implementation using standard HTTP requests.<br>- Immediate response to clients. | - High network traffic due to frequent requests.<br>- Potential latency in updates.<br>- Increased server load. |
| Long Polling | The client sends a request and the server holds it until new data is available. | - Reduces network traffic compared to short polling.<br>- Enables real-time updates. | - Potential timeout issues.<br>- Increased server resource usage.<br>- More complex error handling. |
| WebSockets | A persistent connection allowing full-duplex communication between client and server. | - Low-latency communication suitable for real-time applications.<br>- Efficient data transfer without repeated HTTP overhead. | - More complex implementation.<br>- Potential issues with firewalls or proxies.<br>- Requires careful resource management. |
| Server-Sent Events (SSE) | A server-side technology that allows servers to push updates to the client over HTTP. | - Simple to implement and use with existing HTTP infrastructure.<br>- Automatic reconnection. | - Unidirectional communication (server to client only).<br>- Limited browser support compared to WebSockets. |
| gRPC | A high-performance RPC framework that uses HTTP/2 for transport. | - Supports multiple programming languages.<br>- Efficient binary serialization (Protocol Buffers).<br>- Built-in authentication and load balancing. | - More complex setup.<br>- Requires knowledge of Protocol Buffers.<br>- Not as widely adopted as REST. |
| REST | An architectural style that uses standard HTTP methods for communication. | - Simple and widely understood.<br>- Stateless operations improve scalability.<br>- Easy to cache responses. | - Limited real-time capabilities.<br>- Overhead of HTTP headers in each request.<br>- Can become complex with multiple endpoints. |
| GraphQL | A query language for APIs that allows clients to request specific data. | - Clients can request exactly what they need.<br>- Reduces over-fetching and under-fetching of data.<br>- Strongly typed schema. | - More complex to implement.<br>- Requires additional tooling for caching.<br>- Potential for performance issues with complex queries. |

#### 4.5. [Real Used System Algorithm](#45-real-used-system-algorithm)


| Data Structure/Algorithm | Definition | Pros | Cons |
|--------------------------|------------|------|------|
| Count-Min Sketch | A probabilistic data structure used for estimating the frequency of events in a data stream. | - Space-efficient for large data streams<br>- Allows for quick frequency estimation | - Provides approximate results with possible errors<br>- Cannot delete items once added |
| Bloom Filters | A space-efficient probabilistic data structure used to test whether an element is a member of a set. | - Very low memory usage<br>- Fast membership checks<br>- Reduces unnecessary database queries | - Can produce false positives (indicating an element is present when it is not)<br>- Cannot remove elements |
| Simple Hashing | A technique to distribute data across a fixed number of buckets using a hash function. | - Simple and fast data retrieval<br>- Easy to implement | - Poor distribution can lead to collisions<br>- Not suitable for dynamic datasets |
| Consistent Hashing | A hashing scheme that minimizes the movement of keys when nodes are added or removed. | - Efficiently handles dynamic changes in the system<br>- Reduces rehashing overhead | - More complex than simple hashing<br>- Requires careful implementation to avoid hotspots |
| HyperLogLog | A probabilistic algorithm for estimating the cardinality of a multiset. | - Extremely space-efficient for counting unique items<br>- Suitable for large datasets | - Provides approximate counts with errors<br>- More complex to implement than basic counting |
| CRDT Distributed Counter | A data structure that allows for concurrent updates without conflicts in a distributed system. | - Supports eventual consistency<br>- Allows for concurrent updates without locking | - More complex to implement<br>- Potentially higher memory usage |
| Geo Hash | A method for encoding latitude and longitude coordinates into a compact string representation. | - Efficiently represents geographic data<br>- Supports spatial queries and indexing | - Limited precision depending on the length of the hash<br>- Can lead to clustering of nearby points |
| Quad Tree | A tree data structure used to partition a two-dimensional space by recursively subdividing it into four quadrants. | - Efficient for spatial indexing and querying<br>- Good for representing sparse data | - Can become inefficient with dense data<br>- More complex to implement than simpler structures |
| Rate Limit Algorithms | Techniques used to control the rate of requests sent to a server to prevent overload. | - Protects server resources<br>- Ensures fair usage among users | - Can lead to user frustration if limits are too strict<br>- Requires careful tuning |
| Trie | A tree-like data structure that stores a dynamic set of strings, often used for autocomplete features. | - Fast prefix-based searching<br>- Efficient memory usage for large datasets with common prefixes | - Can consume a lot of memory for large datasets<br>- More complex to implement than hash tables |
| Raft/Paxos | Consensus algorithms used to achieve agreement among distributed systems. | - Provides strong consistency guarantees<br>- Fault-tolerant and resilient to failures | - More complex to implement<br>- Can have performance overhead in high-latency networks |
| Kalman filter | | | |
| Markov Chain | | | |
| hilbert curve | | | |

#### 4.6. [Rate Limit strategy](#46-rate-limit-strategy)

| Strategy Name | Definition | Pros | Cons |
|---------------|------------|------|------|
| User Rate Limiting | Limits the number of requests a user can make in a specified time frame. | Simple to implement; prevents individual users from monopolizing resources. | May not account for legitimate burst traffic from users. |
| Concurrency Rate Limiting | Restricts the number of simultaneous sessions a user can maintain. | Helps mitigate DDoS attacks; ensures fair resource allocation among concurrent users. | Can be complex to manage in highly dynamic environments. |
| Location-Based Rate Limiting | Applies limits based on geographical location or demographics. | Useful for targeted campaigns and improving service availability in specific regions. | May inadvertently block legitimate users from outside the target area. |
| Server Rate Limiting | Limits requests to specific servers, ensuring balanced load across multiple servers. | Protects critical servers from overload; enhances overall system stability. | Can lead to underutilization of resources if not properly configured. |
| Token Bucket | Users have a "bucket" that fills with tokens over time; each request consumes a token. | Supports burst traffic; efficient resource usage and easy to implement. | Requires careful tuning of token refill rates and bucket sizes to avoid abuse. |
| Leaky Bucket | Requests are processed at a steady rate, regardless of incoming burst traffic. | Provides consistent request handling; smoothens traffic spikes effectively. | Can lead to delays for legitimate users during high traffic periods. |
| Fixed Window Counter | Counts requests in fixed time windows, resetting after each window ends. | Simple implementation; low memory usage per user. | Can allow excessive requests if timed perfectly at the window boundaries (e.g., 100 requests at 10:00:59 and another 100 at 10:01:01). |
| Sliding Window Log | Tracks each request timestamp in a log, allowing for more granular control over request limits. | Provides precise control over request rates; minimizes burst effects on overall limits. | Higher memory usage and complexity in managing the log data structure. |

#### 4.7. [Caching Strategy](#47-caching-strategy)

| Strategy Name | Definition | Pros | Cons |
|---------------|------------|------|------|
| Cache Aside | The application checks the cache first; if the data is not present, it fetches from the database and stores it in the cache. | - Simple to implement.<br>- Reduces load on the database.<br>- Allows for lazy loading. | - Potential for cache misses.<br>- Increased latency on cache misses. |
| Read Through | The cache fetches data from the database if it is not present in the cache, acting as the source of truth. | - Ensures data is always available in the cache.<br>- Reduces cache misses. | - Increased complexity.<br>- Higher latency on cache misses. |
| Write Around | Data is written directly to the database, bypassing the cache, which is updated asynchronously. | - Reduced risk of cache inconsistency.<br>- Lower write latency. | - Potential for cache misses on subsequent reads.<br>- Increased load on the database. |
| Write Back | Data is written to the cache first, with asynchronous writing to the database occurring in the background. | - Lower write latency.<br>- Reduced load on the database. | - Increased complexity.<br>- Risk of data loss if the cache fails before writing to DB. |
| Write Through | Data is written to both the cache and the database simultaneously, with I/O completion confirmed for both. | - Ensures data consistency between cache and database.<br>- Simple to understand. | - Higher write latency.<br>- Increased load on the database. |

#### 4.8. [Deployment Strategy](#48-deployment-strategy)

| Strategy Name | Definition | Pros | Cons |
|---------------|------------|------|------|
| Blue-Green Deployment | This pattern involves maintaining two identical production environments, referred to as "blue" and "green." Only one environment is live at any time, allowing for seamless updates and quick rollback if issues arise during deployment. | - Reduces downtime and risk of service disruption.<br>- Allows for quick rollback if issues arise during deployment. | - Requires maintaining two identical environments.<br>- Increases operational overhead. |
| Canary Deployment | In this strategy, a new version of the application is rolled out to a small subset of users before a full-scale deployment. This allows teams to monitor the new version for issues and gather feedback before wider release. | - Allows for controlled testing of new versions.<br>- Helps in gathering user feedback before full deployment. | - Requires careful user selection and monitoring.<br>- May not be suitable for all types of applications. |
| Rolling Deployment | This method gradually replaces instances of the previous version of the application with the new version. It minimizes downtime as the deployment occurs in phases across the infrastructure. | - Reduces downtime and risk of service disruption.<br>- Allows for continuous service availability. | - Requires careful planning and execution.<br>- Can be complex to manage in large-scale deployments. |
| Recreate Deployment | This pattern involves stopping the old version of the application and then starting the new version. While simple, it can lead to downtime as there is no overlap between the old and new versions. | - Simple to implement.<br>- Ensures a clean start with the new version. | - Leads to downtime during deployment.<br>- Potential for initial confusion among users. |
| A/B Testing | This approach involves deploying two versions of an application (A and B) to different user groups to compare performance and user engagement. This helps in making data-driven decisions about which version to adopt fully. | - Allows for direct comparison of different versions.<br>- Helps in making data-driven decisions. | - Requires careful user segmentation and monitoring.<br>- Increases operational overhead. |
| Shadow Deployment | In shadow deployment, the new version of an application runs alongside the old version, but only receives a copy of the production traffic. This allows for testing without impacting the user experience. | - Allows for testing without affecting production traffic.<br>- Helps in gathering user feedback before full deployment. | - Requires careful configuration and monitoring.<br>- May not be suitable for all types of applications. |
| Microservices Deployment | This pattern emphasizes deploying small, independently deployable services that communicate over a network. Each service can be updated and scaled independently, enhancing flexibility and resilience. | - Enhances flexibility and scalability.<br>- Allows for independent updates and scaling. | - More complex to manage and coordinate.<br>- Requires careful orchestration. |
| Serverless Deployment | This pattern allows developers to deploy applications without managing the underlying infrastructure. Functions are executed in response to events, automatically scaling as needed. | - Simplifies infrastructure management.<br>- Reduces operational overhead. | - May not be suitable for all types of applications.<br>- Can be less flexible for certain use cases. |
| Event-Driven Deployment | This approach leverages events to trigger deployments and updates, allowing for more dynamic and responsive systems that react to changes in real-time. | - Enhances responsiveness and adaptability.<br>- Reduces manual intervention. | - More complex to implement and manage.<br>- Requires careful event handling and integration. |
| Immutable Deployment | In this pattern, once an application version is deployed, it is never modified. Any updates involve deploying a new version, ensuring consistency and reducing the risk of configuration drift. | - Ensures consistency and reduces configuration drift.<br>- Simplifies deployment process. | - Requires careful version management and potential for increased deployment frequency. |

#### 4.9. [System Problems](#49-system-problems)

| Problems | Explanation |
|----------|-------------|
| Noisy Neighbour | A single tenant or application consumes disproportionate resources (like CPU, memory, or bandwidth), negatively impacting the performance of other tenants sharing the same infrastructure. Solutions often involve resource allocation strategies, workload prioritization, and monitoring to mitigate the effects of one tenant's resource hogging. |
| Thundering Herd | Many processes or threads attempt to access a shared resource simultaneously, leading to contention and performance degradation. Techniques like exponential backoff or implementing a queuing mechanism can help alleviate this issue. |
| Cache Stampede | Multiple requests for the same resource hit a cache simultaneously, causing a surge in load on the backend system when the cache misses. Strategies such as request coalescing or using a locking mechanism to ensure only one request populates the cache can be employed. |
| Load Imbalance | The distribution of workload across servers or nodes is uneven, leading to some resources being overutilized while others remain underutilized. Dynamic load balancing algorithms that redistribute tasks based on current load metrics can help address this problem. |
| Split-Brain Syndrome | Network partitions lead to multiple nodes believing they are the primary node, resulting in conflicting operations and data inconsistencies. Consensus algorithms like Paxos or Raft can help maintain a single source of truth. |
| Resource Starvation | One or more processes are perpetually denied the resources they need to proceed because other processes are continuously consuming those resources. Implementing fair scheduling algorithms and resource quotas can help mitigate this issue. |
| Latency Issues | Delays in data transfer or processing, often due to network congestion or inefficient data handling. Techniques to reduce latency include optimizing data paths, using content delivery networks (CDNs), and implementing caching strategies. |

#### 4.10. [Concurrency](#410-concurrency)

| Concurrency | |
|-------------|-------------|
| Concurrency | https://www.youtube.com/watch?v=wEsPL50Uiyo |
| Preventing Read Committed SQL Concurrency Errors | https://on-systems.tech/blog/128-preventing-read-committed-sql-concurrency-errors/ |
| Preventing Read Committed SQL Concurrency Errors | https://on-systems.tech/blog/128-preventing-read-committed-sql-concurrency-errors/ |
| PostgreSQL Anti-Patterns: Read Modify Write Cycles | https://www.2ndquadrant.com/en/blog/postgresql-anti-patterns-read-modify-write-cycles/ |
| Distributed Transaction | https://www.youtube.com/watch?v=S4FnmSeRpAY&t=1s |
| Distributed Transaction | https://www.youtube.com/watch?v=4EajrPgJAk0 |
| PostgreSQL Isolation Levels | https://www.postgresql.org/docs/current/transaction-iso.html |

### 5. System Components

#### 5.1. [Databases](#51-databases)

| Database | Description |
|----------|-------------|
| MongoDB | |
| MySQL | |
| PostgreSQL | |
| DynamoDB | |
| Cassandra | |

#### 5.2. [Queues](#52-queues)

| Queue | Description |
|-------|-------------|
| Kafka | |
| RebbitMQ | |
| SQS | |


#### 5.3. [Cache](#53-cache)

| Cache | Description |
|-------|-------------|
| Redis | |
| MemCache | |
| CDN | |
| Open Connect | |

#### 5.4. [Load Balancers](#54-load-balancers)

| Load Balancer | Description |
|---------------|-------------|
| L4 | |
| L7 | |


### Coordination Services

| Coordination Service | Description |
|-----------------------|-------------|
| ETCD | |
| Apache zookeeper | |

#### 5.5. [File Systems](#55-file-systems)

| File System | Description |
|-------------|-------------|
| hdfs | |
| s3 | |

#### 5.6. [Data Processing](#56-data-processing)

| Data Processing | Description |
|-----------------|-------------|
| Map Reduce | |
| Hadoop | |

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




