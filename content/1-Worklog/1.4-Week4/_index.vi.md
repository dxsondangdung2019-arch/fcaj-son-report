---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

- **Kiến trúc Auto Scaling Group & Cân bằng tải:**
  - Hiểu rõ vai trò của Amazon EC2 Auto Scaling Group (ASG) trong việc tự động điều chỉnh số lượng instance và duy trì tính sẵn sàng cao trên nhiều AZ.
  - Thành thạo tạo Launch Template để chuẩn hóa cấu hình khởi chạy EC2 và Elastic Load Balancer (ALB, NLB, GWLB) kết hợp Target Group.
  - Phân biệt các loại Scaling: Manual, Dynamic (Target Tracking, Step, Simple), Scheduled, và Predictive Scaling sử dụng machine learning.
- **Quản trị chi phí với AWS Budgets:**
  - Nắm vững giải pháp quản lý tài chính trên AWS bằng dịch vụ AWS Budgets để chủ động kiểm soát chi phí và đặt ngưỡng cảnh báo.
  - Phân biệt 4 loại Budget cốt lõi: Cost Budget, Usage Budget, RI Budget và Savings Plans Budget.
- **Thực hành triển khai & Kiểm thử hệ thống:**
  - Triển khai ứng dụng FCJ Management tích hợp Launch Template, Target Group và Application Load Balancer.
  - Cấu hình Auto Scaling Group và giả lập tải để kiểm thử khả năng tự động mở rộng/thu nhỏ và kiểm tra sức khỏe Target Group.
  - Thiết lập hệ thống cảnh báo ngân sách AWS Budgets và dọn dẹp toàn bộ tài nguyên.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                 |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - **Nền tảng Auto Scaling & Load Balancing:**<br> - Tìm hiểu tổng quan Auto Scaling Group (ASG), lợi ích sẵn sàng cao và cấu hình Launch Template<br> - Nghiên cứu các loại Elastic Load Balancer (ALB Layer 7, NLB Layer 4, GWLB) và cấu hình Health Check trong Target Group<br> - So sánh các chiến lược scaling: Manual, Dynamic Scaling (Target Tracking/Step/Simple), Scheduled và Predictive Scaling | 2026-06-28   | 2026-06-28      | [Triển khai FCJ Management với ASG](https://000006.awsstudygroup.com/vi/1-introduction/)                                                       |
| 3   | - **Thiết lập hạ tầng ứng dụng:**<br> - Thực hiện các bước chuẩn bị từ máy ảo FCJ Management đã triển khai<br> - Tạo Launch Template chứa đầy đủ thông số AMI, instance type, key pair, network settings và security groups<br> - Cấu hình Application Load Balancer (ALB) và thiết lập Target Group kèm theo health check                                                                                  | 2026-06-29   | 2026-06-29      | [Triển khai FCJ Management với ASG](https://000006.awsstudygroup.com/vi/1-introduction/)                                                       |
| 4   | - **Cấu hình Auto Scaling Group & Kiểm thử:**<br> - Tạo Auto Scaling Group liên kết với ALB Target Group phân bổ trên nhiều Availability Zones<br> - Thiết lập chính sách Dynamic Scaling (Target Tracking theo CPU utilization/traffic)<br> - Tiến hành kiểm thử tải (stress test) để đánh giá khả năng Scale Out / Scale In và phân phối lưu lượng của Load Balancer                                      | 2026-06-30   | 2026-06-30      | [Triển khai FCJ Management với ASG](https://000006.awsstudygroup.com/vi/1-introduction/)                                                       |
| 5   | - **Thiết lập Quản lý chi phí với AWS Budgets:**<br> - Tìm hiểu lợi ích của AWS Budgets trong kiểm soát chi phí và lập kế hoạch tài chính<br> - Khởi tạo Cost Budget với các ngưỡng cảnh báo 80% và 100% ngân sách<br> - Khởi tạo Usage Budget (ví dụ: số giờ chạy EC2) và nghiên cứu các mô hình RI Budget, Savings Plans Budget                                                                           | 2026-07-01   | 2026-07-01      | [Quản lý chi phí với AWS Budgets](https://000007.awsstudygroup.com/vi/)                                                                        |
| 6   | - **Kiểm thử cảnh báo & Dọn dẹp tài nguyên:**<br> - Kiểm tra quy trình gửi thông báo cảnh báo qua email của AWS Budgets<br> - Tiến hành xóa Auto Scaling Group, Application Load Balancer, Target Group, Launch Template và các Budgets đã tạo<br> - Hoàn tất dọn dẹp tài nguyên bài lab để tránh phát sinh chi phí duy trì                                                                                 | 2026-07-02   | 2026-07-02      | [Triển khai FCJ Management với ASG](https://000006.awsstudygroup.com/vi/1-introduction/) & [AWS Budgets](https://000007.awsstudygroup.com/vi/) |

### Kết quả đạt được tuần 4:

- **Thành thạo kiến trúc Mở rộng linh hoạt & Cao khả dụng:**
  - Nắm vững cơ chế phân phối lưu lượng của Elastic Load Balancer và cấu hình health check chính xác cho Target Group.
  - Làm chủ việc sử dụng Launch Template để quản lý phiên bản cấu hình khởi chạy EC2 an toàn.
  - Hiểu cách phối hợp giữa Predictive Scaling (dự báo theo dữ liệu lịch sử) và Dynamic Scaling (xử lý biến động thực tế).

- **Triển khai & Kiểm thử ứng dụng thực tế thành công:**
  - Triển khai thành công ứng dụng FCJ Management phía sau Application Load Balancer và Auto Scaling Group.
  - Xác nhận hệ thống tự động tăng/giảm số lượng máy chủ chính xác theo mức độ sử dụng tài nguyên thực tế.

- **Quản trị tài chính & Chi phí AWS chuyên nghiệp:**
  - Hiểu rõ công dụng của 4 loại ngân sách: Cost Budget, Usage Budget, RI Budget và Savings Plans Budget.
  - Cấu hình thành công các ngưỡng cảnh báo chi phí (80% và 100%), hỗ trợ ngăn ngừa việc vượt quá ngân sách dự kiến.

- **Tối ưu & Dọn dẹp tài nguyên Bài lab:**
  - Thực hiện đúng quy trình Clean up tài nguyên hệ thống (xóa ASG, ALB, Launch Template, Budgets) đảm bảo an toàn chi phí tài khoản.
