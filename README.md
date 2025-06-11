# AWS-SAA-PROJECTS
## AWS VPC Architecture

![AWS SINGLE TIER ARCHITECTURE](SINGLE-TIER-ARCHITECTURE-GIT.pdf)

INTRODUCTION
This architecture represents a  single-tier architecture which is a basic application design where all components (such as the web server, application logic, and database) are hosted on a single instance or layer. We have designed this architecture to be cost-effective, scalable, secure and highly available. 

ARCHITECTURE OVERVIEW.
Infrastructure and Network.
1.	Virtual Private Cloud: This is our Private or logically isolated space in the AWS cloud where we can launch AWS resources we want. We can define our IP ranges, subnets, route tables.
2.	Subnets: We have 2 public subnets where our EC2’s are hosted. Our subnets have public access, and they help us organise our resources and control traffic to them.
3.	Route 53: This Domain name service helps translate domain names to IP addresses thus enabling users to communicate with our application.
4.	Internet Gateway: Enables communication between our VPC and the Public internet.
5.	Elastic Load Balancer: Distributes incoming traffic across our various EC2 instances.
6.	Security Group: Our security group is a stateful service that controls traffic into our EC2 instances.
7.	EC2 instances: These are the core of our application or service as they are virtual servers (compute) which hosts our application, our webserver and database in this case.
8.	EC2 Auto scaling: This service automatically adjusts the number of EC2 instances running based on the demand. It scales up and down to ensure resources are efficiently used.
9.	IAM User: The Identity and Access Management service authenticates and gives us access to our AWS resources. When we create an initial account, we get a root user who is the super user of the account. We then create IAM users for the day-to-day running of the account. In addition, we can use an IAM role to give temporary access to our AWS resources.
INTRODUCTION 
The AWS 3-tier architecture consists of a Presentation layer hosted in public subnets for routing and 
frontend delivery, an application layer in private subnets running business logic, and a Data layer also in 
private subnets for secure storage and database access — all orchestrated across multiple Availability 
Zones for high availability and fault tolerance.


