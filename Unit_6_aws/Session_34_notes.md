## 34th Session: AWS Fundamentals: Networking 

### What is Networking 

- A computer network consists of two or more connected computers that can share data
- This connection is twofold: (a) physical - through wires, cables, and wireless media and (b) logical - through the transport of data across the physical media
- Servers are only able to communicate to other servers or other clients with the use of a Network Interface Card (NIC)
- Every NIC has a hardware address known as a MAC Address, this is unique to each NIC
- Devices connected in a network use a system of rules, called communications protocols, to transmit information over physical or wireless technologies


### Type of Networks
A short-range network is one that doesn't encompass long distances.
PAN -  very short range - used for things like sharing files between a phone and a laptop wirelessly using Bluetooth.
LAN - has a bit of a longer range - a network that is contained within a building where we would have desktops, laptops, network printers and so on connected.
WAN - covers a wide area or long distance, it is a network that exists over a large-scale geographical area. 
A WAN connects different smaller networks, including local area networks (LANs) and metro area networks (MANs). 
This ensures that computers and users in one location can communicate with computers and users in other locations.


### Binary
What is binary?
Computers don’t understand word or numbers
Binary is a system used by the computer to store data, where numbers and values are expressed as 0 or 1 known as a base 2 number system e.g. think the screens in the Matrix 
False (0) or True (1) 
Bit is a single binary value either 0 or 1
Byte contains 8 bits meaning it can have 256 (28) different values
Megabyte is 106 or 1,000,000 bytes
The computer uses binary as a set of instructions
A system where each possible place in a number can be one of 10 digits.  This counting system is known as decimal, denary or base 10.
For example, 176 
 100  10  1
 1  7  6
 100 + 70 + 6 = 176
Binary uses base 2 (allowing us to use 0 to 1):
 128  64  32  16  8  4  2   1
 1  0  1  1  0  0  0  0 
 128 + 32 + 16 = 176


### IPs
An IP address is a series of numbers assigned to a device connected to a computer network or the internet.
Generally, consists of four numbers ranging from 0 to 255.
Each of the 4 numbers is an 8-digit binary number.
Each IP address is split into two parts: Network ID and Host ID
Where the division happens is defined by the subnet mask


### Classless Inter-Domain Routing (CIDR)
Classless Inter-Domain Routing - CIDR, is an alternative to traditional subnetting
The idea is that you can add a component to the IP address itself indicating the number of bits that make up the networking portion. 
With the earlier example of IP address 192.168.1.34 being associated with the subnet mask 255.255.255.0
The CIDR notation would be 192.168.1.34/24 
whereby the /24 comes from the number of bits in the subnet 255.255.255.0 (255 = 128 + 64 + 32 +16 + 8 + 4 + 2 + 1 = 11111111 = 8 and 8 + 8 + 8 = 24) 
Let’s take IP address 192.168.1.34 again but instead associated with subnet mask 255.255.128.0. The CIDR notation would now be 192.168.1.34/17 


### TCP vs UDP
- Both TCP and UDP are protocols used for sending bits of data (packets) over the Internet.
- TCP is more popular across the Internet for sending important data like secure files, important webpages etc. 
- There has to be a three-way packet exchange to establish a session before any data is transmitted between to devices that communicate using the TCP transport mechanism.
- This is known as the TCP three-way handshake 


### TCP vs UDP
Host A sends a TCP SYNchronize packet to Host B
Host B receives A's SYN
Host B sends a SYNchronize-ACKnowledgement
Host A receives B's SYN-ACK
Host A sends ACKnowledge
Host B receives ACK. 
TCP socket connection is ESTABLISHED.
After this they can start transmitting data using the TCP transport. 


### TCP vs UDP
UDP is also common, but it cannot be relied upon for sending important data like secure files, important webpages etc. 
It is used mostly for streaming media including audio and video, like online radio station. 
UDP is faster than TCP and media players work best with it. 
There is no flow control or error correction but the speed is far greater so despite streaming media not being of high quality, it can be viewed properly with UDP


### Network Address Translation (NAT)
Links internal IP addresses with external ones
     For example; 
The internal IP address of a website hosted on KPC is converted to the external IP address clients use to access it
The client types in the URL
From the URL, the DNS finds the public IP it relates to
The NAT then finds which private IP this related to within our private network
The client accesses the website


### DHCP
How computers get assigned IP addresses.
- A computer is connected to the DHCP Server
- The computer sends out a request to get an IP address (Discover)
- The DHCP server replies by sending an offer of an IP address (Offer)
- The computer responds by asking permission to us that IP (Request)
- The DHCP server then confirms that it is okay (Acknowledgement) 


