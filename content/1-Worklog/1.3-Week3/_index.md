---
title: "Week 3 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

- **Amazon RDS Architecture & Fundamentals:**
  - Understand Amazon Relational Database Service (Amazon RDS) features, supported DB engines (MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, Aurora), and OLTP use cases.
  - Master DB Subnet Groups (multi-AZ placement), storage types (General Purpose, Provisioned IOPS, Magnetic), and billing mechanisms.
- **High Availability, Disaster Recovery & Security:**
  - Differentiate synchronous Multi-AZ deployments (for High Availability/DR) from asynchronous Read Replicas (for read-scaling and offloading).
  - Learn DB snapshot management, point-in-time restores, encryption at rest via AWS KMS, and SSL connection security.
- **Hands-on Full-Stack Application Deployment:**
  - Execute prerequisite steps, create EC2 web server instances, and provision RDS database instances inside private DB Subnet Groups.
  - Deploy a web application connected to the RDS database, test automated/manual backups and restores, and execute full resource cleanup.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                                                                                                                            | Start Date | Completion Date | Reference Material                                                           |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ---------------------------------------------------------------------------- |
| Mon | - **Amazon RDS Fundamentals & Infrastructure:**<br> - Learn Amazon RDS architecture, managed service benefits, supported engines, and maintenance windows<br> - Configure DB Subnet Groups spanning multiple Availability Zones<br> - Compare storage types (gp2/gp3 vs Provisioned IOPS) and DB instance pricing models        | 2026-06-21 | 2026-06-21      | [Get Started with Amazon RDS](https://000005.awsstudygroup.com/1-introduce/) |
| Tue | - **Multi-AZ, Read Replicas & Security:**<br> - Study Multi-AZ synchronous replication and automatic failover mechanisms<br> - Explore Read Replica creation (cross-AZ, cross-region) for read-heavy workloads<br> - Configure RDS encryption at rest using KMS and SSL transport encryption                                    | 2026-06-22 | 2026-06-22      | [Get Started with Amazon RDS](https://000005.awsstudygroup.com/1-introduce/) |
| Wed | - **Infrastructure Setup & RDS Provisioning:**<br> - Complete prerequisite steps (VPC, private/public subnets, security groups)<br> - Launch an Amazon EC2 instance as a web application server<br> - Provision an Amazon RDS DB instance inside the private DB Subnet Group                                                    | 2026-06-23 | 2026-06-23      | [Get Started with Amazon RDS](https://000005.awsstudygroup.com/1-introduce/) |
| Thu | - **Application Deployment & Database Integration:**<br> - Deploy web application code on the EC2 instance<br> - Configure database endpoints, security group inbound rules, and establish application-to-RDS connection<br> - Verify database CRUD operations and monitor performance via CloudWatch & RDS Enhanced Monitoring | 2026-06-24 | 2026-06-24      | [Get Started with Amazon RDS](https://000005.awsstudygroup.com/1-introduce/) |
| Fri | - **Backup, Restore & Resource Cleanup:**<br> - Perform manual DB Snapshots and test database point-in-time restoration procedures<br> - Review migration tools (AWS DMS & Schema Conversion Tool) and database anti-patterns<br> - Delete RDS instances, snapshots, and terminate EC2 instances to complete resource cleanup   | 2026-06-25 | 2026-06-25      | [Get Started with Amazon RDS](https://000005.awsstudygroup.com/1-introduce/) |

### Week 3 Achievements:

- **Relational Database Management Mastery:**
  - Understood managed database concepts on AWS, DB instance sizing, maintenance windows, and DB Subnet Group configurations.
  - Gained clarity on appropriate use cases for RDS vs DynamoDB vs EC2 self-hosted databases vs Redshift.

- **High Availability & Security Architecture:**
  - Mastered Multi-AZ deployment strategies for automated failover and zero-data-loss synchronous replication.
  - Learned to scale read performance using asynchronous Read Replicas.
  - Implemented data-at-rest encryption using AWS KMS keys and configured database security groups.

- **Successful End-to-End Application Deployment:**
  - Provisioned a multi-tier infrastructure with an EC2 web server and an RDS database instance.
  - Successfully connected a web application to the RDS database via secure DB endpoints.

- **Backup Strategy & Resource Governance:**
  - Executed automated/manual DB Snapshots and verified point-in-time database restoration.
  - Completed all laboratory cleanup steps to prevent ongoing billing charges.
