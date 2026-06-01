For the **AWS Certified Cloud Practitioner (CLF-C02)** exam, you should know AWS services **with practical real-world use cases**, not just definitions. Here are the most important services and easy-to-remember examples.

# 1. Compute Services

### Amazon EC2

**What it is:** Virtual server in the cloud.

**Real-world example:**
A company hosts its e-commerce website on EC2 instances.

* Website traffic comes to EC2.
* During Black Friday, more EC2 instances are added automatically.

**Exam keyword:** Virtual Machine (VM)

---

### AWS Lambda

**What it is:** Run code without managing servers.

**Real-world example:**
When a customer uploads a profile picture, Lambda automatically resizes the image.

**Exam keyword:** Serverless

---

# 2. Storage Services

### Amazon S3

**What it is:** Stores files, images, videos, backups.

**Real-world example:**
Netflix-like application stores movies in S3.

* Unlimited scalability
* High durability (11 nines)

**Exam keyword:** Object Storage

---

### Amazon EBS

**What it is:** Hard disk attached to EC2.

**Real-world example:**
Database running on EC2 stores data on EBS volumes.

**Exam keyword:** Block Storage

---

### Amazon EFS

**What it is:** Shared file storage.

**Real-world example:**
Multiple EC2 servers access the same files.

**Exam keyword:** Shared Storage

---

# 3. Database Services

### Amazon RDS

**What it is:** Managed SQL database.

**Real-world example:**
Online banking application uses MySQL/PostgreSQL on RDS.

AWS handles:

* Backups
* Patching
* Maintenance

**Exam keyword:** Relational Database

---

### Amazon DynamoDB

**What it is:** NoSQL database.

**Real-world example:**
Gaming application stores player scores.

**Exam keyword:** NoSQL

---

# 4. Networking Services

### Amazon VPC

**What it is:** Private network in AWS.

**Real-world example:**
A bank creates isolated networks for applications and databases.

**Exam keyword:** Network Isolation

---

### Elastic Load Balancing

**What it is:** Distributes traffic across servers.

**Real-world example:**
1 million users visit a website.
Load Balancer distributes requests across many EC2 servers.

**Exam keyword:** High Availability

---

### Amazon Route 53

**What it is:** DNS service.

**Real-world example:**
When users type amazon.com, Route 53 directs them to the correct server.

**Exam keyword:** DNS

---

# 5. Security Services

### AWS IAM

**What it is:** User permissions.

**Real-world example:**
Developers can deploy applications but cannot delete databases.

**Exam keyword:** Least Privilege

---

### AWS KMS

**What it is:** Encryption key management.

**Real-world example:**
Customer data stored in S3 is encrypted using KMS keys.

**Exam keyword:** Encryption

---

# 6. Monitoring Services

### Amazon CloudWatch

**What it is:** Monitoring service.

**Real-world example:**
CPU utilization reaches 90%.
CloudWatch sends an alert to administrators.

**Exam keyword:** Metrics and Monitoring

---

### AWS CloudTrail

**What it is:** Tracks AWS activities.

**Real-world example:**
Security team checks who deleted an EC2 instance.

**Exam keyword:** Audit Logs

---

# 7. Migration Services

### AWS Database Migration Service

**What it is:** Migrates databases to AWS.

**Real-world example:**
Move Oracle database from on-premises to AWS RDS.

**Exam keyword:** Migration

---

# 8. Cost Management Services

### AWS Cost Explorer

**What it is:** Analyze AWS spending.

**Real-world example:**
Finance team checks which service generated the highest bill.

---

### AWS Budgets

**What it is:** Budget alerts.

**Real-world example:**
Send email when monthly spending exceeds $1000.

---

# Exam Memory Trick

| Requirement    | AWS Service |
| -------------- | ----------- |
| Virtual Server | EC2         |
| Serverless     | Lambda      |
| File Storage   | S3          |
| Disk for EC2   | EBS         |
| Shared Files   | EFS         |
| SQL Database   | RDS         |
| NoSQL Database | DynamoDB    |
| Network        | VPC         |
| DNS            | Route 53    |
| Load Balancer  | ELB         |
| Permissions    | IAM         |
| Monitoring     | CloudWatch  |
| Auditing       | CloudTrail  |
| Encryption     | KMS         |
| Migration      | DMS         |

### Most Important Services for Cloud Practitioner

Focus heavily on:

1. S3
2. EC2
3. Lambda
4. RDS
5. DynamoDB
6. VPC
7. IAM
8. CloudWatch
9. CloudTrail
10. Route 53

These 10 services alone typically cover a large portion of service-related questions in the Cloud Practitioner exam.
