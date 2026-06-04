AWS & Cloud Computing Study Notes
1. Cloud Computing
Definition

Cloud computing is the on-demand delivery of IT resources over the internet with pay-as-you-go pricing.

Examples:

Storage
Servers
Databases
Networking
Analytics
Machine Learning
Service Models
IaaS (Infrastructure as a Service)

Provides infrastructure resources such as:

Virtual machines
Storage
Networking

Example:

Amazon EC2
PaaS (Platform as a Service)

Provides a platform for application development.

Example:

AWS Elastic Beanstalk
SaaS (Software as a Service)

Complete software applications delivered over the internet.

Examples:

Gmail
Microsoft 365
Characteristics of Cloud Computing
Self-service provisioning
Elasticity (scale resources automatically)
Measured usage (pay only for what you use)
Access from anywhere with internet
Rapid deployment
No hardware lead time
Converts Capital Expenses (CapEx) to Operational Expenses (OpEx)
Benefits of Cloud Computing
Rapid experimentation
Faster deployment (minutes instead of months)
Global accessibility
Supports AI/ML, IoT, and DevOps
Easy scaling during traffic spikes
Multi-AZ redundancy
Enhanced security and compliance options
Supports remote and distributed teams
Reduces hardware and maintenance costs
Prevents over-provisioning
AWS (Amazon Web Services)

AWS is a cloud platform that provides:

Compute
Storage
Networking
Security
Databases
Analytics

Benefits:

Cost-effective
Highly flexible
Scalable
Global infrastructure
2. Amazon EC2 (Elastic Compute Cloud)
Definition

EC2 provides virtual machines (instances) in the AWS cloud.

Features
Launch virtual servers on demand
Scale up/down based on workload
Full control over:
Security
Networking
Storage
No hardware investment required
Instance Types

Instance types define:

CPU power
Memory
Storage
Networking capacity

Choose instance types according to workload requirements.

vCPU

vCPU = Virtual Central Processing Unit

Represents the processing power allocated to an EC2 instance.

Amazon Machine Image (AMI)
Definition

AMI (Amazon Machine Image) is a template used to launch EC2 instances.

Contains:

Operating System
Installed software
Dependencies
Libraries
Configuration

Benefits:

Launch multiple identical EC2 instances
Consistent deployments
Security Groups
Definition

Security Groups act as a virtual firewall for EC2 instances.

Features
Control inbound traffic
Control outbound traffic
Stateful security
Important Notes
By default, all outbound traffic is allowed.
You must configure inbound rules.
Security groups allow traffic but cannot explicitly deny traffic.
Key Pairs

Used to securely connect to EC2 instances.

Components
Public Key

Stored on AWS EC2 instance.

Private Key

Stored by the user.

Access is granted only when the keys match.

Important: Keep the private key secure.

Tags
Definition

Tags are key-value pairs assigned to AWS resources.

Example:

Environment = Production
Owner = Alan

Benefits:

Resource organization
Easier management
Cost tracking
EC2 Pricing Options
On-Demand

Pay for usage without long-term commitment.

Reserved Instances

Commit for longer periods for lower costs.

Spot Instances

Use unused AWS capacity at discounted prices.

3. Amazon EBS (Elastic Block Store)
Definition

Persistent block storage for EC2 instances.

Characteristics:

Attached to a specific EC2 instance
Data persists independently of the EC2 instance
EBS Volume Types
SSD-Based Volumes
General Purpose SSD

Balanced performance for most workloads.

Provisioned IOPS SSD

High-performance workloads requiring consistent IOPS.

HDD-Based Volumes
Throughput Optimized HDD

Large sequential workloads.

Cold HDD

Low-cost storage for infrequently accessed data.

Instance Store
Definition

Temporary block storage attached directly to the host machine.

Characteristics:

High speed
Temporary storage
Suitable for cache and scratch data
Data is lost when the instance stops/terminates
4. AWS Batch
Definition

AWS Batch allows developers, scientists, and engineers to run large-scale batch computing jobs.

AWS Batch automatically:

Provisions resources
Schedules jobs
Optimizes CPU and memory allocation

Users focus on:

Application code
Shell scripts
Java programs
Linux workloads
AWS Batch Components
Job

The application or workload to run.

Job Definition

Specifies:

IAM Role
vCPU requirements
Memory requirements
Container settings
Job Queue

Stores jobs until scheduled.

Compute Environment

Provides computing resources used to run jobs.

