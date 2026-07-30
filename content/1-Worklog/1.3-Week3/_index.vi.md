---
title: "Worklog Tuần 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

- **Nền tảng & Kiến trúc Amazon RDS:**
  - Nắm vững khái niệm Amazon Relational Database Service (Amazon RDS), các cơ sở dữ liệu hỗ trợ (MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, Aurora) và bài toán OLTP.
  - Hiểu rõ cách thiết lập DB Subnet Groups (trên nhiều AZ), chọn loại ổ lưu trữ (General Purpose, Provisioned IOPS, Magnetic) và mô hình chi phí.
- **Cơ chế Cao khả dụng, Dự phòng & Bảo mật:**
  - Phân biệt kiến trúc Multi-AZ đồng bộ (đảm bảo tính cao khả dụng/DR) và Read Replicas bất đồng bộ (mở rộng khả năng đọc).
  - Hiểu quy trình sao lưu DB Snapshots, khôi phục theo thời điểm (Point-in-time restore), mã hóa dữ liệu qua AWS KMS và kết nối SSL.
- **Thực hành triển khai ứng dụng kết nối Cơ sở dữ liệu:**
  - Thực hiện các bước chuẩn bị (Prerequisite steps), khởi tạo máy chủ EC2 và tạo cơ sở dữ liệu Amazon RDS trong DB Subnet Group.
  - Triển khai ứng dụng (Application Deployment), thực hành Backup/Restore và thực hiện dọn dẹp tài nguyên (Clean up).

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                         | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                       |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------------------------------------------------------------- |
| 2   | - **Tổng quan Amazon RDS & Hạ tầng DB:**<br> - Tìm hiểu tổng quan Amazon RDS, lợi ích dịch vụ Managed Service, các DB Engine và Maintenance Windows<br> - Cấu hình DB Subnet Groups phân bổ trên tối thiểu 2 Availability Zones<br> - So sánh các loại ổ đĩa (gp2/gp3 vs Provisioned IOPS) và cách tính chi phí RDS               | 2026-06-21   | 2026-06-21      | [Nền tảng Amazon RDS](https://000005.awsstudygroup.com/1-introduce/) |
| 3   | - **Kiến trúc Multi-AZ, Read Replicas & Bảo mật:**<br> - Phân tích cơ chế nhân bản đồng bộ Multi-AZ và tự động chuyển vùng khi sự cố (Failover)<br> - Nghiên cứu triển khai Read Replicas (Cross-AZ, Cross-Region) cho các ứng dụng đọc nhiều<br> - Cấu hình mã hóa lưu trữ KMS và bảo mật kết nối qua SSL                        | 2026-06-22   | 2026-06-22      | [Nền tảng Amazon RDS](https://000005.awsstudygroup.com/1-introduce/) |
| 4   | - **Chuẩn bị hạ tầng & Khởi tạo RDS:**<br> - Thực hiện Prerequisite Steps (chuẩn bị VPC, Private/Public Subnets, Security Groups)<br> - Khởi tạo máy chủ Amazon EC2 đóng vai trò Web Application<br> - Tạo DB Instance Amazon RDS trong DB Subnet Group riêng biệt                                                                | 2026-06-23   | 2026-06-23      | [Nền tảng Amazon RDS](https://000005.awsstudygroup.com/1-introduce/) |
| 5   | - **Triển khai ứng dụng & Kết nối Database:**<br> - Cấu hình mã nguồn ứng dụng web trên máy chủ EC2<br> - Thiết lập DB Endpoint, cấu hình luật Security Group cho phép kết nối từ EC2 tới RDS<br> - Kiểm tra truy vấn dữ liệu CRUD và theo dõi qua CloudWatch / Enhanced Monitoring                                               | 2026-06-24   | 2026-06-24      | [Nền tảng Amazon RDS](https://000005.awsstudygroup.com/1-introduce/) |
| 6   | - **Sao lưu, Khôi phục & Dọn dẹp tài nguyên:**<br> - Tạo bản chụp thủ công DB Snapshots và thử nghiệm khôi phục Point-in-time restore<br> - Tìm hiểu dịch vụ chuyển đổi cơ sở dữ liệu AWS DMS, SCT và các mô hình Anti-patterns<br> - Tiến hành xóabắt các bản snapshot, RDS Instance và xóabắt EC2 Instance để hoàn tất Clean up | 2026-06-25   | 2026-06-25      | [Nền tảng Amazon RDS](https://000005.awsstudygroup.com/1-introduce/) |

### Kết quả đạt được tuần 3:

- **Nắm vững quản trị cơ sở dữ liệu Amazon RDS:**
  - Hiểu rõ mô hình Managed Database của AWS, cách chọn Instance Class, thiết lập cửa sổ bảo trì (Maintenance Window) và DB Subnet Groups.
  - Phân biệt rõ khi nào nên dùng RDS, DynamoDB, Redshift hay tự cài Database trên EC2.

- **Triển khai kiến trúc Cao khả dụng & Bảo mật:**
  - Thành thạo mô hình Multi-AZ để đảm bảo tính sẵn sàng cao và tự động khôi phục khi có sự cố.
  - Biết cách tối ưu hiệu năng đọc bằng cách bổ sung các bản sao Read Replicas.
  - Áp dụng thành công mã hóa dữ liệu KMS và thiết lập tường lửa Security Group bảo vệ DB.

- **Triển khai thành công ứng dụng thực tế:**
  - Dựng thành công mô hình ứng dụng web đa tầng kết nối giữa EC2 và Amazon RDS qua DB Endpoint an toàn.
  - Đảm bảo ứng dụng thực hiện các thao tác đọc/ghi dữ liệu chính xác.

- **Quản lý sao lưu & Tối ưu chi phí:**
  - Nắm vững quy trình tạo DB Snapshot và khôi phục dữ liệu theo mốc thời gian.
  - Hoàn thành đầy đủ các bước Clean up tài nguyên, tránh phát sinh chi phí duy trì sau bài Lab.
