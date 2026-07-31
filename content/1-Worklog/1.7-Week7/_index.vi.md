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
  - Nắm vững kỹ năng chẩn đoán, khắc phục lỗi phát sinh khi thao tác qua CLI và quy trình dọn dẹp tài nguyên.### Mục tiêu tuần 7:

- **Tích hợp Full-Stack & Sửa lỗi (Bug Fixing):**
  - Tích hợp ứng dụng frontend với backend APIs để có chức năng end-to-end hoàn chỉnh.
  - Triển khai xử lý lỗi mạnh mẽ, validation dữ liệu và luồng dữ liệu mượt mà giữa FE và BE.
  - Xác định, theo dõi và sửa lỗi trên toàn bộ ứng dụng.
- **Tích hợp API & Quản lý State:**
  - Kết nối các component frontend với RESTful APIs hoặc GraphQL endpoints.
  - Triển khai quản lý state hiệu quả cho API responses và tương tác người dùng.
  - Xử lý loading states, error states và các trường hợp biên trong fetch dữ liệu.
- **Kiểm thử, Tối ưu & Triển khai:**
  - Thực hiện kiểm thử end-to-end toàn diện cho ứng dụng full-stack đã tích hợp.
  - Tối ưu hiệu suất, chất lượng mã và trải nghiệm người dùng.
  - Chuẩn bị triển khai cuối cùng và tài liệu cho ứng dụng hoàn chỉnh.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                         | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                                                                                                              |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 2   | - **Tích hợp Full-Stack (Phần 1 - Kết nối API):**<br> - Thiết lập cấu hình API client và biến môi trường<br> - Kết nối luồng xác thực frontend với backend authentication APIs<br> - Tích hợp các thao tác CRUD cho tất cả tính năng chính<br> - Triển khai request/response interceptors cho API calls<br> - Cấu hình CORS và xử lý headers xác thực API (JWT tokens)                                            | 2026-07-19   | 2026-07-19      | [Axios Documentation](https://axios-http.com/) <br> [React Documentation](https://react.dev/)                                                                               |
| 3   | - **Tích hợp Full-Stack (Phần 2 - Quản lý State & Luồng dữ liệu):**<br> - Triển khai quản lý state toàn cục cho dữ liệu API (Redux/Zustand/Context API)<br> - Tạo custom hooks cho fetch dữ liệu và chiến lược caching<br> - Xây dựng đồng bộ dữ liệu real-time giữa FE và BE<br> - Xử lý optimistic updates để cải thiện trải nghiệm người dùng<br> - Triển khai phân trang, sắp xếp và lọc với truy vấn backend | 2026-07-20   | 2026-07-20      | [React Query Documentation](https://tanstack.com/query/) <br> [Zustand Documentation](https://zustand-demo.pmnd.rs/)                                                        |
| 4   | - **Xử lý Lỗi & Validation:**<br> - Triển khai xử lý lỗi toàn diện cho lỗi API (network errors, server errors, validation errors)<br> - Tạo thông báo lỗi thân thiện và fallback UI components<br> - Triển khai form validation với phản hồi thời gian thực<br> - Thêm global error boundaries và error logging<br> - Xử lý tình huống offline/online và retry logic cho các request thất bại                     | 2026-07-21   | 2026-07-21      | [React Error Boundaries](https://react.dev/reference/react/Component#catching-rendering-errors-with-an-error-boundary) <br> [React Hook Form](https://react-hook-form.com/) |
| 5   | - **Sửa lỗi (Bug Fixing) & Kiểm thử:**<br> - Xác định và sửa lỗi có hệ thống trên toàn bộ ứng dụng<br> - Viết integration tests cho tương tác FE-BE<br> - Thực hiện end-to-end testing cho các luồng người dùng quan trọng<br> - Debug vấn đề hiệu suất và tối ưu các API chậm<br> - Sửa lỗi UI/UX và vấn đề responsive<br> - Thực hiện code review và refactor code có vấn đề                                    | 2026-07-22   | 2026-07-22      | [React Testing Library](https://testing-library.com/react) <br> [Cypress Documentation](https://www.cypress.io/)                                                            |
| 6   | - **Tối ưu cuối cùng & Triển khai:**<br> - Tối ưu dung lượng bundle, tốc độ tải và hiệu suất runtime<br> - Cấu hình môi trường production và biến môi trường<br> - Triển khai ứng dụng full-stack đã tích hợp lên cloud (AWS/DigitalOcean/Vercel)<br> - Thiết lập monitoring và logging cho production<br> - Tạo tài liệu triển khai và hướng dẫn sử dụng<br> - Kiểm thử hệ thống cuối cùng và đảm bảo chất lượng | 2026-07-23   | 2026-07-23      | [AWS Amplify Documentation](https://docs.aws.amazon.com/amplify/) <br> [Vercel Documentation](https://vercel.com/docs)                                                      |

### Kết quả đạt được tuần 7:

- **Tích hợp Full-Stack Xuất sắc:**
  - Tích hợp thành công ứng dụng frontend với backend APIs, đảm bảo chức năng end-to-end hoàn chỉnh.
  - Triển khai quản lý state mạnh mẽ với chiến lược fetch dữ liệu và caching được tối ưu.
  - Đạt được luồng dữ liệu mượt mà giữa frontend và backend với xử lý lỗi phù hợp.

- **Giải quyết Bug & Chất lượng Code:**
  - Xác định và giải quyết có hệ thống tất cả lỗi quan trọng và không quan trọng trên toàn bộ ứng dụng.
  - Triển khai xử lý lỗi, validation và cơ chế phản hồi thân thiện với người dùng.
  - Viết integration và end-to-end tests để đảm bảo độ tin cậy và ổn định của ứng dụng.

- **Ứng dụng sẵn sàng Production:**
  - Triển khai ứng dụng full-stack đã tích hợp hoàn chỉnh lên môi trường production.
  - Tối ưu hiệu suất, dung lượng bundle và tốc độ tải để có trải nghiệm người dùng tốt nhất.
  - Tạo tài liệu đầy đủ cho triển khai, cấu hình và sử dụng.

- **Phát triển Chuyên môn:**
  - Phát triển kỹ năng full-stack kết hợp chuyên môn frontend với tích hợp backend.
  - Có kinh nghiệm trong kiểm thử, debug và tối ưu ứng dụng full-stack phức tạp.
  - Xây dựng ứng dụng sẵn sàng production, có khả năng mở rộng với các thực hành phát triển hiện đại.
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