Compute Environment Types
Managed

AWS manages:

EC2 instance selection
Scaling
Resource provisioning
Unmanaged

You manage:

EC2 resources
ECS cluster
Scheduler

Responsible for:

Job execution
Dependency handling
Queue management
AWS Batch with Fargate

Use Fargate when:

You don't want to manage EC2 infrastructure
Simplicity is preferred

Advantages:

Faster startup
No EC2 management

Use EC2 when:

Workloads are very large
Specific CPU/memory configurations are required
Example Use Case
Stock Market Trading

Process:

Collect large trading datasets
Run batch jobs
Load data into a data warehouse
Perform analytics and predictions
5. AWS Elastic Beanstalk
Definition

Elastic Beanstalk is a service for deploying and scaling applications without managing underlying infrastructure.

Developers focus on:

Writing code
Deploying applications

AWS handles:

Provisioning
Load balancing
Scaling
Monitoring
Benefits
Fast deployment
Easy application scaling
Supports multiple programming languages
Infrastructure management handled by AWS
Monitoring dashboard included
Elastic Beanstalk Environment

When an environment is created, Elastic Beanstalk automatically provisions resources required to run the application.

Web Tier Architecture
HTTP & HTTPS

Protocols used by browsers to communicate with websites.

Route 53

Receives user requests and directs traffic.

Elastic Load Balancer (ELB)

Functions:

Receives requests
Distributes traffic across EC2 instances
Improves availability
Auto Scaling Group (ASG)

Automatically:

Adds EC2 instances during high traffic
Removes EC2 instances during low traffic
Host Manager

Software running inside EC2 instances responsible for:

Log generation
Monitoring
Event management
Quick Exam Revision Sheet
EC2
Virtual machine in AWS
Uses AMIs
Protected by Security Groups
Uses Key Pairs for login
EBS
Persistent storage
Data survives instance restart
Instance Store
Temporary storage
Faster but non-persistent
AWS Batch
Runs batch jobs
Uses Job Definitions, Job Queues, Compute Environments
Fargate
Serverless container execution
No EC2 management
Elastic Beanstalk
Deploy applications quickly
AWS manages infrastructure
ELB
Distributes incoming traffic
ASG
Automatically scales EC2 instances
Route 53
DNS and traffic routing service
AWS Elastic Beanstalk
Web Tier Environment
HTTP and HTTPS

HTTP and HTTPS are foundational web protocols used by browsers to communicate with websites.

Elastic Beanstalk Environment

An Elastic Beanstalk environment automatically provisions and configures AWS resources required to run an application successfully.

Elastic Load Balancer (ELB)

When a user sends a request:

Route 53 receives the request.
Route 53 forwards the request to the Elastic Load Balancer (ELB).
The ELB distributes traffic across multiple EC2 instances within an Auto Scaling Group.

Benefits:

Improved availability
Better performance
Load distribution
Auto Scaling Group (ASG)

Auto Scaling automatically adjusts the number of EC2 instances based on application demand.

Functions:

Adds EC2 instances during increased traffic
Removes EC2 instances during decreased traffic
Host Manager

Host Manager runs on EC2 instances and is responsible for:

Log file generation
Monitoring
Event management
Worker Environment

A worker environment handles background processing tasks that are resource-intensive or time-consuming.

Examples:

Database cleanup
Report generation
Background processing jobs
How It Works

Elastic Beanstalk installs a daemon on each EC2 instance within the Auto Scaling Group.

The daemon:

Polls messages from an Amazon SQS queue.
Executes tasks based on received messages.
Removes messages after successful completion.
Retries failed messages when necessary.
Amazon SQS

SQS (Simple Queue Service) is a message queuing service that allows applications to communicate asynchronously.

Supported Platforms

Elastic Beanstalk supports:

Linux
Windows
Docker
GlassFish
Go
Java
Node.js
Python
Ruby
Tomcat
Elastic Beanstalk Deployment Policies
All at Once Deployment

The new application version is deployed simultaneously to all EC2 instances.

Advantages:

Fast deployment

Disadvantages:

Complete application downtime during deployment
Rolling Deployment

The application is deployed in batches.

Characteristics:

Some instances run the old version while others receive updates.
Reduces downtime compared to All at Once deployments.
Rolling Deployment with Additional Batch

The deployment occurs in batches while AWS temporarily launches additional instances.

Advantages:

Better availability during updates
Reduced impact on users
Immutable Deployment

