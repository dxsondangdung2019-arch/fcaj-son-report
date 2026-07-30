---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

### Mục tiêu tuần 8:

- **Triển khai ứng dụng với Docker & Docker Compose trên AWS:**
  - Hiểu cách đóng gói ứng dụng bằng Docker, chạy thử nghiệm local và triển khai lên máy chủ Amazon EC2.
  - Cấu hình Cơ sở dữ liệu Amazon RDS và kết nối với ứng dụng containerized.
  - Xây dựng Docker Image, thiết lập `docker-compose.yml` điều phối đa container và đẩy image lên registry.
- **Triển khai ứng dụng trên Amazon Elastic Container Service (ECS):**
  - Nắm vững khái niệm Amazon ECS trong việc quản lý, chạy và điều phối các Docker container trên hạ tầng đám mây.
  - Đăng ký Namespace trên AWS Cloud Map phục vụ cơ chế định tuyến và khám phá dịch vụ (Service Discovery).
  - Khởi tạo ECS Cluster, định nghĩa ECS Task Definition, cấu hình Application Load Balancer (ALB) và triển khai ECS Service.
  - Kiểm thử kết quả vận hành qua ALB và tiến hành dọn dẹp tài nguyên sau bài lab.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                            | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                           |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - **Nền tảng Docker & Khởi tạo RDS/EC2:**<br> - Kiểm thử chạy ứng dụng Docker ở môi trường Local và chuẩn bị kịch bản triển khai<br> - Khởi tạo và cấu hình cơ sở dữ liệu Amazon RDS Instance<br> - Cấu hình máy chủ Amazon EC2, cài đặt môi trường Docker sẵn sàng triển khai                                                                       | 2026-07-26   | 2026-07-26      | [Deploy Application on Docker](https://000015.awsstudygroup.com/vi/1-introduce/)                                                         |
| 3   | - **Thực hành Triển khai Docker & Docker Compose:**<br> - Triển khai ứng dụng web lên EC2 bằng phương pháp Docker Image đơn lẻ<br> - Tự động hóa và điều phối hệ thống đa container bằng Docker Compose<br> - Thực hành đẩy (Push) Docker Image lên Registry lưu trữ                                                                                 | 2026-07-27   | 2026-07-27      | [Deploy Application on Docker](https://000015.awsstudygroup.com/vi/1-introduce/)                                                         |
| 4   | - **Kiến trúc Amazon ECS & Cấu hình Cloud Map:**<br> - Tìm hiểu kiến trúc Amazon ECS, khái niệm Cluster, Task và Service<br> - Hoàn thành các bước chuẩn bị và đăng ký Namespace trên AWS Cloud Map<br> - Khởi tạo Amazon ECS Cluster phục vụ quản lý container                                                                                      | 2026-07-28   | 2026-07-28      | [Deploy applications on Amazon ECS](https://000016.awsstudygroup.com/vi/1-introduce/)                                                    |
| 5   | - **Cấu hình Task Definition, ALB & ECS Service:**<br> - Tạo ECS Task Definition quy định thông số RAM/CPU, port mapping và container image<br> - Thiết lập Application Load Balancer (ALB) đi kèm Target Group và Listener rules<br> - Khởi tạo ECS Service kết nối với ALB để tự động điều phối lượng truy cập                                     | 2026-07-29   | 2026-07-29      | [Deploy applications on Amazon ECS](https://000016.awsstudygroup.com/vi/1-introduce/)                                                    |
| 6   | - **Kiểm thử hệ thống & Dọn dẹp tài nguyên:**<br> - Kiểm tra kết quả triển khai ứng dụng bằng cách truy cập tên miền/IP của Application Load Balancer<br> - Xác minh trạng thái hoạt động (Health check) của các task container trên ECS<br> - Thực hiện xóa toàn bộ ECS Service, ECS Cluster, ALB, Cloud Map, RDS và EC2 để tránh phát sinh chi phí | 2026-07-30   | 2026-07-30      | [Deploy on Docker](https://000015.awsstudygroup.com/vi/1-introduce/) & [Deploy on ECS](https://000016.awsstudygroup.com/vi/1-introduce/) |

### Kết quả đạt được tuần 8:

- **Làm chủ kỹ năng Đóng gói & Triển khai Docker:**
  - Đóng gói thành công ứng dụng thành Docker Image và điều phối chạy đa dịch vụ mượt mà bằng Docker Compose trên EC2.
  - Kết nối ứng dụng containerized tới dịch vụ cơ sở dữ liệu quản lý Amazon RDS an toàn và ổn định.

- **Thành thạo Quản trị Container với Amazon ECS:**
  - Khởi tạo và quản lý thành công ECS Cluster, định nghĩa linh hoạt các Task Definition và cấu hình Service Discovery với AWS Cloud Map.
  - Tích hợp thành công Application Load Balancer (ALB) giúp phân phối tải truy cập mượt mà tới các container.

- **Quản trị Tài nguyên & Tối ưu Chi phí:**
  - Hoàn tất kiểm thử và dọn dẹp triệt để các tài nguyên ECS, ALB, Cloud Map, RDS, EC2 để tối ưu chi phí tài khoản.
