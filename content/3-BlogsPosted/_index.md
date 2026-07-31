---
title: "Blogs Posted"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

This section lists and introduces the blogs posted to [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj).

### [Blog 1 - Session Policies in Amazon EKS Pod Identity](3.1-Blog1/)

This blog introduces the newly added session policies feature in Amazon EKS Pod Identity, which allows you to narrow IAM permissions flexibly and precisely for each pod without needing to create multiple separate IAM roles. The article covers key concepts including how session policies work (effective permissions = intersection between role permissions and session policy), benefits such as reducing IAM role proliferation and avoiding quota limits, and practical debugging techniques for AccessDenied errors using the four-question framework (principal, action, resource, context). It also explains the relationship between different IAM policy layers including identity-based policies, resource-based policies, permissions boundaries, SCPs, and session policies.

### [Blog 2 - From Zero to Zero-Downtime: DevOps & CI/CD on AWS](3.2-Blog2/)

This blog shares practical lessons learned from implementing DevOps and CI/CD on AWS. It covers three key lessons: Infrastructure as Code (using Terraform or AWS CDK instead of manual console clicks), Shift-Left Security (integrating security scans early in the pipeline with Checkov, TFLint, and Amazon ECR Image Scanning), and Blue/Green & Canary Deployments (achieving zero-downtime through AWS CodeDeploy strategies). The article also details a complete pipeline architecture: GitHub → AWS CodePipeline → AWS CodeBuild (Unit Tests & Security Scan) → Amazon ECR → AWS CodeDeploy/Helm → Amazon EKS. Results include deployment time reduction from 30 minutes to under 4 minutes with automated rollback capabilities.

### [Blog 3 - ...](3.3-Blog3/)

_Coming soon_