### Ports
When your computer sends data to another computer, it sends the data to a specific IP address and uses a specific port
For example, if I host a website on a web server, I will bind that web server to a specific port. This port will then be used to listen out for traffic wanting to retrieve data from the webserver
Some common port numbers are:
  HTTPS : 443
  HTTP:   80
  FTP:   20, 21
  SSH:   22


### Firewalls
Controls who can access your secured internal network
Two methods of control: Allow traffic, or block traffic

For example:
Block everyone except a list of IP addresses that are allowed access
Allow everyone except IP addresses you know should not have access
Blocking everyone tackles a lot of management, as when someone new needs access, a new rule must be implemented
Allowing everyone leaves you vulnerable to unknown threats 


### How a Protocol Stack Works
**Where did the name come from?**
The term derives from protocols being like a pile of building blocks stacked one upon another. Because of this structure, groups of related protocols are often called stacks or protocol stacks.

**How does it work?**
Data is passed down the stack from one layer to the next, until it is transmitted over the network by the network access layer protocols. The layers in this reference model are crafted to distinguish between the different ways that the data is handled as it passes down the protocol stack from the application layer to the underlying physical network.
At the remote end, the data is passed up the stack to the receiving application. The individual layers do not need to know how the layers above or below them function; they only need to know how to pass data to them.
Each layer in the stack adds control information (such as destination address, routing controls, and checksum) to ensure proper delivery. This control information is called a header and/or a trailer because it is placed in front of or behind the data to be transmitted. Each layer treats all of the information that it receives from the layer above it as data, and it places its own header and/or trailer around that information. 


### Architectural Models 

An architectural model is a common frame of reference for discussing Internet communications. 
It separates the functions performed by communication protocols into manageable layers stacked on top of each other. Each layer in the stack performs a specific function in the process of communicating over a network.


### Architectural Models and Protocols 
**What does an Architectural Model define?**
It defines a data communication function that may be performed by any number of protocols. 

**What is a protocol?**
A protocol is a set of rules and conventions that describe how information is to be exchanged between two entities


### OSI Model 
In the 1970s, the International Standards Organisation (ISO) developed the Open Systems Interconnection (OSI) reference model. It is a conceptual framework that describes the basic functions of a networking system. There are 7 layers to this model.

How many layers does the internet reference model contain?
- Network Access Layer
- Internetwork Layer
- Host-to-Host Transport Layer
- Application Layer

#### Network Layer 
Concerned with getting data through different types of physical networks (Ethernet, Token Ring etc. )

Purpose / Function
- To reduce the need to rewrite higher levels of TCP/IP Stack when new physical network technologies can do it (Asynchronous Transfer Mode and Frame Relay)

Advantages
- it’s addressing scheme  
- Allows users and applications to identify a specific network or host with which to communicate. So Packets (or datagrams) aren’t lost, but also faster delivery. 

With a committed IP address, you're ready to acquire SSL declarations that upgrade the security of your guests.


### Networking Fundamentals 

#### Network Interface Card (NIC)
- A NIC establishes a dedicated, continuous connection between a computer and a network.
- A NIC, Network Interface Card is a piece of hardware is inserted to a computer to connect it to a network. Modern NICs enable computers to perform tasks such as I/O interrupt support, data transfer, network traffic engineering, and partitioning.
- It implements the physical layer circuitry required for data link layer communication using a standard such as Ethernet or Wi-Fi. Each card represents a device and can prepare, transmit, and control data flow throughout the network. The NIC makes use of the OSI model to transmit signals at the physical layer, data packets at the network layer, and as an interface at the TCP/IP layer.
- This connection can also be established with: Wireless NICs, Wired, USB, Optical fibres

#### MAC (Media Access Control)
What is a MAC address:
- Every NIC has a unique hardware address that’s known as a MAC address
- A string of usually six sets of two-digits or characters
- Layer 2 of the OSI model
- Many manufacturers of NICs (e.g. Dell and Cisco) will put a unique sequence at the beginning of their products’ MAC addresses. This is called an organizationally unique identifier (OUI)

What are they used for:
- The MAC address is used to deliver the data to the right device on a network
- Allows you to filter devices on modern routers: you can tell your router to deny access to specific MAC addresses (i.e., specific physical devices) or only allow certain MAC addresses to connect.
- Example use of MAC addresses is diagnosing network issues . This is because they don't change, as opposed to a dynamic IP address, which can change from time to time. For a network administrator, that makes a MAC address a more reliable way to identify senders and receivers of data on the network.


