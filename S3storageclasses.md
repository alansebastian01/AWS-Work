I found the **S3 storage-class questions** in your CLF-C02 zip. Here are the questions, the correct answer, and how to quickly eliminate the distractors.

---

# Q201

> Data is not frequently accessed. If needed, retrieval can take up to **12 hours**. Want the most cost-effective storage.

**A. S3 Standard**
**B. S3 Glacier Flexible Retrieval ✅**
**C. S3 One Zone-IA**
**D. S3 Standard-IA**

### Why B?

The key phrase is **"retrieved within 12 hours"**. Glacier Flexible Retrieval is designed for archival data where retrieval can take minutes to hours.

### Why not the others?

| Option      | Elimination Tip                                                    |
| ----------- | ------------------------------------------------------------------ |
| Standard    | For frequent access                                                |
| One Zone-IA | Immediate retrieval, not archive                                   |
| Standard-IA | Immediate retrieval, costs more than Glacier for archive workloads |

**Exam trigger:** "Hours are acceptable" → Glacier Flexible Retrieval.

---

# Q251

> Data is rarely accessed and **can be regenerated** if necessary. Most cost-effective.

**A. S3 Standard**
**B. S3 Intelligent-Tiering**
**C. S3 Standard-IA**
**D. S3 One Zone-IA ✅**

### Why D?

The phrase **"can be regenerated"** means losing a copy is acceptable. One Zone-IA stores data in a single AZ for lower cost.

### Why not the others?

| Option              | Elimination Tip              |
| ------------------- | ---------------------------- |
| Standard            | Too expensive                |
| Intelligent-Tiering | Access pattern already known |
| Standard-IA         | Multi-AZ costs more          |

**Exam trigger:** "Re-creatable data" → One Zone-IA.

---

# Q294

> Most cost-effective for **unknown access patterns**

**A. Standard**
**B. Standard-IA**
**C. One Zone-IA**
**D. Intelligent-Tiering ✅**

### Why D?

This is the textbook use case.

### Why not others?

| Option      | Elimination Tip                                |
| ----------- | ---------------------------------------------- |
| Standard    | Doesn't optimize costs                         |
| Standard-IA | Assumes infrequent access                      |
| One Zone-IA | Assumes infrequent access and lower durability |

**Exam trigger:** "Unknown" = Intelligent-Tiering.

---

# Q349

> What does Intelligent-Tiering offer?

**A. Reserved storage capacity**
**B. Copies to EBS**
**C. Automatically moves objects between tiers ✅**
**D. Lowest-cost archival storage**

### Why C?

That's literally the purpose of Intelligent-Tiering.

### Distractor tips

| Option | Why Wrong                             |
| ------ | ------------------------------------- |
| A      | Sounds like Reserved Instances        |
| B      | S3 doesn't automatically copy to EBS  |
| D      | That's Glacier Deep Archive territory |

---

# Q446

> Auditors access data only **twice a year**. Lowest cost.

**A. S3 Outposts**
**B. Glacier Instant Retrieval ✅**
**C. Standard**
**D. Intelligent-Tiering**

### Why B?

Very rare access but retrieval must still be immediate.

### Why not others?

| Option              | Why Wrong                                                   |
| ------------------- | ----------------------------------------------------------- |
| Outposts            | On-premises S3, not storage class optimization              |
| Standard            | Too expensive                                               |
| Intelligent-Tiering | More expensive than Glacier when access is predictably rare |

**Exam trigger:** Rare access + immediate retrieval → Glacier Instant Retrieval.

---

# Q453

> Some data accessed daily, some yearly.

**A. Standard**
**B. Glacier Deep Archive**
**C. One Zone-IA**
**D. Intelligent-Tiering ✅**

### Why D?

Mixed access patterns.

### Why not others?

| Option       | Why Wrong                                 |
| ------------ | ----------------------------------------- |
| Standard     | Doesn't optimize costs                    |
| Deep Archive | Yearly data okay, daily data not          |
| One Zone-IA  | Doesn't handle mixed access automatically |

**Exam trigger:** Mixed/unknown access → Intelligent-Tiering.

---

# Q607

> Audio files rarely accessed but **must be retrieved immediately**.

**A. Standard**
**B. Standard-IA ✅**
**C. Glacier Flexible Retrieval**
**D. Glacier Deep Archive**

### Why B?

Rare access + millisecond retrieval.

### Why not others?

| Option           | Why Wrong               |
| ---------------- | ----------------------- |
| Standard         | Frequent-access pricing |
| Glacier Flexible | Retrieval delay         |
| Deep Archive     | Hours retrieval         |

**Exam trigger:** Infrequent + immediate retrieval → Standard-IA.

---

# Q700

> Need object storage access in **single-digit milliseconds**.

**A. S3 Express One Zone ✅**
**B. S3 Standard**
**C. Glacier Flexible Retrieval**
**D. Glacier Instant Retrieval**

### Why A?

This is the marketing phrase AWS uses for S3 Express One Zone.

### Why not others?

| Option           | Why Wrong                                           |
| ---------------- | --------------------------------------------------- |
| Standard         | Fast, but not the special ultra-low-latency service |
| Glacier Flexible | Minutes/hours retrieval                             |
| Glacier Instant  | Immediate retrieval but not Express performance     |

**Exam trigger:** "Single-digit milliseconds" → S3 Express One Zone.

---

# CLF-C02 S3 Storage Class Cheat Sheet

| Question Phrase                       | Answer                                   |
| ------------------------------------- | ---------------------------------------- |
| Unknown access pattern                | Intelligent-Tiering                      |
| Mixed daily/yearly access             | Intelligent-Tiering                      |
| Re-creatable data                     | One Zone-IA(Infrequent Access)           |
| Rarely accessed + immediate retrieval | Standard-IA or Glacier Instant Retrieval |
| Archive + retrieval in hours          | Glacier Flexible Retrieval               |
| Long-term archive                     | Glacier Deep Archive                     |
| Lowest archive cost                   | Glacier Deep Archive                     |
| Single-digit millisecond access       | S3 Express One Zone                      |
| Frequent access                       | Standard                                 |

A lot of CLF-C02 questions can be answered by spotting just one keyword: **unknown, archive, immediate retrieval, re-creatable, or single-digit milliseconds**.
