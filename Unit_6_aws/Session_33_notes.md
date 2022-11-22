## 33rd Session: AWS Fundamentals: Intro to Cloud 

### Introduction to Cloud

Cloud computing is the delivery of computing services over the Internet without direct active management by the user.

You typically pay only for cloud services you use, helping you lower your operating costs, run your infrastructure more efficiently, and scale as your business needs change.

There are 3 main types of cloud computing:
- Private cloud 
- Public cloud 
- Hybrid cloud 

There are 3 main types of cloud computing services.


### Types of cloud computing services 
#### Infrastructure as a Services (IaaS)
**Cloud service provider manages the infrastructure for you.**

- You rent IT infrastructure such as servers, virtual machines , storage etc, from a cloud provider on a pay as you go basis. 
- IaaS lets you bypass the cost and complexity of buying and managing physical servers and datacenter infrastructure. 


#### Platform as a Services (PaaS)
**The hardware and an application-software platform are provided and managed by an cloud service provider, but the user handles the apps running on top of the platform and the data the app relies on.**

- Cloud computing services that supply an on-demand environment for developing, testing, delivering, and managing software applications. 
- Like IaaS, PaaS includes infrastructure but also middleware, development tools, business intelligence (BI) services, database management systems, and more. 
- PaaS is designed to make it easier for developers to quickly create web or mobile apps, without worrying about setting up or managing the underlying infrastructure of servers, storage, network, and databases needed for development.
- PaaS allows you to avoid the expense and complexity of buying and managing software licenses



#### Software as a Services (SaaS)
**A service that delivers a software application (which the cloud service provider manages) to its users.**

- With SaaS, cloud providers host and manage the software application and underlying infrastructure, and handle any maintenance, like software upgrades and security patching. Examples: Emails / dropbox

**IaaS** – There is a shared responsibility between you and the cloud provider. Getting a pizza from the supermarket. The pizza is made for you but you still need to take care of cooking it and the dining environment. 
**PaaS** – This time you only have to manage a few things. When a pizza is delivered it is cooked and ready to eat. You just have to manage the dining situation. 
**SaaS** – Everything is looked after for. 
So depending on how you want to use the cloud, there are different option already ready for you


### Cloud service types
Broadly broken down to several different areas 
- **Compute** – process data
- **Storage** – store large amounts data. We will be focusing on this services later on in this session.
- **Database** – another way to store data in a more structured way
- **ML** – perform artificial intelligence on your data
- **Analytics** – find trends in your data and provide visualized results


### Why use the cloud?
**Speed** - Most cloud computing services are provided self service and on demand, so even vast amounts of computing resources can be provisioned in minutes, typically with just a few mouse clicks, giving businesses a lot of flexibility and taking the pressure off capacity planning.

**Productivity** - On-site datacenters typically require a lot of “racking and stacking”—hardware setup, software patching, and other time-consuming IT management chores. Cloud computing removes the need for many of these tasks, so IT teams can spend time on achieving more important business goals and focusing on the tasks they are good at

**Cost** - Cloud computing eliminates the capital expense of buying hardware and software and setting up and running on-site datacenters—the racks of servers, the round-the-clock electricity for power and cooling, and the IT experts for managing the infrastructure. It adds up fast.

**scale** –(refers to the ability to increase or decrease IT resources as needed to meet changing demand) The benefits of cloud computing services include the ability to scale elastically. For example, Netflix might get a lot of traffic on days when a new season of a popular show is released. Their resources can scale to give more computing power, storage, bandwidth at this time

**Global** – with on prem you used to have to build multiple datacenters across the world if you wanted local compute resources. But now cloud providers have already done this for you, and you can go global at the click of a button.

**Reliability** - Cloud computing makes data backup, disaster recovery, and business continuity easier because data can be mirrored at multiple redundant sites on the cloud provider’s network.

### AWS
**Region** - An AWS Region is a geographical area of the world where aws cluster data centers. And they call each group of logical data centers an  availability zone. 
Each AWS region as at least 3, isolated and physically separate AZs. 

**AZ** - Each zone in a region has independent power, cooling, security and is connected via redundant low latency networks.  This  reduces the likelihood of two zones failing simultaneously. A common misconception is that a single zone equals a single data center, but each AZ consists of one or more physical data centres. 

**Region examples** – region choice is all dependant on your own projects needs, where your customers are based etc. there are cost considerations as some regions are cheaper to use than others. You can place resources within different regions in the same AWS account but just have to give some consideration to this if you want different services to interact with each other. Not all services are supported in all regions. 

A **Local Zone** is an extension of an AWS Region It places select AWS services, like compute and storage services, closer to more end-users, providing them very low latency access to the applications running locally.


