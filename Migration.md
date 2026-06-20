Yes. AWS migration questions are often solved by spotting **one or two keywords**. Here's a cheat sheet that works very well for the exam.

## Rehost (Lift and Shift)

**Keywords:**

* No changes
* Minimal changes
* Quickly migrate
* Existing application
* As-is
* Lift and shift

**Examples:**

* On-prem VM → EC2
* Windows server → EC2

**Exam clue:**

> "The company does not want to modify the application."

✅ **Rehost**

---

## Replatform (Lift, Tinker, and Shift)

**Keywords:**

* Managed service
* Minor optimization
* Little code change
* Reduce administration
* Managed database

**Examples:**

* MySQL → Amazon RDS for MySQL
* Self-managed PostgreSQL → Amazon RDS PostgreSQL

**Exam clue:**

> "Move to a managed database service."

✅ **Replatform**

---

## Refactor / Re-architect

**Keywords:**

* Redesign
* Cloud-native
* Microservices
* Serverless
* Improve scalability
* Modernize application

**Examples:**

* Monolith → Microservices
* EC2 application → Lambda

**Exam clue:**

> "Take advantage of cloud-native features."

✅ **Refactor**

---

## Repurchase

**Keywords:**

* SaaS
* Replace application
* Salesforce
* Workday
* ServiceNow
* New commercial software

**Examples:**

* Legacy CRM → Salesforce
* On-prem HR system → Workday

**Exam clue:**

> "Replace the existing application."

✅ **Repurchase**

---

## Retire

**Keywords:**

* No longer needed
* Unused application
* Decommission
* Eliminate workload

**Examples:**

* Old reporting server no one uses

✅ **Retire**

---

## Retain

**Keywords:**

* Keep on-premises
* Not ready to migrate
* Compliance requirements
* Regulatory constraints
* Deferred migration

**Examples:**

* Mainframe stays on-prem

✅ **Retain**

---

## Relocate

**Keywords:**

* VMware
* VMware Cloud on AWS
* Move entire environment
* No application redesign

**Examples:**

* VMware vSphere → VMware Cloud on AWS

✅ **Relocate**

---

# Fast Exam Mapping

| If you see...           | Answer     |
| ----------------------- | ---------- |
| No changes              | Rehost     |
| Managed service         | Replatform |
| Cloud-native / redesign | Refactor   |
| SaaS replacement        | Repurchase |
| Decommission            | Retire     |
| Keep on-prem            | Retain     |
| VMware Cloud on AWS     | Relocate   |

## Database-Specific Shortcuts

| Scenario                                 | Strategy   |
| ---------------------------------------- | ---------- |
| MySQL → EC2                              | Rehost     |
| MySQL → RDS MySQL                        | Replatform |
| Oracle → Aurora PostgreSQL with redesign | Refactor   |
| Legacy CRM → Salesforce                  | Repurchase |

## The Most Common Exam Traps

### Trap 1

> "Move MySQL to Amazon RDS"

Many people choose Rehost.

❌ Wrong

✅ **Replatform** (managed service)

---

### Trap 2

> "Move application without modification"

People overthink it.

✅ **Rehost**

---

### Trap 3

> "Replace application with Salesforce"

❌ Refactor

✅ **Repurchase**

---

### Trap 4

> "Break monolith into microservices"

❌ Replatform

✅ **Refactor**

For the AWS Cloud Practitioner and Solutions Architect Associate exams, **"no changes" = Rehost** and **"managed service" = Replatform** are probably the two most frequently tested distinctions.
