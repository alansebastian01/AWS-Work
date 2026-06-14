Based on the ZIP file, here’s the AWS service list with quick real-time examples/tips:

| AWS Service                       | Real-time example / exam tip                                    |
| --------------------------------- | --------------------------------------------------------------- |
| **Amazon S3**                     | Store images, backups, logs. Tip: “object storage” = S3.        |
| **S3 Glacier**                    | Archive old records for years. Tip: cheapest long-term storage. |
| **EBS**                           | Hard drive for one EC2 server. Tip: block storage = EBS.        |
| **EFS**                           | Shared Linux file system for many EC2 instances.                |
| **FSx**                           | Managed Windows/specialized file server.                        |
| **Storage Gateway**               | Connect on-prem storage to AWS. Tip: hybrid storage.            |
| **AWS DataSync**                  | Move files from on-prem to AWS quickly.                         |
| **Snowball Edge**                 | Ship large TB/PB data to AWS physically.                        |
| **Snowmobile**                    | Massive 10+ PB data migration.                                  |
| **Amazon EC2**                    | Virtual server. Tip: full control over OS/server.               |
| **AWS Lambda**                    | Run code without servers. Tip: event-driven/serverless.         |
| **Elastic Beanstalk**             | Upload app code; AWS manages infra.                             |
| **AWS Fargate**                   | Run containers without managing servers.                        |
| **Auto Scaling**                  | Add/remove EC2 based on traffic.                                |
| **AppStream 2.0**                 | Stream apps to users’ computers.                                |
| **Amazon WorkSpaces**             | Cloud desktop for remote employees.                             |
| **Amazon RDS**                    | Managed SQL database. Tip: MySQL/PostgreSQL/Oracle = RDS.       |
| **Amazon Aurora**                 | High-performance MySQL/PostgreSQL-compatible DB.                |
| **DynamoDB**                      | Serverless NoSQL key-value DB.                                  |
| **Redshift**                      | Data warehouse for analytics.                                   |
| **Neptune**                       | Graph database for relationships.                               |
| **Route 53**                      | DNS/domain routing.                                             |
| **CloudFront**                    | CDN for faster global content delivery.                         |
| **Direct Connect**                | Dedicated private connection to AWS.                            |
| **Site-to-Site VPN**              | Encrypted connection from office to AWS.                        |
| **Transit Gateway**               | Connect many VPCs like a network hub.                           |
| **Global Accelerator**            | Improve global app performance and failover.                    |
| **IAM**                           | Users, groups, roles, permissions. Tip: “who can do what.”      |
| **STS(Security Token Sevice)**                           | Temporary security credentials.                                 |
| **GuardDuty**                     | Threat detection. Tip: suspicious activity = GuardDuty.         |
| **Inspector**                     | Vulnerability scanning for EC2/container workloads.             |
| **Macie**                         | Finds sensitive data/PII in S3.                                 |
| **Security Hub**                  | Central security findings dashboard.                            |
| **Shield**                        | DDoS protection.                                                |
| **AWS WAF(Web Application Firewall)** | Web firewall; block IPs, SQL injection, countries.              |
| **CloudTrail**                    | Audit API activity. Tip: “who did what?”                        |
| **AWS Artifact**                  | Compliance reports like SOC, ISO, PCI.                          |
| **CloudWatch**                    | Metrics, logs, alarms. Tip: monitoring = CloudWatch.            |
| **AWS Config**                    | Track resource configuration changes.                           |
| **Trusted Advisor**               | Best-practice recommendations.                                  |
| **EventBridge**                   | Event routing and automation.                                   |
| **Cost Explorer**                 | Analyze past AWS spending.                                      |
| **AWS Budgets**                   | Set cost alerts and budget thresholds.                          |
| **AWS Organizations**             | Manage multiple AWS accounts and consolidated billing.          |
| **Application Discovery Service** | Discover on-prem workloads before migration.                    |
| **Application Migration Service** | Lift-and-shift servers to AWS.                                  |
| **Migration Hub**                 | Track migration progress in one place.                          |
| **CloudFormation**                | Infrastructure as Code.                                         |
| **AWS CDK(Cloud Development Kit)**  | Define cloud infrastructure using code.                         |
| **AWS Pricing Calculator**        | Estimate cost before using AWS.                                 |
| **AWS Support / TAM(Technical Account Manager)**| Help with AWS issues; TAM comes with Enterprise Support.        |

**Best exam shortcut:**
Monitoring = **CloudWatch**
Audit = **CloudTrail**
Threats = **GuardDuty**
Vulnerabilities = **Inspector**
Sensitive S3 data = **Macie**
Cost alerts = **Budgets**
Cost analysis = **Cost Explorer**
Serverless code = **Lambda**
NoSQL = **DynamoDB**
DNS = **Route 53**
CDN = **CloudFront**
