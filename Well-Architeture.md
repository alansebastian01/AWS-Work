## AWS Well-Architected Framework Questions & Tips (from the ZIP)

---

### Q30

**Which pillar of the AWS Well-Architected Framework focuses on using computing resources efficiently to meet system requirements?**

A. Reliability
B. Security
✅ **C. Performance Efficiency**
D. Operational Excellence

**Tip:** Performance Efficiency = choosing the right resources and technologies.

---

### Q52

**Which AWS Well-Architected Framework pillar focuses on recovering quickly from failures?**

A. Security
✅ **B. Reliability**
C. Sustainability
D. Cost Optimization

**Tip:** Reliability = backup, recovery, fault tolerance, disaster recovery.

---

### Q86

**A company wants to improve its ability to support development and run workloads effectively. Which Well-Architected pillar should it focus on?**

✅ **A. Operational Excellence**
B. Security
C. Reliability
D. Sustainability

**Tip:** Operational Excellence = run, monitor, improve processes continuously.

---

### Q108

**Which AWS Well-Architected Framework pillar focuses on protecting information, systems, and assets?**

A. Reliability
✅ **B. Security**
C. Cost Optimization
D. Sustainability

**Tip:** IAM, encryption, auditing, least privilege → Security pillar.

---

### Q120

**Which Well-Architected Framework pillar focuses on avoiding unnecessary costs?**

A. Reliability
B. Security
✅ **C. Cost Optimization**
D. Operational Excellence

**Tip:** Right-size resources, eliminate waste, monitor spending.

---

### Q146

**A company wants to minimize environmental impacts from running workloads in AWS. Which pillar should it focus on?**

A. Reliability
B. Security
C. Performance Efficiency
✅ **D. Sustainability**

**Tip:** Sustainability is the newest pillar. Focus on energy-efficient workloads.

---

### Q211

**Which AWS Well-Architected Framework pillar includes workload monitoring and continuous improvement?**

✅ **A. Operational Excellence**
B. Security
C. Reliability
D. Cost Optimization

**Tip:** Monitoring + automation + improvement = Operational Excellence.

---

### Q348

**Which Well-Architected Framework pillar focuses on protecting data while it is stored and in transit?**

A. Reliability
✅ **B. Security**
C. Sustainability
D. Performance Efficiency

**Tip:** Encryption at rest and in transit are Security pillar topics.

---

### Q401

**Which Well-Architected Framework pillar helps ensure a workload can automatically recover from infrastructure failures?**

A. Security
✅ **B. Reliability**
C. Cost Optimization
D. Sustainability

**Tip:** Auto Recovery, Multi-AZ, backups → Reliability.

---

## AWS Well-Architected Framework Pillars

### 1. Operational Excellence

**Keywords**

* Monitoring
* Automation
* Continuous improvement
* Operations

**Real-world Example**
Amazon continuously monitors application logs using CloudWatch and automatically fixes issues.

**Exam Clue**
If you see:

* Improve operations
* Run workloads efficiently
* Monitoring

➡️ **Operational Excellence**

---

### 2. Security

**Keywords**

* IAM
* Encryption
* Least privilege
* Data protection
* Audit

**Real-world Example**
A bank encrypts customer data in S3 and controls access using IAM roles.

**Exam Clue**
If you see:

* Protect data
* Permissions
* Encryption

➡️ **Security**

---

### 3. Reliability

**Keywords**

* Recovery
* Failover
* Backup
* Disaster recovery
* Availability

**Real-world Example**
A website runs across multiple Availability Zones so it stays online if one AZ fails.

**Exam Clue**
If you see:

* Recover quickly
* Fault tolerance
* Backup

➡️ **Reliability**

---

### 4. Performance Efficiency

**Keywords**

* Right resource selection
* Scalability
* Efficient computing

**Real-world Example**
Using Auto Scaling to add EC2 instances during peak traffic.

**Exam Clue**
If you see:

* Efficient resource usage
* Scalability
* Performance

➡️ **Performance Efficiency**

---

### 5. Cost Optimization

**Keywords**

* Reduce cost
* Eliminate waste
* Right sizing

**Real-world Example**
Moving infrequently accessed data to S3 Glacier.

**Exam Clue**
If you see:

* Save money
* Lower costs
* Optimize spending

➡️ **Cost Optimization**

---

### 6. Sustainability

**Keywords**

* Environmental impact
* Energy efficiency
* Carbon footprint

**Real-world Example**
Using serverless services such as Lambda instead of idle EC2 servers.

**Exam Clue**
If you see:

* Environment
* Green computing
* Carbon reduction

➡️ **Sustainability**

---

## Ultimate Memory Trick

| Pillar                 | Remember       |
| ---------------------- | -------------- |
| Operational Excellence | Run Better     |
| Security               | Protect Better |
| Reliability            | Recover Better |
| Performance Efficiency | Perform Better |
| Cost Optimization      | Spend Less     |
| Sustainability         | Save Energy    |

### Exam Shortcut

**Recover?** → Reliability
**Protect?** → Security
**Monitor?** → Operational Excellence
**Scale?** → Performance Efficiency
**Save Money?** → Cost Optimization
**Save Environment?** → Sustainability

These are the Well-Architected Framework topics that repeatedly appear in CLF-C02 practice exams and in your ZIP file.
