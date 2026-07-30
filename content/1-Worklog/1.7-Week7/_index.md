---
title: "Week 7 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

- **Advanced Infrastructure Management via AWS CLI (Part 2):**
  - Master identity & infrastructure provisioning via AWS CLI including IAM role/user management, VPC configuration, and EC2 instance deployment.
  - Gain hands-on troubleshooting skills for common CLI errors and perform complete CLI resource cleanup.
- **Centralized Identity Management with AWS IAM Identity Center:**
  - Understand centralized access management using AWS IAM Identity Center (formerly AWS Single Sign-On) following Zero Trust principles and least privilege.
  - Configure multi-account access, user group assignments, Customer Managed Policies, and time-based access control.
  - Interact with IAM Identity Center Identity Store APIs via CLI and perform systematic resource cleanup.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                                                                                                                                                | Start Date | Completion Date | Reference Material                                                                                                                    |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Mon | - **AWS CLI Core Infrastructure Operations (IAM & VPC):**<br> - Manage IAM entities via CLI: create users, groups, roles, and attach access policies<br> - Provision network infrastructure via CLI: create VPC, subnets, route tables, and Internet Gateways<br> - Configure security groups and inbound/outbound traffic rules using CLI commands | 2026-07-19 | 2026-07-19      | [Getting Started with AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/)                                                      |
| Tue | - **EC2 Launch via CLI & Troubleshooting:**<br> - Launch and configure EC2 instances entirely using AWS CLI commands<br> - Practice CLI troubleshooting techniques (credential issues, permission errors, syntax debugging)<br> - Perform resource cleanup for CLI test resources                                                                   | 2026-07-20 | 2026-07-20      | [Getting Started with AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/)                                                      |
| Wed | - **AWS IAM Identity Center Setup & Access Control:**<br> - Complete preparation steps and enable AWS IAM Identity Center<br> - Configure user directories, groups, and permission sets based on project roles<br> - Implement time-based access control to enforce temporary elevated permissions                                                  | 2026-07-21 | 2026-07-21      | [IAM Identity Center Workshop](https://000012.awsstudygroup.com/vi/1-introduce/)                                                      |
| Thu | - **Customer Managed Policies & Identity Store APIs:**<br> - Design and attach Customer Managed Policies for fine-grained authorization<br> - Programmatically manage users and groups using IAM Identity Center Identity Store APIs<br> - Practice CLI integration for identity management tasks                                                   | 2026-07-22 | 2026-07-22      | [IAM Identity Center Workshop](https://000012.awsstudygroup.com/vi/1-introduce/)                                                      |
| Fri | - **Cross-Account Access Verification & Resource Cleanup:**<br> - Test Single Sign-On (SSO) login experience across assigned AWS accounts and roles<br> - Verify permission boundaries and time-based access constraints<br> - Remove created permission sets, users, groups, and test policies to complete lab cleanup                             | 2026-07-23 | 2026-07-23      | [AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/) & [IAM Identity Center](https://000012.awsstudygroup.com/vi/1-introduce/) |

### Week 7 Achievements:

- **Advanced AWS CLI Proficiency:**
  - Acquired full operational capabilities to manage IAM roles, network infrastructure (VPC/Subnets), and EC2 compute resources via command line.
  - Developed effective troubleshooting skills for diagnosing CLI authentication and permission errors.

- **Enterprise Identity & Access Governance:**
  - Successfully deployed AWS IAM Identity Center for multi-account centralized access control following Zero Trust and least privilege principles.
  - Implemented Customer Managed Policies, time-based access controls, and programmatically interacted with Identity Store APIs.

- **Clean Architecture & Compliance:**
  - Verified cross-account access and executed comprehensive cleanup of all test IAM and CLI resources.
