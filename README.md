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


ARCHITECTURE OVERVIEW 
1. Route 53.  
• AWS-managed DNS service that routes domain names to AWS resources. 
• Can route traffic globally based on latency, geolocation, or failover. 
• Often points to CloudFront or ALB. 
2. Internet Gateway (IGW).  
• Connects our VPC to the internet by allowing our public subnets to send and receive internet 
traffic. 
3. VPC Endpoint.  
• Creates a private connection between our VPC and S3 bypassing the public internet. 
4. Elastic Load Balancer.  
• Distributes incoming traffic across EC2 instances in multiple AZ’s thus improving fault 
tolerance. It also scales with demand. 
5. EC2 Auto Scaling Group. 
•  Automatically adjust the number of EC2 instances based on demand.  
• Ensure high availability and cost efficiency. 
6. Web Application Firewall.  
• Protects our applications from common attacks such as SQL injection and XSS.  
• It adds an additional security layer to our environment. 
7. NAT Gateway.  
• Enables instances in our private subnet to access the internet for updates or patches or to 
communicate with third party or external services.  
• It is placed in a public subnet, and routes via route tables. 
8. EC2. 
•  This compute service hosts our applications or backend logic.  
• It is deployed in a private subnet for security.  
• We attach it to an auto scaling group for high availability. 
9. RDS.  
• Managed relational database instance (e.g., MySQL, PostgreSQL). 
• Deployed in a private subnet for backend data storage. 
• Used by the app tier for structured data. 
10. RDS Standby.  
• This is a synchronous replica of our primary RDS in another AZ.  
• It is used for automatic failover in case of outages.  
• It increases database availability and disaster recovery. 
11. S3 Bucket.  
• Object storage for static files, backups, logs, and media assets. 
• Accessible privately via VPC endpoint or via CloudFront if public. 
• Highly durable and scalable. 
This architecture demonstrates a resilient, scalable, and secure design by leveraging AWS-native services 
across multiple Availability Zones. It ensures high availability through load balancing and auto scaling, 
enforces strong security at both the network and application layers, and supports private, cost-efficient 
connectivity to backend services like RDS and S3.  
Together, these components embody cloud architecture best practices for performance, fault tolerance, 
and operational excellence. 
