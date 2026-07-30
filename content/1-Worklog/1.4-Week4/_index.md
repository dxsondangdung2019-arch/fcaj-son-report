---
title: "Week 4 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

- **Auto Scaling Group & Load Balancing Architecture:**
  - Understand the role of Amazon EC2 Auto Scaling Group (ASG) for dynamic capacity adjustment and high availability across multiple Availability Zones.
  - Master Launch Templates for standardized EC2 provisioning and Elastic Load Balancers (ALB, NLB, GWLB) with Target Groups for traffic distribution.
  - Differentiate scaling policies: Manual, Dynamic (Target Tracking, Step, Simple), Scheduled, and Predictive Scaling using Machine Learning.
- **AWS Cost Governance with AWS Budgets:**
  - Master financial management on AWS using AWS Budgets to prevent cost overruns and set up proactive threshold alerts.
  - Understand the 4 core Budget types: Cost Budget, Usage Budget, Reserved Instance (RI) Budget, and Savings Plans Budget.
- **Hands-on Deployment & Testing:**
  - Deploy the FCJ Management Application with Launch Templates, Target Groups, and Application Load Balancer.
  - Configure Auto Scaling Groups and conduct stress testing to verify automatic scaling policies and health check mechanisms.
  - Set up AWS Cost & Usage Budgets with alert notifications and complete lab resource cleanup.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                                                                                                                                                                                                       | Start Date | Completion Date | Reference Material                                                                                                                              |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Mon | - **Auto Scaling & Load Balancing Fundamentals:**<br> - Study Auto Scaling Group (ASG) core concepts, high availability benefits, and Launch Templates<br> - Learn Elastic Load Balancer types (ALB Layer 7, NLB Layer 4, GWLB) and Target Group health check configurations<br> - Compare scaling strategies: Manual, Dynamic (Target Tracking/Step/Simple), Scheduled, and ML-powered Predictive Scaling | 2026-06-28 | 2026-06-28      | [FCJ Management Deployment with ASG](https://000006.awsstudygroup.com/vi/1-introduction/)                                                       |
| Tue | - **Application Infrastructure Setup:**<br> - Complete prerequisite steps using pre-configured FCJ Management instances<br> - Create a Launch Template specifying AMI, instance type, key pair, and security groups<br> - Provision an Application Load Balancer (ALB) and configure Target Group health checks                                                                                            | 2026-06-29 | 2026-06-29      | [FCJ Management Deployment with ASG](https://000006.awsstudygroup.com/vi/1-introduction/)                                                       |
| Wed | - **Auto Scaling Configuration & Stress Testing:**<br> - Create an Auto Scaling Group associated with the ALB Target Group across multiple AZs<br> - Configure dynamic scaling policies (Target Tracking based on CPU/traffic)<br> - Perform stress tests to verify scale-out/scale-in behaviors, health checks, and load balancing distribution                                                           | 2026-06-30 | 2026-06-30      | [FCJ Management Deployment with ASG](https://000006.awsstudygroup.com/vi/1-introduction/)                                                       |
| Thu | - **AWS Budgets & Cost Management Setup:**<br> - Study AWS Budgets benefits for financial planning and cost optimization<br> - Create a Cost Budget with 80% and 100% threshold alert notifications<br> - Create a Usage Budget (e.g., EC2 running hours) and explore RI & Savings Plans Budgets                                                                                                           | 2026-07-01 | 2026-07-01      | [Cost Management with AWS Budgets](https://000007.awsstudygroup.com/vi/)                                                                        |
| Fri | - **Testing & Lab Cleanup:**<br> - Verify AWS Budget alert triggers and email notification delivery<br> - Deregister targets, delete Auto Scaling Groups, Load Balancers, Launch Templates, and AWS Budgets<br> - Complete full lab resource cleanup to avoid unnecessary charges                                                                                                                          | 2026-07-02 | 2026-07-02      | [FCJ Management Deployment with ASG](https://000006.awsstudygroup.com/vi/1-introduction/) & [AWS Budgets](https://000007.awsstudygroup.com/vi/) |

### Week 4 Achievements:

- **Scalable & Highly Available Architecture Mastery:**
  - Deepened understanding of Elastic Load Balancers (ALB/NLB/GWLB) and Target Group health check configurations.
  - Mastered Launch Templates for maintaining consistent EC2 configurations and version management.
  - Understood how to combine Predictive Scaling (for known traffic patterns) with Dynamic Scaling (for sudden spikes).

- **End-to-End Application Deployment & Testing:**
  - Successfully deployed the FCJ Management Application behind an Application Load Balancer and Auto Scaling Group.
  - Tested and validated automatic scale-out and scale-in triggers under simulated load conditions.

- **AWS Cost Governance & Financial Control:**
  - Understood the 4 types of AWS Budgets: Cost Budget, Usage Budget, RI Budget, and Savings Plans Budget.
  - Configured proactive threshold alerts (80% and 100%) to prevent unpredicted AWS expenses.

- **Resource Governance & Cleanup Execution:**
  - Successfully executed systematic resource cleanup (terminating ASGs, ALBs, Launch Templates, and Budgets) to maintain account cost safety.
