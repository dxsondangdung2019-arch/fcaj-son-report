---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

- **Kiến trúc Hybrid DNS với Route 53 Resolver:**
  - Nắm vững giải pháp tích hợp hệ thống DNS On-Premise hiện có với dịch vụ Amazon Route 53 trên AWS.
  - Hiểu rõ 3 công cụ cốt lõi của Route 53 Resolver: Inbound Endpoints (xử lý truy vấn từ On-Premise lên AWS), Outbound Endpoints (gửi truy vấn từ AWS về On-Premise) và Resolver Rules (quy tắc chuyển tiếp tên miền).
  - Khởi tạo các thành phần tiền đề bao gồm Remote Desktop Gateway (RDGW), Microsoft Active Directory (AD) và cấu hình DNS.
- **Thực hành AWS CLI (Phần 1 - Các dịch vụ cốt lõi):**
  - Hiểu tổng quan về công cụ AWS Command Line Interface (AWS CLI), khả năng tương tác API trực tiếp và hỗ trợ đa nền tảng (Linux, Windows, Remote SSH/SSM).
  - Cài đặt, cấu hình thông tin xác thực AWS CLI đảm bảo nguyên tắc đặc quyền tối thiểu và an toàn bảo mật.
  - Làm chủ các câu lệnh điều khiển dịch vụ Amazon S3 và Amazon SNS thông qua giao diện dòng lệnh.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                               | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                               |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| 2   | - **Nền tảng Hybrid DNS & Chuẩn bị môi trường:**<br> - Tìm hiểu tổng quan Amazon Route 53, Private Hosted Zone và cơ chế phân giải đệ quy<br> - Nghiên cứu tính năng Route 53 Resolver: Inbound Endpoints, Outbound Endpoints và Resolver Rules<br> - Thực hiện các bước chuẩn bị và kết nối tới RDGW (Remote Desktop Gateway)          | 2026-07-12   | 2026-07-12      | [Thiết lập Hybrid DNS với Route 53 Resolver](https://000010.awsstudygroup.com/vi/1-introduce/)                               |
| 3   | - **Triển khai Microsoft AD & Cấu hình Hybrid DNS:**<br> - Triển khai Microsoft Active Directory trên EC2 giả lập môi trường DNS On-Premise<br> - Cấu hình Inbound & Outbound Endpoints trên Route 53 Resolver<br> - Thiết lập quy tắc chuyển tiếp DNS (Forwarding Rules) và kiểm tra phân giải tên miền 2 chiều                        | 2026-07-13   | 2026-07-13      | [Thiết lập Hybrid DNS với Route 53 Resolver](https://000010.awsstudygroup.com/vi/1-introduce/)                               |
| 4   | - **Giới thiệu & Cài đặt AWS CLI:**<br> - Tìm hiểu lợi ích của AWS CLI, các tính năng nâng cao và khả năng tự động hóa bằng script<br> - Tiến hành cài đặt AWS CLI trên máy tính và cấu hình Credentials (Access Key, Secret Key, Region)<br> - Thực hành các câu lệnh kiểm tra thông tin tài khoản và truy vấn tài nguyên cơ bản       | 2026-07-14   | 2026-07-14      | [Làm quen với AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/)                                                     |
| 5   | - **Thực hành AWS CLI với Amazon S3 & Amazon SNS:**<br> - Sử dụng AWS CLI để quản lý Amazon S3: tạo bucket, tải lên/tải xuống tập tin, liệt kê và phân quyền<br> - Thực hành lệnh AWS CLI với Amazon SNS: tạo Topic, cấu hình Subscription và phát bản tin thông báo                                                                    | 2026-07-15   | 2026-07-15      | [Làm quen với AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/)                                                     |
| 6   | - **Kiểm thử Hybrid DNS & Dọn dẹp tài nguyên:**<br> - Xác nhận hệ thống phân giải tên miền Hybrid hoạt động chính xác giữa AWS và On-Premise<br> - Thực hiện xóa Route 53 Resolver Endpoints, Rules, Microsoft AD và RDGW để hoàn tất bài lab Hybrid DNS<br> - Giữ lại môi trường AWS CLI phục vụ cho nội dung thực hành tuần tiếp theo | 2026-07-16   | 2026-07-16      | [Hybrid DNS](https://000010.awsstudygroup.com/vi/1-introduce/) & [AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/) |

### Kết quả đạt được tuần 6:

- **Thành thạo Kiến trúc Mạng & Hybrid DNS:**
  - Tích hợp thành công hệ thống DNS On-Premise với Amazon Route 53 thông qua Inbound/Outbound Endpoints và Resolver Rules.
  - Hiểu cách cấu hình phân giải tên miền thông suốt giữa các tài nguyên trên Cloud và On-Premise.

- **Kỹ năng sử dụng AWS CLI (Phần 1):**
  - Cài đặt và làm chủ môi trường AWS CLI, biết cách bảo vệ Access Keys an toàn.
  - Thành thạo thao tác với Amazon S3 và Amazon SNS bằng các câu lệnh dòng lệnh, hỗ trợ tốt cho việc viết script tự động hóa.

- **Quản lý Tài nguyên & Tối ưu Chi phí:**
  - Hoàn thành dọn dẹp các tài nguyên thuộc bài lab Hybrid DNS (Resolver endpoints, EC2 AD, RDGW) để tránh chi phí duy trì.
