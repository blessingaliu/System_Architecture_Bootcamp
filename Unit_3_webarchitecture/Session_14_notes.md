## 14th Session: Web Architecture: Application layers

## Single-tier applications

One Tier application AKA Standalone application

- you build and ship it to users

One-tier architecture has all the layers such as Presentation, Business, Data Access layers in a single software package. Applications that handle all the three tiers such as MP3 player, MS Office come under the one-tier application. The data is stored in the local system or a shared drive.

**Advantages**

- low latency (time it takes for a server request to get a response) - because all of the layers are in the same machine

**Disadvantages**

- Publishers have no control over single-tier applications, once shipped no code or feature updates can be made until the customer does so by connecting to a remote server
- The code in a single-tier applications is also vulnerable to being tweaked and reverse engineered
- Single-tier applications performace look and feel can be inconsistent as the app rending largely depends on the configuration of the user’s machine

----------

## Two-tier applications

- Involves a client and a server

The Two-tier architecture is divided into two parts:

1. Client Application (Client Tier)

2. Database (Data Tier)

The client system handles both Presentation and Application layers and the Server system handles the Database layer. It is also known as a client-server application. The communication takes place between the Client and the Server. The client system sends the request to the server system and the Server system processes the request and sends back the data to the Client System. 

**Advantages:**

1. Easy to maintain and modification is bit easy
2. Communication is faster

**Disadvantages**:

1. In two tier architecture application performance will be degrade upon increasing the users.
2. Cost-ineffective

----------


## Three-tier applications

- Involves a client, server and a database
- The 3 different layers are physically separated

**Three-tier architecture** typically comprise a presentation tier, a business or data access tier, and a data tier. Three layers in the three tier architecture are as follows:

**1) Client layer**

**2) Business layer**

**3) Data layer**

**1) Client layer:**

It is also called as *Presentation layer* which contains UI part of our application. This layer is used for the design purpose where data is presented to the user or input is taken from the user. For example designing registration form which contains text box, label, button etc.

**2) Business layer:**

In this layer all business logic written like validation of data, calculations, data insertion etc. This acts as a interface between Client layer and Data Access Layer. This layer is also called the intermediary layer helps to make communication faster between client and data layer.

**3) Data layer:**

In this layer actual database is comes in the picture. Data Access Layer contains methods to connect with database and to perform insert, update, delete, get data from database based on our input data.

**Advantages**

1. High performance, lightweight persistent objects
2. Scalability – Each tier can scale horizontally
3. Performance – Because the Presentation tier can cache requests, network utilization is minimized, and the load is reduced on the Application and Data tiers.
4. High degree of flexibility in deployment platform and configuration
5. Better Re-use
6. Improve Data Integrity
7. Improved Security – Client is not direct access to database.
8. Easy to maintain and modification is bit easy, won’t affect other modules
9. In three tier architecture application performance is good.

**Disadvantages**

1. Increase Complexity/Effort

----------

## N-tier applications

- Application that has more than three components (user interface, backend server, database) involved in its architecture

### What are those components?

- cache
- message queues for asynchronous behaviour
- load balancers (process of distributing network traffic across multiple servers)
- search servers
- components involved in processing massive amount of data
- components running heterogenous tech community known as web services, microservices


----------


## REST API

- **REST**, short for **Representational State Transfer**, is a comprehensive network-based architectural style. (design standards)
- A RESTful API is an architectural style for an application program interface ([API](https://www.techtarget.com/searchapparchitecture/definition/application-program-interface-API)) that uses the REST Architectural style and uses HTTP requests to access and use data
- That data can be used to GET, PUT, POST and DELETE data types, which refers to the reading, updating, creating and deleting of operations concerning resources.

**An API for a website is [code](https://www.techtarget.com/whatis/definition/code) that allows two software programs to communicate with each other.** API is some code that you didn’t write yourself, and that code has some methods that you are allowed to call. It could be something that you download and run from your computer or it could be something that’s someplace else on the web.

- API is a way people can access the data from your code backend

- GET `/type`: Get to retrieve all resources
- POST `/type`: Create a new item of a type.
- GET `/type/id`: Get a specific item of a type.
- PUT `/type/id`: Update an existing item of a type.
- DELETE `/type/id`: Delete an existing item of a type.

A RESTful API -- also referred to as a RESTful web service or REST API -- is based on representational state transfer ([REST](https://www.techtarget.com/searchapparchitecture/definition/REST-REpresentational-State-Transfer)), which is an architectural style and approach to communications often used in [web services](https://www.techtarget.com/searchapparchitecture/definition/Web-services) development.

----------


## Different types of servers

## A Good Web Architecture should:

- Avoid frequent crashes (spikes in number of users)
- Be able to scale up or down easily
- Be simple to use
- Have a faster response time
- Have automated deployments
- Log errors
- Not have a single point of failure
- Solve the query in a consistent and uniform manner
- Support the latest standards and technologies
- Utilize strengthened security measures to lessen the chance of malicious intrusions

# **Here are 5 benefits of separating an application into 3 tiers:**

1. It gives you the ability to update the technology stack of one tier, without impacting other areas of the application.
2. It allows for different development teams to each work on their own areas of expertise. Today’s developers are more likely to have deep competency in one area, like coding the front end of an application, instead of working on the full stack.
3. You are able to scale the application up and out. A separate back-end tier, for example, allows you to deploy to a variety of databases instead of being locked into one particular technology. It also allows you to scale up by adding multiple web servers.
4. It adds reliability and more independence of the underlying servers or services.
5. It provides an ease of maintenance of the code base, managing presentation code and business logic separately, so that a change to business logic, for example, does not impact the presentation layer.

Thick clients utilise more of their local resources like processing power, memory and storage when used, whilst thin client utilise more of the resources of the remote servers they connect to.