AWS launches a completely new set of instances with the updated application version.

Advantages:

Safer deployments
Easier rollback
No modification of existing instances
Traffic Splitting

The new version is deployed to a separate group of instances.

Incoming traffic is split between:

Existing version
New version

Benefits:

Real-world testing
Reduced deployment risk
Elastic Beanstalk Pricing

AWS does not charge separately for Elastic Beanstalk.

Users only pay for the underlying AWS resources, such as:

EC2 instances
Elastic Load Balancers (ELB)
Auto Scaling Groups
Storage services
Elastic Load Balancing (ELB)

ELB = Elastic Load Balancing

Purpose:

Automatically distributes incoming application traffic across multiple targets.

Benefits:

Improved fault tolerance
Increased scalability
Better application availability
AWS Lambda
Definition

AWS Lambda is a serverless compute service that allows developers to run code without provisioning or managing servers.

Key Features
Executes code only when needed
Automatically scales based on demand
Pay-per-use pricing model
No charges when code is not running
Event-Driven Execution

Lambda can execute code in response to events such as:

S3 bucket updates
DynamoDB table changes
HTTP requests through API Gateway
API Gateway

Amazon API Gateway is a fully managed service that enables developers to:

Create APIs
Publish APIs
Maintain APIs
Monitor APIs
Secure APIs

at virtually any scale.

API

API = Application Programming Interface

An API enables communication between different software applications.

Serverless Computing

Serverless computing is a cloud execution model where developers write and deploy code without managing the underlying infrastructure.

Characteristics:

Pay only for usage
No server management
Automatic scaling
Infrastructure handled by AWS

Note:
Servers still exist, but AWS manages them on behalf of the user.

Lambda Responsibilities

When using Lambda:

User Responsibilities
Writing code
Uploading code
Configuring triggers
AWS Responsibilities
CPU management
Memory allocation
Networking
Scaling
Infrastructure maintenance

Users cannot:

Log into Lambda servers
Customize the operating system
Lambda Functions

A Lambda function is a block of executable code deployed to AWS Lambda.

Deployment methods include:

ZIP file uploads
Code editor uploads
Amazon S3 uploads
Monitoring Lambda

After deployment, Lambda automatically integrates with Amazon CloudWatch.

CloudWatch provides:

Metrics
Monitoring
Logging
Observability
Lambda Layers

Lambda Layers are reusable packages that contain:

Libraries
Dependencies
Custom runtimes
Additional code

Benefits:

Reusability
Simplified deployment
Reduced package duplication
Client-Server Model
Client

A client is an application that sends requests to a server.

Examples:

Web browser
Desktop application
Mobile application
Server

A server processes requests and returns responses.

Example:

A client requests a news article.
The server processes the request.
The server returns the requested information.
The client displays the content.
Cloud Computing
Definition

Cloud computing is the on-demand delivery of IT resources and applications over the internet using a pay-as-you-go pricing model.

Cloud Deployment Models
Private Cloud

Infrastructure is dedicated to a single organization and typically hosted on-premises.

Benefits:

Greater control
Enhanced security
Public Cloud

Infrastructure is owned and operated by cloud providers such as AWS.

Benefits:

Lower upfront costs
Scalability
Pay-as-you-go pricing
Hybrid Cloud

A combination of cloud resources and on-premises infrastructure.

Benefits:

Flexibility
Gradual cloud adoption
Resource integration
Amazon EC2 (Elastic Compute Cloud)
Definition

Amazon EC2 provides virtual servers, known as instances, in the AWS cloud.

Traditional Infrastructure Approach

Organizations typically:

Purchase servers
Wait for delivery
Install hardware
Configure systems
Maintain infrastructure

Challenges:

High upfront costs
Long deployment times
AWS Approach

AWS:

Owns and manages data centers
Purchases and installs hardware
Makes servers immediately available

Users can launch instances within minutes.

Benefits of EC2
Rapid deployment
Flexible scaling
Pay only for usage
Full administrative control
Cost optimization
Multitenancy

Multitenancy allows multiple virtual machines to share the same physical hardware.

This is enabled through virtualization technology.

Hypervisor

A hypervisor manages virtual machines and allocates resources from the underlying physical host.

EC2 Use Cases
Internal business applications
Web applications
Databases
Third-party software hosting
Instance Types

Instance types define the hardware configuration of an EC2 instance, including:

CPU
Memory
Storage
Networking performance

Different instance types are optimized for different workloads.
Amazon EC2 Instance Families

