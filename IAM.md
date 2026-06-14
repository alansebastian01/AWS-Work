Here are the **high-yield IAM questions from your CLF-C02 zip** and the fastest ways to eliminate the wrong choices.

---

# Q4 — EC2 Accessing S3

> According to security best practices, how should an EC2 instance be given access to an S3 bucket?

A. Hardcode access keys
B. Store access keys in a file
C. Have the EC2 instance assume a role ✅
D. Open bucket access to all services

### Why C?

Use an **IAM Role for EC2**. AWS automatically provides temporary credentials.

### Elimination Tip

| If you see...                  | Eliminate |
| ------------------------------ | --------- |
| Hardcoded credentials          | Wrong     |
| Credentials in files           | Wrong     |
| Temporary credentials via role | Correct   |

**Exam trigger:** *EC2 needs AWS access* → **IAM Role**

---

# Q26 — Password & Access Key Audit

> Audit password and access key rotation details.

A. IAM Access Analyzer
B. AWS Artifact
C. IAM Credential Report ✅
D. AWS Audit Manager

### Why C?

Credential Reports show:

* Password age
* Access key age
* MFA status
* Last password change

### Elimination Tip

| Service           | Purpose                        |
| ----------------- | ------------------------------ |
| Access Analyzer   | External access detection      |
| Artifact          | Compliance documents           |
| Credential Report | IAM credential audit           |
| Audit Manager     | Compliance evidence collection |

**Exam trigger:** *password rotation*, *access key age* → **Credential Report**

---

# Q32 — CLI/API Access

> User needs programmatic access through CLI/API.

A. Amazon Inspector
B. Access Keys ✅
C. SSH Public Keys
D. KMS Keys

### Why B?

CLI and SDK authentication uses:

* Access Key ID
* Secret Access Key

### Elimination Tip

| Option      | Used For          |
| ----------- | ----------------- |
| Access Keys | CLI/API           |
| SSH Keys    | EC2 login         |
| KMS Keys    | Encryption        |
| Inspector   | Security scanning |

**Exam trigger:** *programmatic access* → **Access Keys**

---

# Q36 — External Access Detection

> Identify whether an S3 bucket or IAM role has been shared externally.

A. Service Catalog
B. Systems Manager
C. IAM Access Analyzer ✅
D. Organizations

### Why C?

Access Analyzer identifies:

* Public access
* Cross-account access
* External sharing

### Memory Trick

**Access Analyzer = "Who can access this?"**

---

# Q39 — IAM Security Best Practice

> Which recommendation follows IAM best practices?

A. Use root user access keys
B. Grant broad permissions
C. Enable MFA ✅
D. Avoid credential rotation

### Why C?

AWS best practice:

* Enable MFA
* Use least privilege
* Avoid root usage

### Elimination Tip

Anything that says:

❌ Use root daily
❌ Broad permissions
❌ No credential rotation

is usually wrong.

---

# Q474 — Multiple AWS Account Logins

> Manage multiple logins across AWS accounts in AWS Organizations.

A. VPC
B. GuardDuty
C. Cognito
D. IAM Identity Center ✅

### Why D?

IAM Identity Center provides:

* SSO
* Centralized access
* Multi-account login

### Exam Trigger

"Multiple AWS accounts" + "single sign-on"

→ **IAM Identity Center**

---

# Q482 — IAM Best Practices (Choose Two)

A. Use root daily
B. Use access keys on EC2
C. Rotate credentials regularly ✅
D. Shared admin access keys
E. Enable MFA ✅

### Correct

✅ C
✅ E

### Elimination Tips

| Wrong Choice       | Why           |
| ------------------ | ------------- |
| Root daily         | Never         |
| Access keys on EC2 | Use IAM roles |
| Shared credentials | Never share   |

### Memory Rule

AWS loves:

✅ MFA
✅ Credential rotation
✅ Least privilege

---

# Common IAM Exam Traps

## Root User

If a question asks:

> "Who should perform daily administration?"

Never choose **Root User**.

Use IAM users, roles, or Identity Center.

---

## Access Keys vs Roles

### CLI / SDK User

➡️ Access Keys

### EC2 Accessing AWS Services

➡️ IAM Role

---

## IAM Access Analyzer

If you see:

* External access
* Public access
* Cross-account access

➡️ IAM Access Analyzer

---

## IAM Credential Report

If you see:

* Password age
* Access key age
* MFA enabled?
* Credential audit

➡️ IAM Credential Report

---

## IAM Identity Center

If you see:

* Multiple AWS accounts
* Single sign-on (SSO)
* Centralized access management

➡️ IAM Identity Center

---

# CLF-C02 IAM Cheat Sheet

| Keyword                   | Answer                    |
| ------------------------- | ------------------------- |
| EC2 needs S3 access       | IAM Role                  |
| CLI/API access            | Access Keys               |
| Password/access key audit | Credential Report         |
| Public or external access | IAM Access Analyzer       |
| Multiple account login    | IAM Identity Center       |
| Added login security      | MFA                       |
| Daily administration      | IAM user/role, not root   |
| EC2 credentials           | IAM Role, not access keys |

These IAM questions appear repeatedly on CLF-C02 in slightly different wording, so memorizing the **keyword → service** mapping above gives a big payoff.
