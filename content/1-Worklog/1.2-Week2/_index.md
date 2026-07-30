---
title: "Week 2 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

- **Deep Dive into Amazon VPC & Network Architecture:**
  - Further master custom Amazon VPC architecture, advanced Subnet isolation, Route Tables, Internet Gateways, and NAT Gateways.
  - Understand VPC Security mechanisms (Security Groups & Network ACLs) and advanced Site-to-Site VPN connectivity.
- **Amazon EC2 Fundamentals & Operating Systems:**
  - Master Amazon EC2 core components: Instance Types (Compute, Memory, Storage, Network optimized), AMIs, EBS vs Instance Store volumes.
  - Learn EC2 security mechanisms: Key Pairs, Security Groups, IAM Roles, and SSM Session Manager.
- **Hands-on Application Deployment & Governance:**
  - Launch and configure Microsoft Windows Server 2025 and Amazon Linux 2023 instances.
  - Deploy a Node.js Application on EC2 Windows and an AWS User Management Application on Amazon Linux.
  - Practice Cost & Usage Governance with IAM and resource cleanup.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                                                                                                            | Start Date | Completion Date | Reference Material                                                          |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | --------------------------------------------------------------------------- |
| Mon | - **Advanced Amazon VPC Deep Dive:**<br> - Review and deepen knowledge of custom VPC designs, IPv4/IPv6 CIDR ranges, and Subnets<br> - Study complex routing configurations with Route Tables, Internet Gateways, and NAT Gateways<br> - Explore VPC Firewall rules and Site-to-Site VPN architectural patterns | 2026-06-14 | 2026-06-14      | [Amazon VPC & VPN Deep Dive](https://000003.awsstudygroup.com/1-introduce/) |
| Tue | - **Amazon EC2 Architecture & Storage Options:**<br> - Study EC2 Instance Families (General Purpose, Compute, Memory Optimized)<br> - Compare Amazon AMIs (AWS-provided, Marketplace, Custom AMIs)<br> - Analyze EBS Volumes (persistent) vs Instance Store Volumes (ephemeral storage warnings)                | 2026-06-15 | 2026-06-15      | [Introduction to Amazon EC2](https://000004.awsstudygroup.com/1-introduce/) |
| Wed | - **EC2 Security & Server Provisioning:**<br> - Configure Key Pairs, Elastic IPs, Security Groups, and SSM Session Manager<br> - Launch a Microsoft Windows Server 2025 Instance<br> - Launch an Amazon Linux 2023 Instance inside custom VPC Subnets                                                           | 2026-06-16 | 2026-06-16      | [Introduction to Amazon EC2](https://000004.awsstudygroup.com/1-introduce/) |
| Thu | - **Hands-on Application Deployments:**<br> - Deploy an AWS User Management Application on Amazon Linux 2023<br> - Deploy a Node.js Application on EC2 Windows Server<br> - Verify application connectivity and elastic network access                                                                          | 2026-06-17 | 2026-06-17      | [Introduction to Amazon EC2](https://000004.awsstudygroup.com/1-introduce/) |
| Fri | - **Governance, Cost Control & Cleanup:**<br> - Implement Cost & Usage Governance policies using IAM and Tags<br> - Disassociate/release unused Elastic IPs and terminate unneeded instances<br> - Practice full resource cleanup procedures                                                                    | 2026-06-18 | 2026-06-18      | [Introduction to Amazon EC2](https://000004.awsstudygroup.com/1-introduce/) |

### Week 2 Achievements:

- **Advanced Networking Proficiency (Amazon VPC):**
  - Mastered subnets, routing logic through Route Tables, Internet Gateways, and NAT Gateways for secure public/private isolation.
  - Understood VPC network security design and Site-to-Site VPN concepts for hybrid connectivity.

- **Comprehensive EC2 Lifecycle Knowledge:**
  - Learned how to choose appropriate EC2 Instance Types based on compute, memory, and network requirements.
  - Differed persistent EBS volumes from temporary Instance Store volumes to avoid data loss.
  - Mastered EC2 access controls using Key Pairs, IAM Roles, and secure Systems Manager Session Manager.

- **Multi-OS Application Deployment:**
  - Successfully provisioned Microsoft Windows Server 2025 and Amazon Linux 2023 instances.
  - Deployed and configured a Node.js web application on Windows Server.
  - Deployed an AWS User Management Application on Amazon Linux 2023.

- **Cost & Resource Governance Execution:**
  - Configured IAM Cost & Usage Governance rules using tag-based resource tracking.
  - Successfully executed clean-up procedures to prevent unexpected charges (released idle Elastic IPs, terminated temporary instances).
