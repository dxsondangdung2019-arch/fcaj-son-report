---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

- **Giám sát toàn diện hệ thống với Amazon CloudWatch:**
  - Nắm vững khái niệm Amazon CloudWatch để theo dõi end-to-end tài nguyên hạ tầng và ứng dụng, giúp giảm chỉ số MTTR (Mean Time To Resolution).
  - Quản lý các thành phần chính: CloudWatch Metrics (lưu trữ 15 tháng, tính toán theo thời gian thực), CloudWatch Logs, CloudWatch Alarms (cảnh báo theo ngưỡng) và CloudWatch Dashboards.
  - Hiểu về CloudWatch Container Insights để theo dõi, chẩn đoán lỗi cho các ứng dụng container chạy trên EKS, ECS, Fargate và Kubernetes.
- **Hệ thống hỗ trợ kỹ thuật AWS Support:**
  - Tìm hiểu tổng quan dịch vụ AWS Support, khả năng hỗ trợ toàn cầu 24/7 và các mức thời gian phản hồi SLA (từ 15 phút đến 24 giờ) gói gọn trong 1 ngày.
  - Phân biệt các gói hỗ trợ (AWS Support Plans), cách truy cập trung tâm hỗ trợ và quy trình tạo/quản lý yêu cầu hỗ trợ (Support Cases).
- **Thực hành triển khai Giám sát & Quản lý Yêu cầu:**
  - Thực hiện các bước chuẩn bị, cấu hình CloudWatch Metrics, CloudWatch Logs, CloudWatch Alarms và thiết kế Bảng điều khiển (Dashboard) trực quan.
  - Thực hành truy cập AWS Support, tạo và quản lý bài lab yêu cầu hỗ trợ kỹ thuật, sau đó tiến hành dọn dẹp tài nguyên.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                               | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                        |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | --------------------------------------------------------------------------------------------------------------------- |
| 2   | - **Tổng quan Amazon CloudWatch & Metrics:**<br> - Tìm hiểu kiến trúc Amazon CloudWatch, vai trò tập trung hóa Logs/Metrics và tối ưu MTTR<br> - Nghiên cứu tính năng CloudWatch Metrics, khả năng lưu trữ 15 tháng và phép tính trên metrics<br> - Tìm hiểu CloudWatch Container Insights trong việc giám sát ứng dụng containerized (EKS, ECS, Fargate, K8s)          | 2026-07-05   | 2026-07-05      | [AWS CloudWatch Workshop](https://000008.awsstudygroup.com/vi/)                                                       |
| 3   | - **Thực hành CloudWatch Logs & Phân tích Nhật ký:**<br> - Hoàn thành các bước chuẩn bị hạ tầng giám sát<br> - Cấu hình thu thập, định tuyến và phân tích dữ liệu log qua CloudWatch Logs<br> - Truy vấn nhật ký hệ thống để phát hiện và khắc phục sự cố ứng dụng                                                                                                      | 2026-07-06   | 2026-07-06      | [AWS CloudWatch Workshop](https://000008.awsstudygroup.com/vi/)                                                       |
| 4   | - **Thiết lập CloudWatch Alarms & Dashboards:**<br> - Thiết lập CloudWatch Alarms với ngưỡng cảnh báo tùy chỉnh để tự động hóa phản hồi sự cố<br> - Tạo Bảng điều khiển CloudWatch Dashboards trực quan hóa toàn bộ chỉ số vận hành hệ thống<br> - Kiểm tra khả năng phản hồi và hiển thị biểu đồ thời gian thực                                                        | 2026-07-07   | 2026-07-07      | [AWS CloudWatch Workshop](https://000008.awsstudygroup.com/vi/)                                                       |
| 5   | - **Tìm hiểu & Thực hành AWS Support (Tập trung 1 ngày):**<br> - Nghiên cứu các gói AWS Support Plans, thời gian phản hồi SLA và phạm vi hỗ trợ toàn cầu<br> - Phân tích vai trò của AWS Support trong việc tư vấn bảo mật, tuân thủ và kiến trúc hệ thống<br> - Truy cập AWS Support Center, thực hành tạo, cập nhật và quản lý bài lab yêu cầu hỗ trợ (Support Cases) | 2026-07-08   | 2026-07-08      | [Yêu cầu Hỗ trợ từ AWS Support](https://000009.awsstudygroup.com/vi/)                                                 |
| 6   | - **Kiểm thử hệ thống & Dọn dẹp tài nguyên:**<br> - Kiểm tra lại hoạt động kích hoạt cảnh báo Alarm và dữ liệu trên Dashboard<br> - Xử lý và đóng các yêu cầu hỗ trợ thử nghiệm<br> - Tiến hành xóa Dashboards, Alarms, Log Groups và các tài nguyên bài lab để tránh phát sinh chi phí                                                                                 | 2026-07-09   | 2026-07-09      | [AWS CloudWatch Workshop](https://000008.awsstudygroup.com/vi/) & [AWS Support](https://000009.awsstudygroup.com/vi/) |

### Kết quả đạt được tuần 5:

- **Làm chủ dịch vụ Giám sát Hệ thống (Amazon CloudWatch):**
  - Hiểu cách thu thập và quản lý tập trung toàn bộ dữ liệu chỉ số (metrics) và nhật ký (logs) trên cùng một nền tảng.
  - Ứng dụng thành công Container Insights để theo dõi hiệu năng CPU, bộ nhớ, mạng và chẩn đoán sự cố cho ứng dụng container.
  - Xây dựng thành công Bảng điều khiển (Dashboard) trực quan và thiết lập cảnh báo thông minh (Alarms) giúp phản hồi tự động trước sự cố.

- **Thành thạo quy trình AWS Support:**
  - Hiểu rõ sự khác biệt giữa các gói AWS Support Plans và tiêu chí lựa chọn gói phù hợp với doanh nghiệp thông qua chuyên đề học tập trong 1 ngày.
  - Nắm vững các bước tạo, gửi và quản lý yêu cầu hỗ trợ kỹ thuật với đội ngũ chuyên gia AWS theo chuẩn quy trình.

- **Tối ưu hóa Chi phí & Quản trị tài nguyên:**
  - Hoàn thành đầy đủ các bước Clean up bài lab (xóa Dashboards, Alarms, Log Streams, Test Instances) đảm bảo tài khoản không phát sinh chi phí ngoài ý muốn.
