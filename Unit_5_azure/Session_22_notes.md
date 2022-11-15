## 22nd Session: Azure Fundamentals 

### Azure Regions 
- Azure regions are set of datacenters deployed within a latency-defined perimeter and connected through a dedicated regional low-latency network. 
- Standard patterns for High Availability and Disaster Recovery

### Azure Structure
- Users are mapped to specific subscription mapped to an environment 

-- Management groups help you manage access, policy, and compliance for multiple subscriptions. All subscriptions in a management group automatically inherit the conditions that are applied to the management group.

-- Subscriptions logically associate user accounts with the resources that they create. Each subscription has limits or quotas on the amount of resources that it can create and use. Organizations can use subscriptions to manage costs and the resources that are created by users, teams, and projects.

-- Resource groups are logical containers where you can deploy and manage Azure resources like web apps, databases, and storage accounts.

-- Resources are instances of services that you can create, such as virtual machines, storage, and SQL databases.


### Azure Access 

Azure role-based access control (Azure RBAC) helps you manage who has access to Azure resources, what they can do with those resources, and what areas they have access to.

Azure RBAC is an authorization system built on Azure Resource Manager that provides fine-grained access management to Azure resources.


### Azure IaaS, PaaS and Shared Responsibility 

# IaaS vs PaaS vs SaaS

## Three categories of cloud computing

- 📝 [IaaS](#infrastructure-as-a-service-iaas), [PaaS](#platform-as-a-service-paas), [SaaS](#software-as-a-service-saas).
- Allows using a combination of these types of infrastructure.
  - E.g. [Microsoft 365 Apps](https://www.microsoft.com/en-ww/microsoft-365/business/microsoft-365-apps-for-business?market=af) on company computers (SaaS), VMs (IaaS) on Azure and Azure SQL Database (PaaS) to store your data.

### Infrastructure as a service (IaaS)

- Instant computing infrastructure, provisioned and managed over the internet.
- Aims to give you the most control over the provided hardware that runs your application
- 📝 E.g. virtual machines (VMs), storage, and operating systems.
- You rent hardware instead of buying
- Ensuring that a service is up and running is a shared responsibility (see [shared responsibility model](./4.1.%20Shared%20Responsibility%20Model.md))
  - cloud provider ensures the cloud infrastructure is functioning correctly
  - cloud customer ensures the service they are using is
    - configured correctly
    - up to date
    - available to their customers.

#### Common IaaS use cases

- **Migrating workloads**: Managed similar to on-prem infrastructure & provides easy migration path.
- **Test and development**: Teams can quickly set-up & dispose test/dev environments with fast & economical scaling.
- **Storage, backup and recovery**: Organizations avoid the capital outlay and complexity of storage management.
  - Useful for managing unpredictable demand and steadily growing storage needs.
  - can also simplify the planning and management of backup and recovery systems.

### Platform as a service (PaaS)

- Provides an environment for building, testing, and deploying software applications
  - Can add features such authentication.
- Aims to help creating an application quickly without managing the underlying infrastructure.
  - 📝 E.g. for a web app / Azure SQL databases you don't need to install an operating system, web server, or even system updates.
- Resources are purchased on a pay-as-you-go basis and accessed over a secure Internet connection.

#### Common PaaS use cases

##### Development framework

- Lets developers create applications using built-in software components.
- 📝 Cloud features such as scalability, high-availability, and multi-tenant capability are included
- Reducing the amount of coding that developers must do.

##### Analytics or business intelligence

- Tools provided as a service with PaaS allow organizations to analyze and mine their data.
- They can find insights and patterns, and predict outcomes to improve business decisions such as forecasting, product design, and investment returns.

### Software as a service (SaaS)

- Software that is centrally hosted and managed for the end customer.
- Usually based on an architecture where one version of the application is used for all customers
- Usually licensed through a monthly or annual subscription
- 📝 E.g. Office 365, Skype, and Dynamics CRM Online.

## Cost and Ownership

| | IaaS | PaaS | SaaS |
| -- | --- | --- | --- |
| Upfront costs | None, pay for what you use | None, pay for what you use | None, monthly / annual subscription |
| User ownership | purchase, installation, configuration, and management of their own software, operating systems, middleware, and applications | development of their own applications | not responsible for any maintenance or management of that software. |
| Cloud provider ownership | underlying cloud infrastructure (such as virtual machines, storage, and networking) is available for the user. | operating system management, network, and service configuration.. typically everything except user application | provision, management, and maintenance of the application software |

## Management responsibilities

- These categories are layers on top of each other
  - Abstraction order: SaaS > PaaS > IaaS
  - Abstraction = Hide details, quicker production but less control over the underlying hardware.
- IaaS: user is responsible for managing the operating systems, data, and applications.
- PaaS: user is responsible for the applications and data they run and store.
- SaaS: user just uses the software.

![shared responsibility model](./img/shared-responsibility-model.png)


### Resources & Locks
As an administrator, you can lock a subscription, resource group, or resource to prevent other users in your organization from accidentally deleting or modifying critical resources. 
You can set the lock level to CanNotDelete or ReadOnly. In the portal, the locks are called Delete and Read-only respectively.
CanNotDelete means authorized users can still read and modify a resource, but they can't delete the resource.
ReadOnly means authorized users can read a resource, but they can't delete or update the resource. Applying this lock is similar to restricting all authorized users to the permissions granted by the Reader role.

### Storage 
- Storage accounts and Data Lakes

### Networking  
Networking concepts:
VNet
Subnet
NIC
NSG
IP


### Compute
Concepts:
Virtual Machine
Managed Disk
Network Interface Card
Public IP Address
Virtual Network (VNet)
Subnet
Network Security Group


### Security & Performance  
Concepts:
Firewalls
Application Gateways 
Load Balancers