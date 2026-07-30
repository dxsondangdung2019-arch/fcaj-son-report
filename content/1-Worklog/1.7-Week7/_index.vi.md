---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

- **Nâng cao kỹ năng quản trị hạ tầng qua AWS CLI (Phần 2):**
  - Thành thạo quản trị tài nguyên nâng cao qua AWS CLI: cấu hình IAM (User/Role/Policy), khởi tạo VPC, Subnet và triển khai máy chủ EC2.
  - Nắm vững kỹ năng chẩn đoán, khắc phục lỗi phát sinh khi thao tác qua CLI và quy trình dọn dẹp tài nguyên.
- **Quản lý danh tính tập trung với AWS IAM Identity Center:**
  - Hiểu và triển khai AWS IAM Identity Center (tiền thân là AWS SSO) giúp quản lý truy cập tập trung đa tài khoản theo nguyên tắc Zero Trust và đặc quyền tối thiểu.
  - Thiết lập phân quyền dựa trên nhóm người dùng (Group-based access), cấu hình Customer Managed Policies và kiểm soát truy cập theo thời gian (Time-based access control).
  - Thao tác với IAM Identity Center Identity Store APIs qua dòng lệnh và hoàn tất dọn dẹp tài nguyên bài lab.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - **Thực hành AWS CLI nâng cao (IAM & VPC):**<br> - Sử dụng AWS CLI để quản lý IAM: tạo người dùng, nhóm, vai trò (roles) và gán quyền access policy<br> - Khởi tạo hạ tầng mạng VPC, Subnet, Route Table và Internet Gateway bằng CLI<br> - Thiết lập Security Groups và quy tắc truy cập inbound/outbound qua câu lệnh CLI                | 2026-07-19   | 2026-07-19      | [Làm quen với AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/)                                                              |
| 3   | - **Khởi tạo EC2 qua CLI & Khắc phục lỗi:**<br> - Thực hành khởi tạo và cấu hình máy chủ EC2 hoàn toàn bằng AWS CLI<br> - Khắc phục các lỗi phổ biến khi dùng CLI (lỗi xác thực credentials, thiếu quyền IAM, sai cú pháp)<br> - Xóa các tài nguyên EC2/VPC thử nghiệm của phần CLI                                                         | 2026-07-20   | 2026-07-20      | [Làm quen với AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/)                                                              |
| 4   | - **Cấu hình AWS IAM Identity Center & Time-based Access:**<br> - Hoàn thành các bước chuẩn bị và bật AWS IAM Identity Center<br> - Cấu hình danh mục người dùng, nhóm (Groups) và Permission Sets theo vai trò dự án<br> - Cấu hình Time-based access control nhằm giới hạn thời gian truy cập tạm thời                                    | 2026-07-21   | 2026-07-21      | [IAM Identity Center Workshop](https://000012.awsstudygroup.com/vi/1-introduce/)                                                      |
| 5   | - **Customer Managed Policies & Identity Store APIs:**<br> - Thiết kế và gắn Customer Managed Policies để kiểm soát truy cập chi tiết<br> - Sử dụng IAM Identity Center Identity Store APIs để quản lý người dùng và nhóm bằng dòng lệnh<br> - Thực hành kết hợp AWS CLI trong quản trị danh tính IAM Identity Center                       | 2026-07-22   | 2026-07-22      | [IAM Identity Center Workshop](https://000012.awsstudygroup.com/vi/1-introduce/)                                                      |
| 6   | - **Kiểm thử truy cập Đa tài khoản & Dọn dẹp tài nguyên:**<br> - Kiểm thử trải nghiệm đăng nhập Single Sign-On (SSO) vào các tài khoản AWS thuộc tổ chức<br> - Xác minh chính sách giới hạn quyền hạn và kiểm soát thời gian truy cập<br> - Tiến hành xóa Permission Sets, Users, Groups và các chính sách thử nghiệm để dọn dẹp tài nguyên | 2026-07-23   | 2026-07-23      | [AWS CLI](https://000011.awsstudygroup.com/vi/1-introduce/) & [IAM Identity Center](https://000012.awsstudygroup.com/vi/1-introduce/) |

### Kết quả đạt được tuần 7:

- **Làm chủ kỹ năng AWS CLI nâng cao:**
  - Tự tay khởi tạo và quản lý toàn bộ hệ thống từ IAM, VPC đến EC2 thông qua giao diện dòng lệnh.
  - Có kỹ năng phân tích log lỗi và khắc phục các sự cố thường gặp trong quá trình vận hành AWS CLI.

- **Quản trị danh tính doanh nghiệp với IAM Identity Center:**
  - Triển khai thành công giải pháp đăng nhập một lần (SSO) và quản lý quyền truy cập tập trung trên mô hình đa tài khoản AWS.
  - Làm chủ việc thiết lập Customer Managed Policies, giới hạn thời gian truy cập (Time-based access) và thao tác qua Identity Store APIs.

- **Dọn dẹp & An toàn hệ thống:**
  - Hoàn tất kiểm thử và dọn dẹp toàn bộ tài nguyên thử nghiệm, đảm bảo an toàn bảo mật và không phát sinh chi phí ngoài ý muốn.
