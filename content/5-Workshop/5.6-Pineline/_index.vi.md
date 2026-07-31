---
title: "Pipeline Data Engineering"
date: 2026-07-28
weight: 6
chapter: false
pre: " <b> 5.6 </b> "
---

Trong phần này bạn sẽ tìm hiểu **Pipeline Data Engineering** được xây dựng để làm sạch và chuẩn hóa dữ liệu tương tác trước khi bàn giao cho nhóm Machine Learning.

Pipeline tập trung vào việc **kiểm tra chất lượng dữ liệu**, **chuẩn hóa dữ liệu**, **bảo toàn định danh gốc** và **tạo các artifact phục vụ kiểm tra**. Pipeline **không huấn luyện mô hình**, **không triển khai frontend** và **không quản lý cơ sở dữ liệu của ứng dụng**.

---

## Quy trình xử lý

Quy trình này bao gồm các giai đoạn sau:
![Kiến Trúc Tổng Thể](/images/5-Workshop/architecture.png)

| Giai đoạn                          | Mô tả                                                                                                                                                                                                     |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Database Export**             | Dữ liệu được xuất từ hệ thống dưới dạng một file ZIP chứa `interactions.csv`, `Products.json` và `items.csv` (không sử dụng trong pipeline).                                                              |
| **2. Amazon S3**                   | File ZIP được tải lên bucket Amazon S3. Sự kiện `ObjectCreated` sẽ tự động kích hoạt AWS Lambda để bắt đầu xử lý dữ liệu.                                                                                 |
| **3. Processing Lambda**           | Lambda đọc dữ liệu từ file ZIP, kiểm tra cấu trúc dữ liệu, xác thực `EVENT_TYPE` và `TIMESTAMP`, đối chiếu `ITEM_ID` với `Products.json`, loại bỏ bản ghi trùng lặp và bảo toàn `USER_ID` cùng `ITEM_ID`. |
| **4. CloudWatch Logs**             | Trong suốt quá trình xử lý, Lambda ghi lại log thực thi và lỗi vào Amazon CloudWatch để phục vụ việc giám sát và kiểm tra.                                                                                |
| **5. Processed Dataset**           | Các bản ghi hợp lệ được ghi vào thư mục `processed/` dưới dạng `interactions_clean.csv`, sẵn sàng cho bước huấn luyện mô hình.                                                                            |
| **6. Rejected Dataset**            | Các bản ghi không hợp lệ được lưu trong thư mục `rejected/` cùng với lý do bị loại để phục vụ việc kiểm tra và khắc phục dữ liệu.                                                                         |
| **7. Data Quality Reports**        | Pipeline sinh các báo cáo `data_quality_report.json` và `data_quality_report.md`, cung cấp thống kê chất lượng dữ liệu và kết quả kiểm tra bảo toàn định danh.                                            |
| **8. Downstream Machine Learning** | Sau khi hoàn tất xử lý, dataset sạch và các báo cáo được bàn giao cho nhóm Machine Learning để sử dụng trong Amazon Personalize hoặc các bước đánh giá tiếp theo.                                         |

{{% notice info %}}
Toàn bộ hạ tầng của pipeline được triển khai bằng **AWS SAM/CloudFormation**, bao gồm Amazon S3, AWS Lambda, IAM Permissions, S3 Event Notification và CloudWatch Logs. Điều này giúp việc triển khai và quản lý hạ tầng được thực hiện tự động và nhất quán.
{{% /notice %}}

---

## Kiểm tra dữ liệu đầu vào

Pipeline đọc hai file bắt buộc:

- `interactions.csv`
- `Products.json`

File `interactions.csv` phải có bốn cột:

```text
USER_ID
ITEM_ID
EVENT_TYPE
TIMESTAMP
```

Trong đó:

- `USER_ID` và `ITEM_ID` là định danh của người dùng và sản phẩm.
- `EVENT_TYPE` là loại hành động của người dùng.
- `TIMESTAMP` là thời gian phát sinh tương tác theo Unix Timestamp.

`Products.json` được sử dụng để xây dựng danh sách sản phẩm hợp lệ nhằm kiểm tra `ITEM_ID` trong quá trình xử lý.

---

## Validation và chuẩn hóa dữ liệu

Pipeline thực hiện nhiều bước kiểm tra nhằm đảm bảo chất lượng dữ liệu trước khi bàn giao.

Các kiểm tra chính bao gồm:

