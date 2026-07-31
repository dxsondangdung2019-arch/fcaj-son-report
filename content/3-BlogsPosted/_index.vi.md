---
title: "Các bài blogs đã đăng"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Tại đây sẽ là phần liệt kê, giới thiệu các blogs đã đăng trên [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj).

### [Blog 1 - Session Policies trong Amazon EKS Pod Identity](3.1-Blog1/)

Blog này giới thiệu tính năng session policies mới được bổ sung trong Amazon EKS Pod Identity, cho phép thu hẹp quyền IAM linh hoạt và chính xác cho từng pod mà không cần tạo nhiều IAM roles riêng biệt. Bài viết bao gồm các khái niệm chính như cách session policy hoạt động (quyền hiệu lực = giao điểm giữa role permissions và session policy), lợi ích như giảm số lượng IAM roles và tránh chạm quota, cùng kỹ thuật debug lỗi AccessDenied thực tế với khung bốn câu hỏi (principal, action, resource, context). Bài viết cũng giải thích mối quan hệ giữa các tầng IAM policy khác nhau.

### [Blog 2 - Từ Zero Đến Zero-Downtime: DevOps & CI/CD Trên AWS](3.2-Blog2/)

Blog này chia sẻ những bài học thực tế từ quá trình triển khai DevOps và CI/CD trên AWS. Bài viết đề cập ba bài học quan trọng: Infrastructure as Code (dùng Terraform hoặc AWS CDK thay vì bấm tay trên console), Shift-Left Security (tích hợp bảo mật sớm với Checkov, TFLint và Amazon ECR Image Scanning), và Blue/Green & Canary Deployments (đạt zero-downtime qua CodeDeploy). Bài viết còn mô tả chi tiết kiến trúc pipeline: GitHub → AWS CodePipeline → AWS CodeBuild (Unit Tests & Security Scan) → Amazon ECR → AWS CodeDeploy/Helm → Amazon EKS. Kết quả đạt được bao gồm thời gian deploy giảm từ 30 phút xuống dưới 4 phút với khả năng tự động rollback.

### [Blog 3 - ...](3.3-Blog3/)

_Sắp ra mắt_