### IAM
If you are using AWS to host your applications then you would want to make sure that not everyone can access everything in AWS. For example, you may want only a certain group of people to be able to access customer data. 

AWS has many security services but Identity and Access management (aka IAM)  is one of the most widely used. 

IAM enables you to securely control access to AWS services and resources for your users. You use it to control who is authenticated and authorised to use resources.
Authentication verifies who the user is (so it checks you are who you say you are). Authorisation determines what resources a user can access. 
Passwords, security questions, biometrics etc are authentication methods. 

#### Components of IAM
**Users**
An IAM user is an identity with an associated credential and permissions attached to it. This can be an actual person who is the user, or it could be an application. 
A company might create an IAM user for each employee. One IAM user is associated with one AWS account

**Groups**
A collection of IAM users is an IAM group. 
You can use groups to specify permissions for multiple users so that any permissions applied to the group are applied to the individual users in the group as well. 
This can lessen the administrative burden of assigning permissions for every single user, instead you can just add them to groups. 

**Policies**
An IAM policy sets permissions and controls access to AWS resources. 
Permissions specify who has access to the resources and what actions they can perform. 

**Roles**
An IAM role is an IAM identity that you can create in your account that has specific permissions
It is similar to an IAM user, in that it is an AWS identity with permission policies that determine what the identity can and cannot do in AWS.
The difference is that instead of being uniquely associated with one person, a role can be assumed by anyone who needs it.
Roles also do not have standard long-term credentials such as a password.  Roles have temporary credentials for your session.

**Terminology**
Might here some of these terms used with IAM
Principal entity - Essentially just someone or something that has been verified.


### Features of IAM
**Granular Permissions**: You can grant different permissions to different people for different resources

**Identity federation** – if the user is already authenticated (e.g. through a facebook or google account) IAM can be made to trust that authentication and then allow access based on that. So a user doesnt have to remember multiple passwords. 

**Attribute-based Access Control (ABAC)**: authorization strategy you can use to create fine-grained permissions based on user attributes, such as department, job role, and team name. Using ABAC, you can reduce the number of distinct permissions that you need for creating fine-grained controls in your AWS account.

**Shared acces** – allows you to create separate usernames and passwords for individual users or resources and delegate access. 

**MFA** – you can add 2 factor authentication to individual users for extra security. So this is putting in you password and then when you get an additional text with a code.

**Free** - IAM is an AWS service that is offered at no additional charge


### Policy and Permissions
A policy defines an identity's or resource's permissions. AWS will check these permissions when someone or something makes a request to that resource. 
Sid - Sid value is just a sub-ID of the policy document’s ID. In IAM, the Sid value must be unique within a JSON policy.

This example has wildcards which should be used carefully.

**Principle of Least Privilege**: ensuring that services, users and roles only have the access permissions that they require in order to fulfil their role/function. This means reviewing IAM permissions periodically in order to revoke permissions when they are no longer needed and to review current permissions. 


1. Identity-based: Attach managed or inline policies to IAM identities (users, groups to which users belong, or roles). Identity-based policies grant permissions to an identity.

2. Resource-based: Attach inline policies to resources. The most common examples of resource-based policies are Amazon S3 bucket policies and IAM role trust policies. Resource-based policies grant permissions to the principal that is specified in the policy. 

3. Permission boundaries: A permissions boundary is an advanced feature in which you set the maximum permissions that an identity-based policy can grant to an IAM entity. A permissions boundary alone doesn’t grant access to anything. Rather, it enforces a boundary that can’t be exceeded

4. Organizations SCPs: Use an AWS Organizations service control policy (SCP) to define the maximum permissions for account members of an organization or organizational unit (OU).
offer central control over the maximum available permissions for all accounts in your organization and again do not grant permissions.

5. ACLs: Use ACLs to control which principals in other accounts can access the resource to which the ACL is attached. ACLs are similar to resource-based policies, although they are the only policy type that does not use the JSON policy document structure. ACLs are cross-account permissions policies that grant permissions to the specified principal. ACLs cannot grant permissions to entities within the same account. (ACLs are an access control mechanism that predates resource-based policies and IAM. )
ACLs are an access control mechanism that predates resource-based policies and IAM. 

6. Advanced policies that you pass as a parameter when you programmatically create a temporary session for a role – so you can interact with aws resources through your command line interface. But to do this you’re going to need to login to your AWS when you are using CLI. So a session policy can be used here. Session policies limit the permissions that the role or user's identity-based policies grant to the session. Session policies limit permissions for a created session, but do not grant permissions.

PTN Example you’ve attached an identity based policies that allows someone read access to a resource, but you’ve also put a deny actions on the resource


