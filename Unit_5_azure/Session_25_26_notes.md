## 25th Session and 26th Session: Azure Fundamentals: Serverless and Containers

### What is Cloud native and why?

A cloud-native application is a program that is designed for a cloud computing architecture. It was deisgned to reside in the cloud from the start.

Example of common cloud native scenarios 
- SaaS delivery
- Real-time telemetry 
- AI powered applications 
- Run applications anywhere 
- Geo-distributed applications 


### What do customers use cloud native for?

**Predictable**
Cloud native apps conform to a framework or “contract” designed to maximize resilience through predictable behaviors. The automated, container-driven infrastructure used in cloud platforms drives the way software is written. A good example of such a “contract” is illustrated by the 12 principles first documented as the 12-factor app.

**OS abstraction**
A cloud native architecture gives developers a means of abstracting away underlying infrastructure dependencies. Instead of configuring, patching, and maintaining operating systems, teams focus on software. The most efficient means of abstraction is a formalized platform.

**Collaborative**
Cloud native architecture facilitates DevOps, a combination of people, process, and tools that increases collaboration between development and operations teams to speed and smooth the transfer of finished application code into production.

**Continuous delivery**
IT teams make individual software updates available for release as soon as they are ready. Organizations that release software rapidly get a tighter feedback loop and can respond more effectively to customer needs. Continuous delivery works best with other related approaches including test-driven development and continuous integration.

**Independent**
Microservices architecture decomposes applications into small, loosely coupled, independently operating services. These services map to smaller, independent development teams and make possible frequent updates, scaling, and failover/restart without impacting other services.

**Automated scalability**
Infrastructure automation at scale eliminates downtime due to human error, consistently applying the same set of rules across any size deployment. Cloud native also goes beyond the ad-hoc automation built on top of traditional virtualization-oriented orchestration. A fully cloud native architecture is about automating systems, not servers.	

**Rapid recovery**
The container runtime and orchestrator provides a dynamic, high-density virtualization overlay, ideally matched to the microservices architecture. Orchestration dynamically manages placement of containers across a cluster to provide elastic scaling and recovery/restart in the event of app or infrastructure failure.	

### Cloud Native solution Components 

Containers, service meshes, microservices, immutable infrastructure, and declarative APIs exemplify this approach.

#### Infrastructure as Code (IaaC)
This is the process of managing and provisioning infrastructure through code instead of through manual processes. It acts as a ‘template’ that makes deploying new applications much faster.

#### Containers
Containers are the smallest compute unit in a cloud-native application. They help to package application code with the operating systems and dependent libraries, which can be run in any environment. This means that cloud-native applications can be deployed on premises, on cloud infrastructure or on hybrid cloud. Due to the lightweight nature of containers, they can be scaled quickly compared to regular virtual machines.  Developers use containers for packaging the microservices with their respective dependencies, such as the resource files, libraries, and scripts that the main application requires to run.


#### Immutable infrastructure 
Immutable infrastructure means that the servers for hosting cloud-native applications remain unchanged after deployment. If the application requires more computing resources, the old server is discarded, and the app is moved to a new high-performance server. By avoiding manual upgrades, immutable infrastructure makes cloud-native deployment a predictable process.


#### Microservices
Microservices are small, independent software components that collectively perform as complete cloud-native software. Each microservice focuses on a small, specific problem. Microservices are loosely coupled, which means that they are independent software components that communicate with each other. Developers make changes to the application by working on individual microservices. That way, the application continues to function even if one microservice fails. 


#### API
Application Programming Interface (API) is a method that two or more software programs use to exchange information. Cloud-native systems use APIs to bring the loosely coupled microservices together. API tells you what data the microservice wants and what results it can give you, instead of specifying the steps to achieve the outcome. 


#### Service Mesh
Service mesh is a software layer in the cloud infrastructure that manages the communication between multiple microservices. Developers use the service mesh to introduce additional functions without writing new code in the application. 

#### Serverless
Serverless computing is a cloud-native model where the cloud provider fully manages the underlying server infrastructure. Developers use serverless computing because the cloud infrastructure automatically scales and configures to meet application requirements. Developers only pay for the resources the application uses. The serverless architecture automatically removes compute resources when the app stops running. 


#### Azure Arc

What’s enabling the multi-cloud, multi-edge vision is Azure Arc.  Azure Arc brings cloud operations anywhere for your cloud native applications.  

First, Azure Arc helps you build cloud native apps anywhere, at scale. you can use DevOps techniques to deploy and manage Kubernetes apps at scale on your choice of any certified Kubernetes distribution. 

Next, Azure Arc provides a single pane of glass with central visibility through Azure Portal, and governance and compliance of your applications and Kubernetes clusters through Azure Policy.

And lastly, Azure Arc works with any CNCF-conformant Kubernetes cluster, making it possible to use Azure application services, data services and more anywhere to accelerate innovation. 