Amazon EC2 instance types are grouped into different instance families, each optimized for specific workloads.

General Purpose (GP)

General Purpose instances provide a balanced mix of:

Compute (CPU)
Memory
Networking
Common Use Cases
Web servers
Application servers
Code repositories
Diverse workloads
Compute Optimized (CO)

Compute Optimized instances are designed for applications requiring high processing power.

Common Use Cases
Compute-intensive workloads
Gaming servers
High Performance Computing (HPC)
Scientific modeling
Batch processing
Memory Optimized (MO)

Memory Optimized instances are designed for workloads requiring large amounts of memory.

Common Use Cases
Databases
In-memory applications
Real-time data processing
High-performance database systems
Accelerated Computing (AC)

Accelerated Computing instances use hardware accelerators to improve performance.

Common Use Cases
Floating-point calculations
Graphics processing
Machine learning
Data pattern matching
Specialized computing workloads
Hardware Accelerator

A hardware accelerator is a component that improves performance by handling specific computational tasks more efficiently than a standard CPU.

Storage Optimized (SO)

Storage Optimized instances provide high-performance access to locally stored data.

Common Use Cases
Large-scale databases
Data warehousing
High-speed storage workloads
Applications requiring high I/O performance
Amazon EC2
Definition

Amazon EC2 (Elastic Compute Cloud) is a service that provides virtual servers in the AWS cloud.

Benefits
Easy to scale
Reliable
Integrates with other AWS services
Pay-as-you-go pricing model
Amazon Machine Image (AMI)
Definition

An AMI (Amazon Machine Image) is a template used to launch EC2 instances.

It contains:

Operating system
Pre-installed software
Application dependencies
Configuration settings

Benefits:

Faster deployments
Consistent server configurations
Connecting to an EC2 Instance

Once connected to an EC2 instance, users can:

Run commands
Install software
Add storage
Copy files
Manage applications

This provides administrative access to the virtual server.

Networking and Security
Key Pair

A key pair consists of:

Public Key

Stored on the EC2 instance.

Private Key

Stored by the user.

Used together to securely authenticate access to the instance.

Security Group

A Security Group acts as a virtual firewall that controls inbound and outbound traffic to an EC2 instance.

Remote Desktop Protocol (RDP)

RDP (Remote Desktop Protocol) enables users to remotely access and manage Windows-based EC2 instances.

HTTPS

HTTPS (Hypertext Transfer Protocol Secure) provides encrypted communication over the internet.

VPC (Virtual Private Cloud)

A Virtual Private Cloud (VPC) provides an isolated network environment within AWS.

Benefits:

Enhanced security
Network control
Resource isolation
IPS (Intrusion Prevention System)

An Intrusion Prevention System monitors network traffic and helps prevent malicious activity.

TCP (Transmission Control Protocol)

TCP is a communication protocol that ensures reliable transmission of data across networks.

Amazon EBS (Elastic Block Store)
Definition

Amazon EBS provides persistent block storage for EC2 instances.

General Purpose SSD (GP)

General Purpose SSD volumes offer a balance of performance and cost for most workloads.

Launching an EC2 Instance

After creating an EC2 instance:

Wait until the status checks pass successfully.
Verify the instance status indicator turns green.
Download the RDP file (Windows instances).
Use the previously saved key pair.
AWS decrypts the administrator password using the private key.
Connect to the instance.
Managing EC2 Instances
Stop

Stopping an instance:

Shuts down the virtual machine
Preserves the attached EBS volume
Stops compute charges
Storage charges continue
Terminate

Terminating an instance:

Permanently deletes the instance
Removes associated resources (depending on configuration)
Stops all compute charges
Amazon S3 (Simple Storage Service)
Definition

Amazon S3 is AWS's object storage service.

Characteristics:

Stores files as objects
Highly scalable
Cost-effective
Durable and reliable

Examples of stored objects:

Documents
Images
Videos
PDFs
Backups
Buckets

Objects are stored inside containers called buckets.

Bucket Characteristics
Bucket names must be globally unique.
Buckets can be private or public.
Data is accessible worldwide.
Bucket Organization

Buckets can contain:

Files
Folders (logical organization)
Multiple object versions
Access Control
ACL (Access Control List)

ACLs control who can access S3 resources.

Bucket Policies

Policies define permissions for users and services.

Access Point Policies

Provide customized access controls for applications and users.

Important: Be cautious when granting public access.

Bucket Versioning

