The **database questions** on CLF-C02 are usually less about deep database knowledge and more about matching the workload to the AWS service.

# Q14 — Relational Database

> Which AWS service is a fully managed relational database service?

A. DynamoDB
B. RDS ✅
C. Redshift
D. ElastiCache

### Why?

RDS supports:

* MySQL
* PostgreSQL
* MariaDB
* Oracle
* SQL Server

### Eliminate

| Service     | Type           |
| ----------- | -------------- |
| DynamoDB    | NoSQL          |
| Redshift    | Data warehouse |
| ElastiCache | Cache          |

### Exam Trigger

**Relational database** → **RDS**

---

# Q72 — High Performance NoSQL

> Need a highly available NoSQL database with single-digit millisecond latency.

A. Aurora
B. DynamoDB ✅
C. Redshift
D. Neptune

### Why?

DynamoDB is AWS's flagship NoSQL service.

### Exam Trigger

**NoSQL** → **DynamoDB**

---

# Q130 — Data Warehouse

> Analyze petabytes of business data using SQL.

A. RDS
B. DynamoDB
C. Redshift ✅
D. ElastiCache

### Why?

Redshift = Data warehouse.

### Common Trap

| Service  | Purpose          |
| -------- | ---------------- |
| RDS      | OLTP             |
| Redshift | Analytics / OLAP |

### Exam Trigger

**Business analytics**, **petabytes**, **warehouse** → **Redshift**

---

# Q165 — Graph Relationships

> Store relationships between users and products.

A. DynamoDB
B. Neptune ✅
C. RDS
D. Redshift

### Why?

Neptune is the graph database.

### Keywords

* Relationships
* Social networks
* Recommendation graphs
* Connected data

### Exam Trigger

**Graph database** → **Neptune**

---

# Q184 — In-Memory Performance

> Improve application performance by caching frequently accessed data.

A. Aurora
B. ElastiCache ✅
C. DynamoDB
D. Redshift

### Why?

ElastiCache supports:

* Redis
* Memcached

### Exam Trigger

**Cache**, **reduce latency** → **ElastiCache**

---

# Q248 — Time-Series Data

> Store IoT sensor data and time-series metrics.

A. Timestream ✅
B. RDS
C. Neptune
D. Redshift

### Why?

Timestream is built specifically for time-series workloads.

### Keywords

* IoT
* Metrics
* Monitoring
* Sensor readings

### Exam Trigger

**Time-series** → **Timestream**

---

# Q352 — Fastest Relational Database

> Which relational database combines enterprise database capabilities with cloud scalability?

A. DynamoDB
B. Aurora ✅
C. Redshift
D. Neptune

### Why?

Aurora is AWS's cloud-native relational database.

### Common Exam Trick

Both are relational:

* RDS = managed relational DB
* Aurora = AWS-optimized relational DB

### Memory Tip

If they mention:

* Higher performance
* MySQL/PostgreSQL compatibility
* AWS-built relational database

→ Aurora

---

# Q527 — Key-Value Database

> Fully managed key-value database.

A. DynamoDB ✅
B. Aurora
C. Neptune
D. Redshift

### Why?

DynamoDB = Key-value + document database.

---

# Q575 — Database Compatibility

> Existing MySQL application with minimal code changes.

A. Neptune
B. DynamoDB
C. Aurora MySQL-Compatible ✅
D. Redshift

### Why?

Aurora supports MySQL compatibility.

### Exam Trigger

**Minimal code changes from MySQL** → Aurora MySQL

---

# High-Yield Database Elimination Table

| Service     | Remember This                                  |
| ----------- | ---------------------------------------------- |
| RDS         | Traditional relational database                |
| Aurora      | AWS-built high-performance relational database |
| DynamoDB    | NoSQL, key-value, document                     |
| Redshift    | Data warehouse, analytics                      |
| ElastiCache | Cache                                          |
| Neptune     | Graph database                                 |
| Timestream  | Time-series database                           |
| DocumentDB  | MongoDB-compatible document database           |
| QLDB        | Immutable ledger database                      |

---

# Rare Database Questions

## DocumentDB

Question:

> Need MongoDB compatibility.

✅ DocumentDB

**Keyword:** MongoDB

---

## QLDB

Question:

> Need immutable transaction history.

✅ QLDB

**Keyword:** Ledger, audit trail, immutable

### Tip

Think:

* Blockchain without cryptocurrency
* Financial records
* Audit logs

---

# CLF-C02 Database Cheat Sheet

| Question Says          | Answer      |
| ---------------------- | ----------- |
| Relational DB          | RDS         |
| AWS relational DB      | Aurora      |
| NoSQL                  | DynamoDB    |
| Key-value              | DynamoDB    |
| Data warehouse         | Redshift    |
| Analytics on petabytes | Redshift    |
| Cache                  | ElastiCache |
| Graph relationships    | Neptune     |
| Time-series metrics    | Timestream  |
| MongoDB compatible     | DocumentDB  |
| Immutable ledger       | QLDB        |

### Fast Memory Trick

**R-A-D-R-E-N-T-D-Q**

* **RDS** = Relational
* **Aurora** = Advanced Relational
* **DynamoDB** = NoSQL
* **Redshift** = Warehouse
* **ElastiCache** = Cache
* **Neptune** = Graph
* **Timestream** = Time-series
* **DocumentDB** = MongoDB
* **QLDB** = Ledger

For CLF-C02, if you can instantly identify **Relational vs NoSQL vs Warehouse vs Cache vs Graph**, you'll get almost every database question right.
