Networking is one of the biggest CLF-C02 sections because AWS loves testing whether you know **Internet vs Private vs Hybrid vs Global networking**.

Here are the most useful network questions from your zip along with the elimination tricks.

---

# Q30 — Dedicated Private Connection

> A company needs a dedicated private network connection between its on-premises data center and AWS.

A. VPN
B. Direct Connect ✅
C. Transit Gateway
D. Route 53

### Why?

**AWS Direct Connect** = dedicated physical connection.

### Eliminate

| Service         | Why Wrong                    |
| --------------- | ---------------------------- |
| VPN             | Uses internet                |
| Transit Gateway | Connects networks inside AWS |
| Route 53        | DNS                          |

### Exam Trigger

**Dedicated**, **private circuit**, **consistent bandwidth**

→ Direct Connect

---

# Q84 — Connect Multiple VPCs

> Connect many VPCs together using a hub-and-spoke model.

A. Internet Gateway
B. Transit Gateway ✅
C. NAT Gateway
D. Route 53

### Why?

Transit Gateway acts as a central router.

### Exam Trigger

**Many VPCs**
**Hub and spoke**
**Centralized connectivity**

→ Transit Gateway

---

# Q95 — Public Internet Access

> Which component allows resources in a VPC to communicate with the internet?

A. NAT Gateway
B. Transit Gateway
C. Internet Gateway ✅
D. Direct Connect

### Why?

Internet Gateway provides internet access.

### Common Trap

Students confuse:

* Internet Gateway
* NAT Gateway

### Memory

**Internet Gateway = inbound + outbound internet**

---

# Q122 — Private Instances Need Updates

> Private EC2 instances need internet access to download updates.

A. Internet Gateway
B. NAT Gateway ✅
C. Route 53
D. VPN

### Why?

Private instances can't have public IPs.

NAT Gateway allows:

* Outbound internet
* No inbound internet

### Exam Trigger

**Private subnet**
**Need internet access**
**Download patches**

→ NAT Gateway

---

# Q141 — DNS Service

> Which AWS service routes users to applications using domain names?

A. Route 53 ✅
B. CloudFront
C. Direct Connect
D. Transit Gateway

### Why?

Route 53 = DNS.

### Exam Trigger

**DNS**
**Domain names**
**Route traffic**

→ Route 53

---

# Q186 — Global Content Delivery

> Deliver content to users worldwide with low latency.

A. Route 53
B. CloudFront ✅
C. Direct Connect
D. VPC

### Why?

CloudFront caches content at edge locations.

### Exam Trigger

**Low latency**
**Global users**
**Content delivery**

→ CloudFront

---

# Q290 — DDoS Protection

> Which service protects applications from DDoS attacks?

A. GuardDuty
B. CloudTrail
C. Shield ✅
D. Inspector

### Why?

AWS Shield provides DDoS protection.

### Memory Tip

**Shield protects**

---

# Q345 — Filter Network Traffic

> Which AWS feature acts as a virtual firewall for EC2 instances?

A. NACL
B. Security Group ✅
C. Route Table
D. Transit Gateway

### Why?

Security Groups are instance-level firewalls.

### Exam Trigger

**EC2 firewall**

→ Security Group

---

# Q348 — Subnet-Level Filtering

> Which feature controls traffic entering and leaving a subnet?

A. Security Group
B. NACL ✅
C. Route Table
D. Direct Connect

### Why?

NACL = subnet firewall.

### Super Common Exam Pair

| Feature        | Scope    |
| -------------- | -------- |
| Security Group | Instance |
| NACL           | Subnet   |

---

# Q526 — Hybrid Connectivity

> Extend an on-premises network into AWS securely over the internet.

A. Direct Connect
B. VPN ✅
C. Transit Gateway
D. Route 53

### Why?

VPN uses encrypted tunnels over the internet.

### Exam Trigger

**Secure**
**Internet**
**Hybrid connectivity**

→ VPN

---

# The Most Important Networking Distinctions

## Internet Gateway vs NAT Gateway

### Internet Gateway

Question says:

* Public subnet
* Internet access
* Public web server

→ Internet Gateway

---

### NAT Gateway

Question says:

* Private subnet
* Download updates
* Outbound only

→ NAT Gateway

---

## Direct Connect vs VPN

### Direct Connect

Question says:

* Dedicated connection
* Consistent performance
* Private circuit

→ Direct Connect

---

### VPN

Question says:

* Encrypted
* Uses internet
* Quick setup

→ VPN

---

## Security Group vs NACL

### Security Group

* Instance level
* Stateful

Think:

> Firewall attached to EC2

---

### NACL

* Subnet level
* Stateless

Think:

> Firewall attached to subnet

---

# High-Yield CLF-C02 Network Cheat Sheet

| Keyword                            | Answer                |
| ---------------------------------- | --------------------- |
| DNS                                | Route 53              |
| CDN                                | CloudFront            |
| Dedicated connection               | Direct Connect        |
| Encrypted connection over internet | VPN                   |
| Public internet access             | Internet Gateway      |
| Private subnet internet access     | NAT Gateway           |
| Connect many VPCs                  | Transit Gateway       |
| EC2 firewall                       | Security Group        |
| Subnet firewall                    | NACL                  |
| DDoS protection                    | Shield                |
| Global AWS backbone network        | Global Infrastructure |
| Edge caching                       | CloudFront            |

---

### My favorite memory picture

```text
Internet
    |
Internet Gateway
    |
Public Subnet
    |
ALB
    |
Private Subnet
    |
EC2
    |
NAT Gateway ---> Internet (outbound only)

On-Prem
    |
 VPN or Direct Connect
    |
 Transit Gateway
    |
 Multiple VPCs

Route53 ---> Finds application
CloudFront ---> Delivers content faster
Shield ---> Protects from DDoS
```

If you can visualize that diagram, you'll answer most CLF-C02 networking questions without memorizing definitions.
