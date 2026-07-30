---
title: "Event 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch "AWS First Cloud AI Journey Community Day - June 2026"

### Thông Tin Chung

Đây là sự kiện cộng đồng được tổ chức online bởi AWS Study Group, phát trực tiếp trên YouTube vào sáng thứ Bảy, ngày 27/06/2026, từ 9h đến 12h. Sự kiện ban đầu dự kiến diễn ra tại Bitexco Financial Tower, TP.HCM. Tôi tham gia với vai trò người tham dự.

### Mục Đích Của Sự Kiện

Buổi chia sẻ quy tụ các founder và chuyên gia trong ngành để kể lại những trải nghiệm thực tế khi làm việc với Cloud và AI. Ngoài phần chia sẻ kinh nghiệm, chương trình còn đi sâu vào cách xây dựng và vận hành một Voice Agent trên nền tảng AWS bằng Amazon Bedrock, cách các công cụ AI như DevOps Agent và Amazon Q đang được dùng để giải quyết các bài toán vận hành IT và nhân sự hàng ngày, và khép lại bằng chủ đề bảo mật khi tích hợp AI qua MCP Server.

### Danh Sách Diễn Giả

- **Steve Tran** – Founder, Cloud Thinker
- **Nghi, Kiet, Trung** – Diễn giả phiên Voice AI (Renova Cloud, Student Video Group, R AI)
- **Bao & Nguyen** – Cloud Kinetis
- **Truong & Minh Anh** – Noventis
- **Toan Nguyen & Nghi** – Phiên Security & Amazon Q Integration

### Nội Dung Nổi Bật

#### Tư duy "Cloud Thinker" khi xây dựng sản phẩm

Steve Tran mở đầu bằng câu chuyện khởi nghiệp của chính mình và những khó khăn khi vận hành một Contact Center. Điều đọng lại nhất với tôi là: trước khi bắt tay viết code, kỹ sư cần thực sự hiểu "nỗi đau" của khách hàng — công nghệ chỉ nên là bước tiếp theo, không phải điểm xuất phát.

#### Voice AI trong thực tế, cho thị trường Việt Nam

Đây là phần kỹ thuật đậm đặc nhất buổi sáng. Nghi trình bày kiến trúc tổng thể để xây dựng một hệ thống Voice AI hoàn chỉnh, sau đó Kiet demo trực tiếp một Voice Agent chạy trên nền Amazon Bedrock. Trung tiếp nối bằng góc nhìn thực chiến khi triển khai giải pháp này cho doanh nghiệp lớn tại Việt Nam — từ chuyện giọng vùng miền, từ vựng chuyên ngành, cho đến điều quan trọng nhất: thiết kế kịch bản chuyển giao mượt mà giữa AI và con người (human fallback) khi AI không xử lý được.

#### DevOps Agent như một công cụ vận hành

Bao và Nguyen cho thấy cách một Dev Agent có thể giúp đội IT tự động truy tìm nguyên nhân gốc rễ của sự cố, từ đó rút ngắn thời gian hệ thống bị downtime — một cách trực tiếp để giảm Mean Time To Recovery.

#### Amazon Q trong lĩnh vực nhân sự

Truong và Minh Anh đưa câu chuyện sang mảng back-office, chia sẻ cách Amazon Q đang được ứng dụng để tự động hóa một phần quy trình tuyển dụng, từ sàng lọc ứng viên đến phân tích dữ liệu HR một cách khách quan hơn.

#### Giữ an toàn: tích hợp với MCP Server

Toan Nguyen và Nghi khép lại phần kỹ thuật bằng cách giải thích cách cấu hình bảo mật riêng cho Amazon Q, và cách MCP Server cho phép AI kết nối với các hệ thống bên thứ ba mà không đánh đổi an toàn dữ liệu.

### Những Gì Học Được

**Về tư duy sản phẩm** — Một Voice Agent chỉ thực sự trở thành sản phẩm khi nó xử lý được sự "lộn xộn" của hội thoại đời thực (giọng vùng miền, tiếng lóng) và luôn chừa chỗ cho con người can thiệp khi cần.

**Về nền tảng công nghệ** — Tôi có được hiểu biết bước đầu về Amazon Bedrock và cách các ứng dụng GenAI được xây dựng trên đó, lần đầu tiên tiếp cận kiến trúc MCP và lý do nó quan trọng để mở rộng khả năng của AI một cách an toàn, cùng cái nhìn rõ hơn về việc AI không chỉ dùng để trò chuyện mà còn có thể đọc log, phân tích nguyên nhân và hỗ trợ debug hệ thống thực sự hữu ích.

### Ứng Dụng Vào Công Việc

Sắp tới, tôi muốn chậm lại trước khi lao vào code, thay vào đó áp dụng thói quen của Steve Tran là phân tích kỹ vấn đề và bối cảnh trước khi thiết kế giải pháp. Tôi cũng đưa Amazon Bedrock vào danh sách cần tìm hiểu cho các dự án GenAI sắp tới, và sẽ áp dụng quy trình phân tích nguyên nhân gốc rễ từ phiên DevOps Agent vào lần debug tiếp theo trong các bài lab AWS của mình.

### Trải Nghiệm Trong Event

Dù chỉ theo dõi online qua YouTube, FCAJ Community Day vẫn mang lại cảm giác khá sống động.

**Demo giúp lý thuyết trở nên dễ hình dung** — Xem Kiet demo Voice Agent và Bao trình bày DevOps Agent giúp những khái niệm vốn trừu tượng trở nên trực quan và dễ hiểu hơn hẳn.

**Nhiều góc nhìn khác nhau trong cùng một buổi** — Với diễn giả đến từ Cloud Thinker, Renova Cloud, R AI, Cloud Kinetis và Noventis, chương trình di chuyển tự nhiên giữa các vấn đề kỹ thuật như bảo mật, kiến trúc và các vấn đề kinh doanh như vận hành HR, Contact Center.

**Một cộng đồng luôn sát cánh** — Sự kiện khép lại bằng tấm ảnh lưu niệm và hoạt động giveaway, một khoảnh khắc nhỏ nhưng cho thấy rõ sự gắn kết của cộng đồng AWS Study Group, và điều đó khiến tôi có thêm động lực để tiếp tục theo đuổi con đường cloud technology.

**Một số hình ảnh khi tham gia sự kiện**
_Thêm các hình ảnh của các bạn tại đây_

> Nhìn chung, sự kiện là một cầu nối trọn vẹn giữa công nghệ AI hiện đại và thực tế vận hành doanh nghiệp. Nó giúp tôi có thêm nền tảng kiến trúc vững hơn và một tư duy hướng đến giá trị rõ ràng hơn cho hành trình Cloud sắp tới của mình.
