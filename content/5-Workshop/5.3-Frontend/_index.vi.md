---
title: "Triển khai lớp giao diện"
date: 2026-07-28
weight: 3
chapter: false
pre: " <b> 5.3 </b> "
---

Trong phần này bạn sẽ triển khai giao diện web bằng **Amazon S3** và **Amazon CloudFront**.

- **Amazon S3** dùng để lưu trữ toàn bộ file tĩnh của ứng dụng React.
- **CloudFront** đóng vai trò CDN, phân phối nội dung đến người dùng với tốc độ nhanh và bảo mật hơn.

Điểm cần lưu ý là **bucket S3 sẽ hoàn toàn riêng tư (private)**. Người dùng sẽ **không truy cập trực tiếp vào S3** mà chỉ có thể truy cập thông qua CloudFront bằng cơ chế **Origin Access Control (OAC)**.

---

## Bước 1. Tạo bucket lưu giao diện

1. Mở **Amazon S3 Console**.

2. Chọn **Create bucket**.

3. Điền các thông tin:

| Thuộc tính              | Giá trị                                   |
| ----------------------- | ----------------------------------------- |
| **Bucket name**         | `fcj-recsys-frontend-<tên-bạn>`           |
| **AWS Region**          | Asia Pacific (Singapore) `ap-southeast-1` |
| **Block Public Access** | Giữ nguyên tất cả đều bật                 |

4. Chọn **Create bucket**.

![Tạo bucket](/images/5-Workshop/5.3/create-bucket.png)

{{% notice note %}}
Nhiều hướng dẫn cũ yêu cầu bật **Static Website Hosting** và mở quyền public cho bucket. Cách này hiện không còn được AWS khuyến nghị vì làm bucket có thể truy cập trực tiếp từ Internet.

Trong workshop này, bucket sẽ luôn ở trạng thái **private**, chỉ CloudFront mới có quyền đọc dữ liệu.
{{% /notice %}}

---

## Bước 2. Build giao diện

Di chuyển vào thư mục **frontend** và build project.

```bash
cd frontend
npm install
npm run build
```

Sau khi hoàn thành sẽ sinh ra thư mục:

```text
dist/
```

Đây là thư mục chứa toàn bộ file tĩnh sẽ được triển khai lên Amazon S3.

{{% notice tip %}}
Hiện tại chưa cần cấu hình địa chỉ API.

Sau khi hoàn thành phần **API Gateway** ở mục **5.5**, bạn sẽ cấu hình biến môi trường `VITE_API_BASE_URL` rồi build lại ứng dụng.
{{% /notice %}}

---

## Bước 3. Upload lên Amazon S3

Sử dụng AWS CLI:

```bash
aws s3 sync dist/ s3://fcj-recsys-frontend-<tên-bạn>/ --delete
```

Tham số:

```text
--delete
```

giúp xóa các file cũ không còn tồn tại trong bản build mới, tránh để lại dữ liệu dư thừa sau nhiều lần triển khai.

Sau khi upload xong, kiểm tra bucket cần có cấu trúc tương tự:

```text
index.html
assets/
favicon.ico
...
```

---

## Bước 4. Tạo CloudFront Distribution

Mở **CloudFront Console**.

Chọn **Create distribution**.

### Origin

Thiết lập:

| Thuộc tính    | Giá trị                                 |
| ------------- | --------------------------------------- |
| Origin domain | Bucket S3 vừa tạo                       |
| Origin access | **Origin Access Control (recommended)** |

Chọn **Create new OAC**.

Giữ nguyên toàn bộ cấu hình mặc định rồi chọn **Create**.

### Default cache behavior

Thiết lập:

| Thuộc tính             | Giá trị                |
| ---------------------- | ---------------------- |
| Viewer protocol policy | Redirect HTTP to HTTPS |
| Allowed HTTP methods   | GET, HEAD              |

### Settings

Thiết lập:

| Thuộc tính          | Giá trị      |
| ------------------- | ------------ |
| Default root object | `index.html` |

Sau đó chọn **Create distribution**.

![Tạo CloudFront Distribution](/images/5-Workshop/5.3/create-distribution.png)

---

## Bước 5. Cấp quyền cho CloudFront đọc bucket

Sau khi Distribution được tạo, CloudFront sẽ hiển thị thông báo yêu cầu cập nhật Bucket Policy.

Thực hiện:

1. Chọn **Copy policy**
2. Mở **S3 Console**
3. Chọn bucket
4. Vào tab **Permissions**
5. Chọn **Bucket Policy**
6. Chọn **Edit**
7. Dán policy vừa sao chép
8. Chọn **Save changes**

Bucket policy này chỉ cấp quyền đọc cho đúng CloudFront Distribution vừa tạo.

---

## Bước 6. Xử lý lỗi 403 và 404 cho React Router

React sử dụng **Client-side Routing**.

Ví dụ:

```text
https://domain.com/cart
```

CloudFront sẽ tìm file:

```text
/cart
```

trong S3.

Do file này không tồn tại nên CloudFront sẽ trả về:

```text
403 Forbidden
```

hoặc

```text
404 Not Found
```

Để xử lý, vào Distribution:

**Error pages → Create custom error response**

Tạo cấu hình:

