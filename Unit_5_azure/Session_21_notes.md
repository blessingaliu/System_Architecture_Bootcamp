## 21th Session: Microservices

### What is Ubiquitous language?
- language bound to the specific context

This is a shared common vocabulary that the entire team involved in a project, from stakeholders, to developers. This is to reduce the ambiguity of communication, part of Domain Driven Design (DDD)

+ clear communication 
+ creating a beneficial feedback loop
+ common language 


### Domains and Sub-Domains  
Domain knowledge is knowledge of specific, specialised discipline in constrast to general knowledge, or domain-independent knowledge.

eg a specific industry like Education, Banking, IT

Sub-domains are areas where domains are decomposed into to ease modelling and comprehension.

### Bounded context
A bounded context is a logical boundary. it defines some tangible boundary between sub-domains.

A description of a boundary (typically a subsystem, or the work of a particular team) within which a particular model is defined and applicable.

- we want to keep our bounded context decoupled

### Implementation

#### Entity
Entity = has attributes of continuity and identity.
This is an object primarily defined by its specific identity, it's usually something you have to keep track over time.

#### Value Object
A Value object is an object that doesn't have a conceptual identity but is just describing some characteristics of a thing. Characteristics of a Value Object:

- It measures, quantifies or describes a thing in the domain 
- It is immutable, meaning that its state cannot be changed after creation.
- It is comparable to others using value equality.
- Its behavior is side-effect free.

#### Aggregation
This is a special type of association in which objects are assembled or configured together to create a more complex object. An aggregation describes a group of objects and how you interact with them.


### Monolithic architecture explained 
- Monolithic applications are built with each components (presentation, application logic and database) corresponding to a single functionality, each components are combined into one single machine. If one of the components stops working, the whole system fails.

- All the components are too dependent on each other, if any component fails, the whole application crashes.

- It is very hard to scale a monolithic application, it is also hard to deploy and difficult to switch to another programming language.


### Microservices architecture explained 
- A microservice is an application composed of independent services that can run independently and scale freely on different servers

- The main advantage of microservices is that they are easy to reconfigure for different purposes
- Rapid deployment
- fault tolerance
- horizontal scaling
- low barrier to entry

#### How Microservices work
Microservices architecture is a collection of services that communicate with each other via APIs.

- each component is built using the specific languages/frameworks necessary for the functionality
- Microservices architectures are enabled by :
containerization technology (Docker)
container orchestration tools (Kubernetes)
cloud computing
API gateways 