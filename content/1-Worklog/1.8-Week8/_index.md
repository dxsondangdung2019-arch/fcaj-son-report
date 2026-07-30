---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

- **Application Deployment using Docker & Docker Compose on AWS:**
  - Understand application containerization fundamentals, local testing, and multi-container deployment on Amazon EC2.
  - Configure Amazon RDS instances as backend databases and integrate them with containerized web applications.
  - Build custom Docker images, write `docker-compose.yml` configurations, and manage Docker image registries/pushing.
- **Microservices Deployment on Amazon Elastic Container Service (ECS):**
  - Master Amazon ECS concepts for running and stop-managing Docker containers across a cluster.
  - Register service namespaces using AWS Cloud Map for service discovery.
  - Define ECS Task Definitions, launch ECS Clusters, configure Application Load Balancers (ALB), and create scalable ECS Services.
  - Validate application health via ALB endpoints and perform resource cleanup.

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                                                                                                                                               | Start Date | Completion Date | Reference Material                                                                                                                       |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Mon | - **Docker Fundamentals & RDS Integration:**<br> - Test local container deployment and prepare deployment scripts<br> - Launch and configure Amazon RDS database instance<br> - Provision and configure Amazon EC2 instance with Docker environment                                                                                                | 2026-07-26 | 2026-07-26      | [Deploy Application on Docker](https://000015.awsstudygroup.com/vi/1-introduce/)                                                         |
| Tue | - **Docker & Docker Compose Deployment on EC2:**<br> - Deploy web applications using standalone Docker images<br> - Orchestrate multi-container applications using Docker Compose<br> - Push built container images to container registry and clean up EC2 local resources                                                                         | 2026-07-27 | 2026-07-27      | [Deploy Application on Docker](https://000015.awsstudygroup.com/vi/1-introduce/)                                                         |
| Wed | - **Amazon ECS Architecture & Cluster Setup:**<br> - Study Amazon ECS architecture, cluster concepts, and service discovery mechanisms<br> - Complete prerequisite configurations and register namespaces in AWS Cloud Map<br> - Create an Amazon ECS Cluster for container hosting                                                                | 2026-07-28 | 2026-07-28      | [Deploy Applications on Amazon ECS](https://000016.awsstudygroup.com/vi/1-introduce/)                                                    |
| Thu | - **ECS Task Definitions, ALB & Service Deployment:**<br> - Create ECS Task Definitions specifying container images, CPU/Memory limits, and port mappings<br> - Configure Application Load Balancer (ALB) with Target Groups and listener rules<br> - Create and launch ECS Service connected to the ALB for automated scaling and traffic routing | 2026-07-29 | 2026-07-29      | [Deploy Applications on Amazon ECS](https://000016.awsstudygroup.com/vi/1-introduce/)                                                    |
| Fri | - **Verification, Testing & Complete Resource Cleanup:**<br> - Test deployment results by accessing application endpoints via ALB DNS<br> - Verify container health checks, auto-recovery, and ECS task status<br> - Clean up ECS Services, Clusters, ALBs, Cloud Map namespaces, EC2, and RDS instances                                           | 2026-07-30 | 2026-07-30      | [Deploy on Docker](https://000015.awsstudygroup.com/vi/1-introduce/) & [Deploy on ECS](https://000016.awsstudygroup.com/vi/1-introduce/) |

### Week 8 Achievements:

- **Docker Containerization Mastery:**
  - Successfully containerized applications locally and deployed them to AWS EC2 using both standalone Docker images and Docker Compose orchestrations.
  - Integrated containerized front-end/backend applications with Amazon RDS managed databases.

- **Enterprise Container Orchestration with Amazon ECS:**
  - Provisioned high-availability ECS Clusters, managed task definitions, and implemented service discovery via AWS Cloud Map.
  - Configured Application Load Balancers (ALB) to distribute web traffic smoothly across running ECS Tasks and Services.

- **Cloud Governance & Cost Cleanup:**
  - Conducted end-to-end verification of deployed microservices and systematically removed all ECS, ALB, RDS, and EC2 resources to prevent unnecessary cloud costs.