Versioning allows multiple versions of an object to be stored.

Benefits:

Recover deleted files
Restore previous versions
Protect against accidental overwrites
Encryption

S3 supports encryption for protecting stored data.

Encryption can help prevent unauthorized access and deletion.

EBS vs EFS
EBS (Elastic Block Store)

Characteristics:

Attached to a single EC2 instance
Block-level storage
Not directly accessible through a URL
Typically used by one server at a time
EFS (Elastic File System)

Characteristics:

Shared file storage
Can be mounted by multiple EC2 instances simultaneously
Supports concurrent access
Ideal for shared applications and workloads
Amazon RDS (Relational Database Service)
Definition

Amazon RDS is a managed relational database service.

Relational Database Concepts
Table

Stores related data.

Row (Record)

Represents a single entry in a table.

Column

Represents a data field.

Primary Key

A Primary Key:

Uniquely identifies each record
Cannot contain duplicate values
Foreign Key

A Foreign Key creates relationships between tables.

It links data across multiple tables.

SQL Language Categories
DDL (Data Definition Language)

Used to define database structures.

Examples:

CREATE TABLE
ALTER TABLE
DROP TABLE

Includes:

Table names
Column names
Data types

Example data type:

VARCHAR
DML (Data Manipulation Language)

Used to manage data within tables.

Operations include:

INSERT
UPDATE
DELETE
DCL (Data Control Language)

Used to manage permissions and access controls.

Examples:

Read permissions
Write permissions
Common Database Technologies
Oracle
MySQL
PostgreSQL
DynamoDB
Amazon Redshift
AWS Snow Family

AWS Snow Family devices help transfer large amounts of data between on-premises environments and AWS.

AWS Snowball Edge
Physical device used for data transfer and edge computing.
Allows on-site data processing at no additional charge for compute capabilities.
Useful when network bandwidth is limited.
Amazon Inspector
Definition

Amazon Inspector is a security assessment service that helps identify:

Application vulnerabilities
Infrastructure security issues
Deviations from security best practices

Benefits:

Automated security assessments
Continuous monitoring
Security recommendations
AWS Storage Gateway
File Gateway

AWS Storage Gateway allows on-premises file storage systems to integrate with AWS cloud storage.

Features
Stores files in Amazon S3.
Provides low-latency access to frequently used data.
Maintains local access performance while leveraging cloud storage.
Centralized storage management.
Users can access files as though they are stored locally.
Benefits
Simplifies cloud storage integration.
Eliminates the need to manage separate S3 buckets for each user.
Enables hybrid cloud storage architectures.
Connecting EC2 to an S3 Bucket

To allow an EC2 instance to upload files to an S3 bucket:

Create an IAM role.
Assign the role to the EC2 instance.
Grant the required S3 permissions.
The EC2 instance assumes the role and gains access to upload or retrieve files.
Amazon DynamoDB
Definition

Amazon DynamoDB is a fully managed NoSQL database service.

Shared Responsibility Model

AWS is responsible for:

Managing infrastructure
Availability
Hardware maintenance
Scaling

Customers are responsible for:

Managing access permissions
Authentication mechanisms
Access control policies
Data security configurations

Goal:

Ensure only authorized users and services can access DynamoDB tables.

AWS Cloud Adoption Framework (CAF)

The AWS Cloud Adoption Framework provides guidance for organizations adopting cloud technologies.

Perspectives
Business

Focuses on:

Business strategy
Value realization
Organizational objectives
People

Focuses on:

Organizational roles
Skills development
Change management
Governance

Focuses on:

Budgeting
Risk management
Compliance
Controls
Platform

Focuses on:

Cloud architecture
Infrastructure
AWS services
Security

Focuses on:

Data protection
Security controls
Compliance requirements
Operations

Focuses on:

Monitoring
Operational excellence
Day-to-day management
AWS Fargate
Definition

AWS Fargate is a serverless compute engine for containers.

It works with:

Amazon ECS
Amazon EKS
Benefits
No server management
No cluster management
Automatic scaling
Pay only for resources used

Users focus on containers while AWS manages the infrastructure.

AWS Lambda
Definition

AWS Lambda is a serverless computing service that enables developers to run code without provisioning or managing servers.

Benefits:

Automatic scaling
Event-driven execution
Reduced operational overhead
Amazon RDS
Definition

Amazon RDS (Relational Database Service) is a fully managed relational database service.

AWS handles:

