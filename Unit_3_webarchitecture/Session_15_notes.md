## 15th Session: Web Architecture: Scalability and Latency

## What is Scalability?

- Scalability means the application’s ability to handle and withstand increased workload without sacrificing performance

## What is Latency?

- The time it takes for your application to respond to a users request
- If the latency remains the same, we can say that the application scaled well with the increased load and is highly scalable
- Latency is measured as the time difference between the action that a user takes on the website and the systems response in reaction to that action.
- Divided into two parts: Network latency and Application latency

## Network latency

- Time that the network takes to send a data packet from point A to point B
- To cut down the network latency, businesses use a *CDN* (Content Delivery Network) to deploy their servers across the globe as close to the end-user as possible.
- These close to the user locations are also known as *Edge* locations.

## Application latency

- Time it takes the application to process a user request (eg a user sends request to the database)
- There are more than a few ways to cut down the application latency. The first step is to run *stress*
 and *load tests* on the application and scan for the *bottlenecks* that slow down the system as a whole.

## Types of Scalability

- Vertical Scaling
- Horizontal Scaling


### **Vertical Scaling (scaling up)**

- adding more power (eg CPU, RAM) to an exisiting machine (server)
- adding more power to your server eg from 16gb to 32gb of ram

**Pros** 

- simpler than horizontal code as you do not need to refactor code or make any complex system configurations

**Cons**

- Availabilty risk - just one server which there is a risk of the server going down and the webiste going offline

### **Horizontal Scaling (scaling out)**

- adding more hardware/machines to your pool of resources
- splits the workload across multiple servers that work in parallel.

**Pros** 

- no limit to augmenting the hardware capacity
- Data is replicated across different geographical regions as nodes and data center are setup across the globe

**Cons**

- Cost with adding more hardware - not cost efficient

### **Dynamic Scaling**

- Resources scale up and down as traffic spikes occur

### Which scalability approach is right for our app

- If app is a utility or tool expected to recieve minimal predictable traffic then a single server is enough to manage the traffic, so we can go ahead with vertical scaling when we know the traffic load will not spike in the future

- If you app is a public-facing social app where the traffic is unpredictable. Both high-availability and traffic is important. Best to build an app that can be deployed on the cloud.

### High availability

- High Availability refers to a system (a network, a server array or cluster, etc.) that is designed to be available 99.999% of the time, or as close to it as possible. Usually this means configuring a failover system that can handle the same workloads as the primary system.
- High availability can be achieved only with thorough planning and consistent monitoring.

### Fault tolerance

- Fault tolerance refers to the ability of a system (computer, network, cloud cluster, etc.) to continue operating without interruption when one or more of its components fail.
- **Guaranteeing Zero down-time** despite the system taking a hit
- Implemented using a Microservice

The difference between fault tolerance and high availability, is this: **A fault tolerant environment has no service interruption but a significantly higher cost, while a highly available environment has a minimal service interruption**.

### Redundnacy

- duplicating the server instances and keeping them on standby to take over in case any of the active server instances fo down
- Used to maintain high availability

### Load balancing

- Load balancing is used to distribute the workload between different servers
- distribute

### Database

- component in application architecture required to persist data
- Data can be in many forms: structured, unstructured and semi-structured

**Structured data** 

- Typically managed by a query language such as structured query language (SQL)
- SQL databases have a pre-defined schema for defining and manipulating data.
- SQL databases are table-based and relational (has a relationship)
- All of your data must follow the same structure, its good for complex queries but it might be too restrictive
- If you need to change the structure of your data it might be difficult
- You’re able to increase the load on a single server by adding more CPU, RAM, or SSD capacity (**vertical scaling**)
- Eg MySQL, Oracle, PostgreSQL

**Unstructured data** 

- data that is not structured via predefined data model or schems
- may be textual or non-textual, and human- or machine-generated
- eg text files, images, video files
- may also be stored within a non-relational database like NoSQL.

- NoSQL databases are document, key-value, graph, or wide-column stores and are non-relational
- You’re able to handle higher traffic by sharding, which adds more servers to your NoSQL database (**horizontally scalable)**
- Eg MongoDB

## What are relationships?

- A relationship is established between two database tables when one table uses a foreign key that references the primary key
of another table.

### Types of Database relationships

### One-to-One

- This type of relationship allows only one record on each side of the relationship. The primary key relates to only one record (or none) in another table.
- it associates a row from a parent table to multiple rows in a child table.

### One-to-Many (1:N)

- A one-to-many relationship allows a single record in one table to be related to multiple records in another table.
- requires the child table Primary Key to be associated via a Foreign Key with the parent table Primary Key column.

### Many-to-Many

- This is a complex relationship in which many records in a table can link to many records in another table
- requires a link table containing two Foreign Key columns that reference the two different parent tables.

## Caching

- Caching is key to the performance of any kind of application.
- It ensures low latency and high throughput.
- An application with caching will undoubtedly do better than an application without caching, simply because a cache intercepts all the requests darting towards the database and provides the response in no time.