| Thuộc tính               | Giá trị       |
| ------------------------ | ------------- |
| HTTP error code          | 403           |
| Customize error response | Yes           |
| Response page path       | `/index.html` |
| HTTP Response code       | 200           |

Sau đó tạo thêm một cấu hình tương tự cho lỗi:

```text
404 Not Found
```

---

## Bước 7. Quản lý biến môi trường (Environment Variables)

Dự án sử dụng **Vite**, do đó các biến môi trường phải có tiền tố:

```text
VITE_
```

Tạo file:

```text
frontend/.env
```

Ví dụ:

```env
VITE_API_BASE_URL=https://xxxxx.execute-api.ap-southeast-1.amazonaws.com
```

Đối với môi trường Production, nên sử dụng:

```text
.env.production
```

để tránh ảnh hưởng tới môi trường phát triển.

### Phân biệt biến môi trường

| Loại   | Tiền tố | Có thể truy cập từ Browser |
| ------ | ------- | -------------------------- |
| VITE\_ | Có      | Có                         |
| Khác   | Không   | Không                      |

Ví dụ:

```env
# Đúng
VITE_APP_TITLE=My Store
```

```env
# Sai
VITE_STRIPE_SECRET=sk_live_xxx
```

{{% notice warning %}}
Không lưu API Key, Secret Key hoặc bất kỳ thông tin nhạy cảm nào trong biến có tiền tố **VITE\_**, vì toàn bộ giá trị sẽ được đóng gói vào JavaScript và người dùng có thể xem được.
{{% /notice %}}

---

## Bước 8. Quản lý trạng thái với Redux Toolkit

Dự án sử dụng **Redux Toolkit** thay cho Context API để quản lý trạng thái toàn cục.

### Lý do

- Giảm số lượng component phải re-render.
- Hỗ trợ xử lý bất đồng bộ.
- Redux DevTools mạnh mẽ.
- Dễ mở rộng khi dự án lớn.

Ví dụ cấu trúc:

```text
store/
├── slices/
│   ├── authSlice.ts
│   ├── cartSlice.ts
│   ├── productsSlice.ts
│   └── uiSlice.ts
└── store.ts
```

Ví dụ sử dụng `createAsyncThunk`:

```typescript
export const fetchProducts = createAsyncThunk(
  "products/fetch",
  async (_, { rejectWithValue }) => {
    try {
      const response = await api.get("/products");
      return response.data;
    } catch (err: any) {
      return rejectWithValue(err.response.data);
    }
  },
);
```

---

## Bước 9. Bảo mật xác thực (JWT)

Trong dự án demo, JWT có thể được lưu trong:

```text
localStorage
```

để đơn giản hóa quá trình phát triển.

Tuy nhiên, trong môi trường Production, đây không phải là lựa chọn an toàn do nguy cơ tấn công XSS.

### So sánh

| Cách lưu               | Ưu điểm                           | Nhược điểm          | Mức độ an toàn |
| ---------------------- | --------------------------------- | ------------------- | -------------- |
| localStorage           | Đơn giản                          | Dễ bị XSS           | Thấp           |
| HttpOnly Cookie        | Không truy cập được từ JavaScript | Cần chống CSRF      | Cao            |
| Memory + Refresh Token | Bảo mật cao                       | Triển khai phức tạp | Rất cao        |

Khuyến nghị Production:

- Backend (AWS Lambda) thiết lập:

```text
HttpOnly
Secure
SameSite=Strict
```

Frontend không cần lưu JWT mà trình duyệt sẽ tự động gửi Cookie.

---

## Bước 10. Tối ưu hiệu năng

Một số kỹ thuật được áp dụng trong dự án:

- `React.memo`
- `useMemo`
- `useCallback`

Ví dụ:

```typescript
const filteredProducts = useMemo(() => {
  return products.filter((p) => p.category === selectedCategory);
}, [products, selectedCategory]);

const handleAddToCart = useCallback((product: Product) => {
  dispatch(addToCart(product));
}, []);
```

Khi số lượng sản phẩm lớn (trên 100–200 sản phẩm), nên kết hợp thêm:

- Lazy Loading
- Virtual Scrolling
- Code Splitting
- Image Lazy Loading

---

## Kiểm tra

Chờ khoảng **5 phút** để CloudFront chuyển sang trạng thái:

```text
Deployed
```

Sau đó mở địa chỉ:

```text
https://dxxxxxxxxxxxx.cloudfront.net
```

Giao diện ứng dụng sẽ hiển thị thành công như hình bên dưới hoặc bạn có thể xem qua đường link này:

https://d20h0irrznuf1m.cloudfront.net/

![Giao diện Web Frontend](/images/5-Workshop/5.3/a.png)
![Giao diện Web Frontend](/images/5-Workshop/5.3/b.png)

Trong giai đoạn này, dữ liệu sản phẩm chưa xuất hiện do API Gateway và Backend chưa được triển khai.

{{% notice warning %}}
Sau mỗi lần upload bản build mới lên Amazon S3, bạn cần tạo **CloudFront Invalidation** để xóa cache.

Nếu không, CloudFront sẽ tiếp tục trả về phiên bản cũ và bạn có thể nhầm tưởng rằng ứng dụng chưa được cập nhật.

```bash
aws cloudfront create-invalidation \
  --distribution-id <DISTRIBUTION_ID> \
  --paths "/*"
```

{{% /notice %}}