#### Virtual Private Cloud (VPCs)
- A virtual private cloud (VPC) is a secure, isolated private cloud hosted within a public cloud. 
- VPC customers can run code, store data, host websites, and do anything else they could do in an ordinary private cloud, but the private cloud is hosted remotely by a public cloud provider. (Not all private clouds are hosted in this fashion.) 
- VPCs combine the scalability and convenience of public cloud computing with the data isolation of private cloud computing.
- Imagine a public cloud as a crowded restaurant, and a virtual private cloud as a reserved table in that crowded restaurant. Even though the restaurant is full of people, a table with a "Reserved" sign on it can only be accessed by the party who made the reservation. Similarly, a public cloud is crowded with various cloud customers accessing computing resources – but a VPC reserves some of those resources for use by only one customer.


#### Subnets 
##### What is a subnet
- When you divide a network into two or more networks you will create subnets.
- They are containers within your VPC that segment off a slice of the CIDR block you define in your VPC. 
- So a subnet will have a range of IP addresses in your VPC.

##### Why do we use them?
- Subnetting allows you to create a fast and efficient computer network:
- As networks become larger and more complex, the traffic traveling through them needs more efficient routes. If all network traffic was traveling across the system at the same time using the same route, congestion would occur resulting in inefficient backlogs.
- Creating a subnet allows you to limit the number of routers that network traffic has to pass through.
- Subnets allow you to give different access rules and place resources in different containers where those rules should apply.
- For example, in a business network the HR department may want their devices to be on a restricted part of the network because they store payroll information and other sensitive employee data. 

##### Route Tables
What is a route table
- A route table is a set of rules called routes that are used to determined where network traffic is directed. 

How does it work
- When a router receives a data packet that needs to be forwarded to a host on another network, it examines its destination IP address and looks for the routing information stored in the routing table.
- A typical IP routing table entry contains the following information:
- Network ID or host route internetwork address.
- Subnet mask used to determine the network ID from the IP address.
- Forwarding address or gateway. 
- Port number used to forward packets to the network ID.

##### Subnets and Route tables in AWS
- AWS provides two types of subnetting:
- Public - allows the internet to access the machine

What makes this possible is that the route table will have an internet gateway attached to it
Private - hidden from the internet
- Each subnet in your VPC must be associated with a route table, which controls the routing for the subnet (subnet route table). A subnet can be explicitly associated with custom route table.
- Main route table automatically comes with VPC. It controls the routing for all subnets that are not explicitly associated with any other route table.
- A subnet can only be associated with one route table at a time, but you can associate multiple subnets with the same subnet route table.

##### Express Route/AWS Direct Connect 
What is an express route?
- Super-fast connection into Azure 
- Don’t go over public internet
- Private, secure, high bandwidth, low latency connection

How does it work?
- Direct Connect is a network service that allows a customer to establish a dedicated fast network connection between on premise and AWS WITHOUT the internet.
- Secure, low latency connection
- Provides a safer, more consistent network experience than Internet-based connections.
- Direct Connect can be used with all AWS services

##### VPN
What is an VPN?
- A virtual private network, or VPN, is an encrypted connection over the Internet from a device to a network. 
Gives you online privacy by masking your internet protocol (IP) address and encrypting all the traffic leaving your device

Why do we use them?
- The encrypted connection helps ensure that your data is safely transmitted.

How does it work?
- A VPN works by routing your device’s internet connection through your chosen VPN’s private server rather than your internet service provider (ISP)

##### Internet Gateway (IGW)
What is an internet gateway(IGW)?
- Component that allows communication between your VPC and the internet.
- Not a hardware component but a software component 

Why do we use them?
- Enables inbound and outbound access to the internet
- performs network address translation (NAT) for public instances
- Horizontally scaled, redundant and highly available

How does it work?
- Provides private network with a route to the internet
- Without a IGW then the VPC would not be able to access the internet
- One IGW can handle all the traffice from one VPC only.


##### Network Address Translation (NAT) Gateway
- A NAT Gateway creates an instance in a private subnet which can connect to services outside your VPC, but external services cannot initiate a connection with those instances. 
- A NAT Gateway has its own public IP address and allows your workloads to access the internet using it public IP address but prevents any connection from the internet to the private subnet being made. 
- NAT Gateways are very important for maintaining SECURITY when wanting to give internal services access to the internet

##### Network Address Control List (NACLs)
- Network Access Control Lists (NACLs) are an optional layer of security inside your VPC that behaves like a firewall before the subnets 
- A NACL is composed of a series of rules that allows or restricts network traffic of a particular sort (i.e., http, https, ssh) or IP range. You can create many rules and these rules are evaluated in numerical order based on the smallest number first. 
- A NACL can be assigned to many subnets, however you cannot assign a subnet to many NACLs. 
- An example use case for a NACL is if you wanted to restrict access to a public subnet to only a small set of IP addresses. 
