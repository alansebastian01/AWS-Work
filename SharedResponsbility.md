Here are the **Shared Responsibility Model questions from your CLF-C02 zip** that are worth memorizing, along with elimination tricks for the wrong answers.

---

# Q5

> Which option is a customer responsibility when using Amazon DynamoDB?

A. Physical security of DynamoDB
B. Patching of DynamoDB
C. Access to DynamoDB tables ✅
D. Encryption of data at rest in DynamoDB

### Why C?

Customers control who can access their data (IAM policies, permissions).

### Elimination Tips

| Option             | Why Wrong                                     |
| ------------------ | --------------------------------------------- |
| Physical security  | AWS responsibility                            |
| Patching DynamoDB  | AWS responsibility (managed service)          |
| Encryption at rest | Enabled/managed by AWS by default in DynamoDB |

**Exam trigger:** "Access control" → Customer.

---

# Q8

> Running a NoSQL database on EC2. What is AWS responsible for?

A. Update guest OS
B. Database HA
C. Patch physical infrastructure hosting EC2 ✅
D. Configure security groups

### Why C?

AWS manages the hardware and facilities.

### Quick Rule

**EC2 = Customer manages OS, AWS manages hardware.**

---

# Q243

> Which maintenance task is the customer's responsibility?

A. Physical connectivity between AZs
B. Network switch maintenance
C. Hardware updates and firmware patches
D. Amazon EC2 updates and security patches ✅

### Why D?

Anything inside your EC2 instance = customer responsibility.

### Memory Trick

**EC2 = You patch it.**

---

# Q249

> Which option is a shared control?

A. Configuration management ✅
B. Physical and environmental controls
C. Data integrity authentication
D. Identity and access management

### Why A?

AWS provides tools; customer configures them.

### Exam Shortcut

| AWS                     | Customer | Shared                   |
| ----------------------- | -------- | ------------------------ |
| Physical infrastructure | Data     | Configuration management |

---

# Q282

> Customer responsibilities? (Choose two)

A. Configure infrastructure devices
B. Hardware patching
C. Configure guest OS and applications ✅
D. Encryption decisions ✅
E. Infrastructure hardware

### Correct

✅ C
✅ D

### Memory Trick

Customer controls:

* OS
* Applications
* Data
* Encryption choices
* IAM

AWS controls:

* Hardware
* Facilities
* Networking

---

# Q293

> Customer applies security patches to:

A. DynamoDB
B. EC2 instances ✅
C. RDS
D. S3

### Why B?

EC2 is IaaS.

### Elimination

| Service  | Patching |
| -------- | -------- |
| EC2      | Customer |
| RDS      | AWS      |
| DynamoDB | AWS      |
| S3       | AWS      |

---

# Q297

> Who rotates IAM access keys?

A. No rotation needed
B. Customer ✅
C. AWS automatically rotates
D. AWS Support rotates

### Why B?

IAM users and credentials are always customer-managed.

### Exam Trigger

"Users, passwords, keys, MFA" → Customer.

---

# Q300

> Entirely AWS responsibility?

A. Security awareness training
B. IAM password policy
C. Guest OS patching
D. Physical and environmental controls ✅

### Why D?

This is classic "security OF the cloud."

### Memory Trick

If you can physically touch it → AWS.

---

# Q334

> AWS responsibility?

A. Encrypt application data
B. Authenticate application users
C. Protect physical network infrastructure ✅
D. Configure firewalls

### Why C?

Infrastructure protection is AWS.

### Eliminate

Application-related = usually customer.

---

# Q384

> AWS responsibility?

A. Application data security
B. Application patching on EC2
C. Patch underlying infrastructure for managed services ✅
D. Application IAM

### Why C?

Managed service infrastructure is AWS-owned.

### Exam Trigger

**Managed service → AWS patches.**

---

# Q434

> AWS Lambda responsibilities (Choose two)

A. Manage infrastructure
B. Manage OS
C. Write business logic code ✅
D. Install runtime
E. IAM access to Lambda ✅

### Correct

✅ C
✅ E

### Lambda Rule

AWS manages:

* Servers
* OS
* Runtime

Customer manages:

* Code
* Permissions

---

# Q437

> What is "security OF the cloud"?

A. Availability of EC2
B. Security of AWS infrastructure running services ✅
C. Password policies
D. Customer firewall configuration

### Why B?

This is the exact AWS definition.

---

# Ultimate CLF-C02 Cheat Sheet

### AWS is responsible for:

✅ Data centers
✅ Physical security
✅ Servers
✅ Storage hardware
✅ Networking hardware
✅ Hypervisor
✅ Managed-service patching (RDS, DynamoDB, S3)

---

### Customer is responsible for:

✅ Data
✅ IAM users/roles
✅ Passwords & access keys
✅ MFA
✅ Security groups & NACLs
✅ EC2 OS patching
✅ EC2 applications
✅ Encryption configuration decisions

---

### Fast Exam Mnemonic

**Security OF the Cloud = AWS**

* Buildings
* Hardware
* Network
* Hypervisor

**Security IN the Cloud = Customer**

* Data
* IAM
* OS
* Applications
* Configurations

For CLF-C02, about 90% of Shared Responsibility questions can be answered by first identifying whether the service is **EC2 (customer patches)** or a **managed service like RDS/DynamoDB/S3 (AWS patches)**.