Identity based are JSON permissions policy documents that control what actions an identity can perform. (and if you recall identities are users, groups and roles)

Inline policies – Policies that you add directly to a single user, group, or role. Inline policies maintain a strict one-to-one relationship between a policy and an identity. They are deleted when you delete the identity.

Resource based – granting the principle (which is just an authenticated entity)
Resource-based policies are inline policies. There are no managed resource-based policies.


John Smith – John can perform list and read actions on Resource X. He is granted this permission by the identity-based policy on his user and the resource-based policy on Resource X.

Carlos Salazar – Carlos can perform list, read, and write actions on Resource Y, but is denied access to Resource Z. The identity-based policy on Carlos allows him to perform list and read actions on Resource Y. The Resource Y resource-based policy also allows him write permissions. However, although his identity-based policy allows him access to Resource Z, the Resource Z resource-based policy denies that access. An explicit Deny overrides an Allow and his access to Resource Z is denied. 

Mary Major – Mary can perform list, read, and write operations on Resource X, Resource Y, and Resource Z. Her identity-based policy allows her more actions on more resources than the resource-based policies, but none of them deny access.

Zhang Wei – Zhang has full access to Resource Z. Zhang has no identity-based policies, but the Resource Z resource-based policy allows him full access to the resource. Zhang can also perform list and read actions on Resource Y.


Identity-based policies and resource-based policies are both permissions policies and are evaluated together. For a request to which only permissions policies apply, AWS first checks all policies for a Deny. If one exists, then the request is denied. Then AWS checks for each Allow. If at least one policy statement allows the action in the request, the request is allowed. It doesn't matter whether the Allow is in the identity-based policy or the resource-based policy.



### Storage - S3

#### What is S3?
The service itself is called Amazon simple storage service and is known as S3

Object storage – it requires less metadata than traditional file systems to store and access files

S3 offers unlimited storage space. The maximum file size for an object in Amazon S3 is 5 TB.

#### How does S3 work?
**Objects** - You can upload any type of file to Amazon S3, such as images, videos, text files, and so on. 

**Keys**: -  Amazon S3 encrypts an object before saving it to disk and decrypts it when you download the objects.

**Versioning** - You can also version objects to protect them from accidental deletion of an object. What this means is that you always retain the previous versions of an object, as like a paper trail.

#### Feature of S3 - Access Management 
**Block public access** – if you have other bucket policies or object permissions to allow public access, the S3 Block Public Access settings will override these policies and permissions. 

**Bucket policies** - You can use bucket policies to add or deny permissions for the objects in a bucket.

**ACLs** - ACLs are an access control mechanism that predates resource-based policies and IAM. 

#### Feature of S3 - Storage classes

**S3 standard** - data is stored in such a way that AWS can sustain the concurrent loss of data in two separate storage facilities. This is because data is stored in at least three facilities. So multiple copies reside across locations

**S3-IA** -  used for data that is accessed less frequently but requires rapid access when needed. So it’s a good place to store backups, disaster recovery files, or any object that requires long term storage. 

**One Zone IA** – noticeable difference is that data is only stored in one availability zone. However, because of this it has a lover storage price than S3 Standard IA. You would only want to use this if you could easily reproduce your data in the event of an AZ failure

**Intelligent tiering** – does require a small monthly monitoring and automation fee per object

**S3 Glacier** - say, we need to retain data for several years for auditing purposes. And we don't need it to be retrieved very rapidly – then you can use S3 Glacier to archive that data. 
You have three options for retrieval which range from minutes (being glacier instant) to hours (being deep archive)

**Lifecycles**
You can use lifecycle policies to move data between tiers. This can help optimise costs. 
With Lifecycle policies, you create that configuration without changing your application code and it will perform those moves for you automatically

#### Feature of S3 - Pricing 

Storage - You pay for storing objects in your S3 buckets. The rate you’re charged depends on your objects' size, and the storage class
Requests - You pay for requests made against your S3 buckets and objects. S3 request costs are based on the request type, and are charged on the quantity of requests 
Data transfer - You pay for all bandwidth into and out of Amazon S3 with some exceptions
We don’t cover the last 3 but:
Management and analytics –You can use analytics and insights in Amazon S3 to understand, analyze, and optimize your storage usage and you pay for these features
Replication -  copying of objects across Amazon S3 buckets
Lamba - With S3 Object Lambda you can add your own code to S3 GET requests

Have put some pricing information here. You don’t need to know the amounts to the cents but the One Zone IA  is the cheapest of the S3 Standard options but Glacier deep archive is the cheapest of them all due to the long retrieval times.