- Thiếu `USER_ID`, `ITEM_ID` hoặc `TIMESTAMP`.
- `ITEM_ID` không tồn tại trong `Products.json`.
- `EVENT_TYPE` không thuộc tập giá trị hợp lệ (`view`, `add_to_cart`, `remove_from_cart`, `purchase`).
- `TIMESTAMP` không đúng định dạng Unix Timestamp.
- Phát hiện các dòng dữ liệu trùng lặp.

Trong quá trình chuẩn hóa:

- `EVENT_TYPE` được chuyển về chữ thường.
- `USER_ID` và `ITEM_ID` chỉ được loại bỏ khoảng trắng ở đầu và cuối.
- Định dạng, ký tự và giá trị của ID luôn được giữ nguyên.

---

## Bảo toàn định danh

Một yêu cầu quan trọng của pipeline là không tạo mới hoặc thay đổi định danh của người dùng và sản phẩm.

Sau khi xử lý:

- Không phát sinh `USER_ID` mới.
- Không phát sinh `ITEM_ID` mới.
- Toàn bộ ID trong dữ liệu đầu ra đều là tập con của dữ liệu đầu vào.

Điều này giúp dữ liệu sạch có thể được sử dụng trực tiếp trong hệ thống Recommendation mà không làm mất liên kết với dữ liệu nguồn.

---

## Kết quả đầu ra

Pipeline tạo bốn artifact phục vụ cho quá trình huấn luyện và kiểm tra dữ liệu.

| Artifact                    | Mục đích                                  |
| --------------------------- | ----------------------------------------- |
| `interactions_clean.csv`    | Dataset sạch sử dụng cho Machine Learning |
| `interactions_rejected.csv` | Các bản ghi bị loại cùng lý do            |
| `data_quality_report.json`  | Báo cáo chất lượng dữ liệu dạng JSON      |
| `data_quality_report.md`    | Báo cáo chất lượng dữ liệu dạng Markdown  |

Các artifact này được lưu trữ để phục vụ kiểm tra và bàn giao cho các bước xử lý tiếp theo.

---

## Thực thi trên AWS

Pipeline được triển khai theo mô hình **event-driven** sử dụng Amazon S3 và AWS Lambda.

Khi một file ZIP được tải lên bucket Amazon S3:

1. Amazon S3 phát sinh sự kiện `ObjectCreated`.
2. AWS Lambda được kích hoạt tự động.
3. Lambda đọc dữ liệu từ file ZIP.
4. Pipeline thực hiện kiểm tra và làm sạch dữ liệu.
5. Các artifact được ghi trở lại Amazon S3.

Mô hình này giúp toàn bộ quá trình xử lý diễn ra tự động mà không cần can thiệp thủ công.

---

## Kết quả kiểm thử

Sau khi xử lý bộ dữ liệu mẫu, pipeline thu được kết quả sau:

| Chỉ số          | Giá trị |
| --------------- | ------: |
| Input rows      |  23.377 |
| Clean rows      |  23.377 |
| Rejected rows   |       0 |
| Duplicate rows  |       0 |
| Unique Users    |     200 |
| Unique Items    |     100 |
| Product IDs     |     100 |
| ID Preservation |    PASS |

Kết quả cho thấy toàn bộ dữ liệu hợp lệ, không phát sinh định danh mới và sẵn sàng được sử dụng cho bước huấn luyện mô hình.

---

## Kiểm thử tự động

Pipeline được kiểm thử bằng **48 test case** bao gồm:

- Kiểm tra cấu trúc file ZIP.
- Kiểm tra schema dữ liệu.
- Kiểm tra Product Lookup.
- Kiểm tra Duplicate Detection.
- Kiểm tra Output Schema.
- Kiểm tra ID Preservation.
- Kiểm tra Lambda Event.
- Kiểm tra vị trí lưu output.

Việc kiểm thử giúp đảm bảo pipeline hoạt động ổn định trước khi triển khai trên AWS.

---

## Bàn giao cho Machine Learning

Sau khi pipeline hoàn tất, nhóm Machine Learning sẽ nhận các artifact:

- `interactions_clean.csv`
- `data_quality_report.json`
- `data_quality_report.md`

Từ đây, dữ liệu sẽ được sử dụng để import vào Amazon Personalize, huấn luyện mô hình, đánh giá kết quả và triển khai hệ thống gợi ý sản phẩm.
