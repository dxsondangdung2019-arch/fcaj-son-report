---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

- **Nghiên cứu sâu về Amazon VPC & Hạ tầng mạng:**
  - Đào sâu kiến trúc VPC tùy chỉnh, phân chia Subnet nâng cao, Route Table, Internet Gateway và NAT Gateway.
  - Nắm chắc cơ chế bảo mật mạng VPC (Security Groups & Network ACLs) cùng mô hình kết nối Site-to-Site VPN.
- **Nền tảng Amazon EC2 & Hệ điều hành:**
  - Hiểu rõ các thành phần cốt lõi của EC2: Instance Types (tối ưu Compute, Memory, Storage, Network), AMIs, phân biệt EBS Volume và Instance Store Volume.
  - Làm chủ các phương thức bảo mật EC2: Key Pairs, Security Groups, IAM Roles và AWS Systems Manager Session Manager.
- **Thực hành triển khai ứng dụng & Quản trị chi phí:**
  - Khởi tạo và cấu hình máy chủ Microsoft Windows Server 2025 và Amazon Linux 2023.
  - Triển khai ứng dụng Node.js trên EC2 Windows và ứng dụng AWS User Management trên Amazon Linux.
  - Thực hành Quản trị chi phí (Cost & Usage Governance) với IAM và quy trình dọn dẹp tài nguyên.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                            | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                   |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------------------------------------------------------------------------- |
| 2   | - **Nghiên cứu nâng cao Amazon VPC:**<br> - Ôn tập và đi sâu vào thiết kế VPC tùy chỉnh, dải IP CIDR IPv4/IPv6 và Subnets<br> - Phân tích cấu hình định tuyến phức tạp với Route Table, Internet Gateway và NAT Gateway<br> - Tìm hiểu cơ chế Firewall trong VPC và mô hình kết nối Site-to-Site VPN | 2026-06-14   | 2026-06-14      | [Nghiên cứu sâu Amazon VPC & VPN](https://000003.awsstudygroup.com/1-introduce/) |
| 3   | - **Kiến trúc Amazon EC2 & Lưu trữ:**<br> - Tìm hiểu các họ EC2 Instance (General Purpose, Compute, Memory Optimized)<br> - So sánh các loại AMIs (AWS-provided, Marketplace, Custom AMIs)<br> - Phân biệt ổ lưu trữ bền vững EBS Volume và ổ tạm thời Instance Store Volume                         | 2026-06-15   | 2026-06-15      | [Giới thiệu Amazon EC2](https://000004.awsstudygroup.com/1-introduce/)           |
| 4   | - **Bảo mật EC2 & Triển khai máy chủ:**<br> - Cấu hình Key Pairs, Elastic IP, Security Groups và SSM Session Manager<br> - Khởi tạo máy chủ Microsoft Windows Server 2025<br> - Khởi tạo máy chủ Amazon Linux 2023 trong Subnet tùy chỉnh                                                            | 2026-06-16   | 2026-06-16      | [Giới thiệu Amazon EC2](https://000004.awsstudygroup.com/1-introduce/)           |
| 5   | - **Thực hành triển khai ứng dụng:**<br> - Triển khai ứng dụng AWS User Management trên Amazon Linux 2023<br> - Triển khai ứng dụng Node.js trên máy chủ EC2 Windows<br> - Kiểm tra kết nối ứng dụng và truy cập qua Elastic IP                                                                      | 2026-06-17   | 2026-06-17      | [Giới thiệu Amazon EC2](https://000004.awsstudygroup.com/1-introduce/)           |
| 6   | - **Quản trị chi phí & Dọn dẹp tài nguyên:**<br> - Thiết lập chính sách Cost & Usage Governance thông qua IAM và Tags<br> - Hủy liên kết và giải phóng Elastic IP không sử dụng, xóabắt các Instance không cần thiết<br> - Thực hiện quy trình Clean up tài nguyên hoàn chỉnh                        | 2026-06-18   | 2026-06-18      | [Giới thiệu Amazon EC2](https://000004.awsstudygroup.com/1-introduce/)           |

### Kết quả đạt được tuần 2:

- **Thành thạo hạ tầng mạng nâng cao (Amazon VPC):**
  - Hiểu sâu cơ chế phân chia Subnet, định tuyến bảng Route Table, kết nối Internet Gateway và NAT Gateway.
  - Nắm vững kiến trúc bảo mật mạng với VPC Firewall và khái niệm kết nối Hybrid qua Site-to-Site VPN.

- **Nắm trọn vòng đời máy chủ Amazon EC2:**
  - Đánh giá và lựa chọn đúng EC2 Instance Type phù hợp với từng loại ứng dụng (Compute, Memory, Bandwidth).
  - Phân biệt chính xác giữa EBS Volume (Dữ liệu không mất khi Stop) và Instance Store Volume (Mất dữ liệu khi Stop).
  - Sử dụng thành thạo các phương thức truy cập an toàn: Key Pair, IAM Roles và Systems Manager Session Manager.

- **Triển khai thành công ứng dụng đa hệ điều hành:**
  - Khởi tạo hoàn chỉnh 2 máy chủ chạy Windows Server 2025 và Amazon Linux 2023.
  - Triển khai hoạt động thành công ứng dụng Node.js trên nền tảng EC2 Windows.
  - Triển khai thành công ứng dụng AWS User Management trên máy chủ Amazon Linux.

- **Tối ưu chi phí & Quản trị tài nguyên:**
  - Áp dụng các quy tắc Quản trị chi phí (Cost Governance) dựa trên IAM và thẻ Tags.
  - Hoàn thành quy trình Clean up dọn dẹp tài nguyên bài Lab (giải phóng Elastic IPs, xóabắt EC2) tránh phát sinh chi phí.