Hardware provisioning
Database maintenance
Backups
Patching
Availability
Amazon Athena
Definition

Amazon Athena is an interactive query service.

Features
Queries data directly in Amazon S3.
Uses standard SQL.
No infrastructure management required.

Benefits:

Fast data analysis
Serverless architecture
Cost-effective analytics
Cost Explorer
Definition

AWS Cost Explorer provides detailed cost and usage reporting.

Features
Cost analysis
Usage tracking
Spending trends
Forecasting

Benefits:

Better budgeting
Cost visibility
Usage optimization
AWS Compute Optimizer
Definition

AWS Compute Optimizer analyzes workloads and recommends optimal AWS resources.

Benefits
Improved performance
Reduced costs
Resource right-sizing

Examples:

EC2 recommendations
EBS recommendations
Lambda recommendations
AWS Trusted Advisor
Definition

AWS Trusted Advisor provides recommendations to improve AWS environments.

Areas of Focus
Cost Optimization
Identifies underutilized resources
Helps reduce unnecessary spending
Security
Detects security risks
Monitors configurations
Performance
Improves resource efficiency
Recommends performance enhancements
Reliability
Increases application resilience
Identifies potential failures
Amazon EC2 Auto Scaling
Definition

Amazon EC2 Auto Scaling automatically adjusts the number of EC2 instances based on demand.

Scalability

Scalability is the ability of an application to automatically respond to changing demand by scaling resources in or out.

Auto Scaling Policies
Dynamic Scaling

Automatically adjusts capacity based on real-time demand and performance metrics.

Predictive Scaling

Uses historical usage patterns to forecast demand and proactively launch instances.

Auto Scaling Group (ASG)

An Auto Scaling Group manages EC2 instances and maintains desired capacity levels.

Capacity Settings
Minimum Capacity

Minimum number of EC2 instances that must always remain running.

Desired Capacity

Target number of EC2 instances that Auto Scaling attempts to maintain.

Maximum Capacity

Maximum number of EC2 instances that can be launched during increased demand.

Elastic Load Balancing (ELB)
Definition

Elastic Load Balancing automatically distributes incoming traffic across multiple EC2 instances.

Benefits:

High availability
Fault tolerance
Improved performance
Relationship Between ELB and Auto Scaling

ELB acts as the single entry point for incoming traffic.

Auto Scaling adjusts the number of EC2 instances based on demand.

Together they provide:

Scalability
High availability
Performance optimization
Monolithic Architecture

In a monolithic application:

All application components are tightly coupled.
Components depend heavily on one another.
A failure in one component can affect the entire application.

Examples of components:

User Interface
Business Logic
Databases
Backend Services
Microservices Architecture

In a microservices architecture:

Components are loosely coupled.
Services operate independently.
Individual services communicate through APIs or messaging systems.

Benefits:

Better fault isolation
Independent deployment
Improved scalability

If one service fails, the remaining services can often continue functioning.

Amazon SNS (Simple Notification Service)
Definition

Amazon SNS is a publish-subscribe messaging service.

Components
Publisher

Sends messages to a topic.

Topic

A communication channel that receives published messages.

Subscriber

Receives messages from a topic.

Subscribers may include:

Email addresses
Web servers
AWS Lambda functions
Mobile applications
SNS Example

A coffee shop newsletter system:

Single Newsletter

Customers receive updates about:

Company news
Coffee trivia
New products
Topic-Based Newsletters

Separate topics are created for:

Company updates
Coffee trivia
New products

Customers subscribe only to topics they are interested in.

Benefits:

Targeted communication
Reduced unnecessary notifications
Amazon SQS (Simple Queue Service)
Definition

Amazon SQS is a managed message queuing service.

Purpose

Allows applications and services to exchange messages asynchronously.

How It Works
An application sends a message to a queue.
The message remains in the queue until processed.
A service retrieves the message.
The service processes the message.
The message is deleted from the queue.
Benefits
Decouples applications
Improves reliability
Prevents message loss
Supports scalable architectures
Serverless Computing
Traditional EC2-Based Deployment

To run an application:

Provision EC2 instances.
Deploy application code.
Manage infrastructure while the application runs.
Serverless Deployment

With serverless computing:

Code still runs on servers.
AWS manages the servers.
Developers focus only on application code.
Benefits
No server management
Automatic scaling
Faster development
Reduced operational effort

Serverless applications can automatically adjust resources such as:

Compute power
Memory
Throughput

based on workload demand.
