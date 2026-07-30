---
title: "Tự đánh giá"
date: 2026-07-29
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

#### Bảng tự đánh giá

| Tiêu chí           | Mức độ         | Nhận xét                                                              |
| ------------------ | -------------- | --------------------------------------------------------------------- |
| Kiến thức          | Khá            | Nắm vững kiến trúc serverless và các dịch vụ cốt lõi của AWS          |
| Khả năng học hỏi   | Khá            | Chủ động khai thác tài liệu chính hãng và áp dụng qua thực hành       |
| Tính chủ động      | Khá            | Tích cực cải thiện chất lượng dữ liệu giúp tối ưu hệ thống gợi ý      |
| Kỷ luật            | Khá            | Tuân thủ quy trình phát triển và hoàn thành công việc đúng hạn        |
| Giao tiếp          | Khá            | Diễn đạt tốt các khái niệm kỹ thuật với các thành viên trong nhóm     |
| Teamwork           | Trung bình khá | Đúc kết bài học về việc thống nhất chuẩn dữ liệu/API ngay từ đầu      |
| Giải quyết vấn đề  | Khá            | Đã hình thành tư duy phân tích lỗi theo chuỗi và xử lý tận gốc        |
| Đóng góp cho dự án | Khá            | Trực tiếp triển khai hạ tầng AWS và hỗ trợ hoàn thiện tính năng gợi ý |

#### Nhận xét chi tiết theo từng tiêu chí

**Kiến thức — Khá**

Trước kỳ thực tập, kiến thức về Điện toán đám mây của em chủ yếu dừng ở mức lý thuyết. Qua quá trình làm dự án thực tế, em đã trực tiếp triển khai mô hình Serverless sử dụng các dịch vụ AWS như Lambda, API Gateway, DynamoDB, S3 và CloudFront. Em đã nắm rõ cách các dịch vụ này tương tác với nhau cũng như lý do lựa chọn chúng cho bài toán của nhóm.

Để hoàn thiện hơn, em dự định nâng cao kiến thức về mạng trong cloud như cấu hình VPC, Subnet và Security Groups—những phần dự án vừa qua chưa khai thác sâu.

**Khả năng học hỏi — Khá**

Dự án đặt ra yêu cầu tự học rất cao. Thay vì phụ thuộc vào các bài hướng dẫn đơn giản, em đã rèn luyện thói quen đọc tài liệu chính thức (AWS Docs) và tự xây dựng các bài thử nghiệm nhỏ (POC) để hiểu sâu bản chất.

Em nhận ra rằng "chương trình chạy được" chỉ là bước đầu, việc hiểu rõ "tại sao nó chạy" mới giúp hệ thống ổn định. Do đó, khi gặp lỗi, em luôn đào sâu tìm nguyên nhân gốc rễ thay vì áp dụng các giải pháp tạm thời.

**Tính chủ động — Khá**

Khi kết quả của hệ thống gợi ý chưa đạt kì vọng, em đã chủ động phân tích các điểm nghẽn và cùng nhóm tinh chỉnh lại bộ dữ liệu sao cho phản ánh chính xác hành vi người dùng. Nhờ đó, chất lượng gợi ý đã được cải thiện rõ rệt.

Bên cạnh đó, em cũng chủ động theo dõi chi phí sử dụng tài nguyên AWS và rà soát các thiết lập bảo mật cơ bản trước khi đưa ứng dụng lên môi trường thực tế.

**Kỷ luật — Khá**

Em luôn tuân thủ tiến độ chung và hoàn thành tốt các nhiệm vụ được giao. Dù giai đoạn đầu có tốn chút thời gian định hướng do lượng kiến thức mới khá rộng, em đã nhanh chóng điều chỉnh tập trung vào mục tiêu chính ngay khi bài toán của dự án được chốt hạ.

**Giao tiếp — Khá**

Làm việc cùng các thành viên có thế mạnh kỹ thuật khác nhau giúp em nâng cao kỹ năng truyền đạt. Em đã tự tin hơn trong việc giải thích các khái niệm về hạ tầng AWS một cách đơn giản, dễ hiểu cho cả nhóm.

Em sẽ tiếp tục rèn luyện kỹ năng trình bày và lắng nghe để phối hợp hiệu quả hơn trong các nhóm phát triển lớn sau này.

**Teamwork — Trung bình khá**

Bài học lớn nhất em rút ra về làm việc nhóm là tầm quan trọng của việc thống nhất quy chuẩn dữ liệu (schema) và chuẩn giao tiếp API ngay từ bước khởi chạy.

Sự lệch pha nhỏ giữa dữ liệu Frontend và Backend ở giai đoạn đầu đã tiêu tốn thêm thời gian tích hợp. Kinh nghiệm này giúp em chủ động chốt hợp đồng dữ liệu (data contract) rõ ràng hơn trong các dự án tiếp theo.

**Giải quyết vấn đề — Khá**

Tư duy xử lý lỗi của em đã chuyên nghiệp hơn. Thay vì thử nghiệm cảm tính, em tuân thủ quy trình bài bản: phân tích log, khoanh vùng sự cố và kiểm thử từng thành phần.

Điển hình như sự cố giao diện mới không hiển thị sau khi deploy, em đã xác định được nguyên nhân do cơ chế bộ nhớ đệm (edge cache) của CloudFront và thực hiện xử lý vô hiệu hóa cache (invalidation) thành công.

**Đóng góp cho dự án — Khá**

Em đã đóng góp trực tiếp vào việc cấu hình hạ tầng Serverless trên AWS, tích hợp các thành phần hệ thống và tối ưu tính năng gợi ý sản phẩm. Em cũng tích cực tham gia vào giai đoạn kiểm thử end-to-end và sửa lỗi trước khi bàn giao.

Chương trình thực tập đã mang lại cho em trải nghiệm thực tế quý giá và sự tự tin khi xây dựng ứng dụng cloud-native trên nền tảng AWS.

#### Hướng phát triển

Sau kỳ thực tập, em đặt mục tiêu ôn luyện và chinh phục chứng chỉ **AWS Certified Solutions Architect – Associate**. Đồng thời, em sẽ thực hiện thêm các dự án cá nhân để trau dồi chuyên sâu về Cloud Networking, Container (Docker/ECS) và Infrastructure as Code (IaC).
