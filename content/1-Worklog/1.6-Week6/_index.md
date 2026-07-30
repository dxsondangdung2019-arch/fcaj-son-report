---
title: "Week 6 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

- **Hybrid DNS Architecture with Route 53 Resolver:**
  - Understand hybrid DNS requirements connecting on-premises DNS infrastructure with Amazon Route 53.
  - Master Route 53 Resolver components: Inbound Endpoints (for on-prem queries to AWS), Outbound Endpoints (for AWS queries to on-prem), and Resolver Rules (forwarding specific domain queries).
  - Deploy prerequisites including Remote Desktop Gateway (RDGW), Active Directory (AD), and custom DNS configurations.
- **AWS CLI Hands-On Mastery (Part 1 - Core Services):**
  - Understand AWS CLI capabilities, cross-platform shell environments (Linux Bash/Zsh, Windows PowerShell/CMD, SSH/SSM), and direct AWS API access benefits.
  - Install and configure AWS CLI credentials safely following the principle of least privilege.
  - Perform operational commands and scripts for Amazon S3 and Amazon SNS resource management.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                                                                                                                                               | Start Date | Completion Date | Reference Material                                                                                                                                  |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Mon | - **Hybrid DNS Concepts & Environment Preparation:**<br> - Study Amazon Route 53, private DNS zones, and hybrid resolution mechanisms<br> - Learn Route 53 Resolver components: Inbound/Outbound Endpoints and Forwarding Rules<br> - Perform initial lab setup and launch Remote Desktop Gateway (RDGW)                                           | 2026-07-12 | 2026-07-12      | [Hybrid DNS with Route 53 Resolver](https://000010.awsstudygroup.com/vi/1-introduce/)                                                               |
| Tue | - **Microsoft Active Directory & Hybrid DNS Deployment:**<br> - Deploy Microsoft Active Directory on EC2 to simulate on-premises DNS infrastructure<br> - Configure Route 53 Inbound & Outbound Endpoints<br> - Establish forwarding rules and test bidirectional DNS resolution between AWS and AD DNS                                            | 2026-07-13 | 2026-07-13      | [Hybrid DNS with Route 53 Resolver](https://000010.awsstudygroup.com/vi/1-introduce/)                                                               |
| Wed | - **AWS CLI Fundamentals & Environment Setup:**<br> - Learn AWS CLI features, high-level vs low-level commands, and multi-environment shell support<br> - Install AWS CLI v2 and configure Access Keys, Secret Keys, default region, and output formats<br> - Execute resource discovery and account verification commands via CLI                 | 2026-07-14 | 2026-07-14      | [Getting Started with AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/)                                                                    |
| Thu | - **AWS CLI Practical Operations (Amazon S3 & Amazon SNS):**<br> - Perform S3 bucket management via CLI (create buckets, upload/download objects, list contents, set policies)<br> - Manage Amazon Simple Notification Service (SNS) topics and subscriptions via CLI<br> - Test notification publishing and payload verification via CLI commands | 2026-07-15 | 2026-07-15      | [Getting Started with AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/)                                                                    |
| Fri | - **Hybrid DNS Testing & Clean up:**<br> - Verify seamless domain resolution across hybrid environments<br> - Delete Route 53 Resolver Endpoints, Rules, Microsoft AD, and RDGW instances to complete hybrid DNS cleanup<br> - Retain AWS CLI configurations for upcoming advanced labs                                                            | 2026-07-16 | 2026-07-16      | [Hybrid DNS with Route 53 Resolver](https://000010.awsstudygroup.com/vi/1-introduce/) & [AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/) |

### Week 6 Achievements:

- **Hybrid Network & DNS Architecture Proficiency:**
  - Mastered hybrid DNS integration using Route 53 Inbound and Outbound Endpoints alongside custom Resolver Rules.
  - Successfully connected simulated on-premises Active Directory DNS with AWS Route 53 private hosted zones.

- **AWS CLI Core Capabilities (Part 1):**
  - Configured AWS CLI across local shell environments with credential security best practices.
  - Gained hands-on competency in querying, managing, and automating Amazon S3 buckets/objects and Amazon SNS topics via command-line interface.

- **System Hygiene & Cost Governance:**
  - Executed complete cleanup for all Route 53 Resolver endpoints and AD instances to prevent ongoing charges.
