# 🛒 E-Commerce Dashboard

![Tình trạng dự án](https://img.shields.io/badge/Status-Active-success)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)

Hệ thống Quản trị (Admin Dashboard) chuyên nghiệp dành cho nền tảng Thương mại điện tử (E-Commerce). Dự án được xây dựng trên nền tảng web hiện đại với **Next.js (App Router)** mạnh mẽ, tái cấu trúc tốt và tối ưu hóa hiệu năng tối đa. Ứng dụng cung cấp bộ công cụ quản lý toàn diện bao gồm: theo dõi thống kê cửa hàng, quản lý danh mục, xử lý thông tin sản phẩm và theo dõi đơn hàng thời gian thực.

---

## ✨ Các tính năng nổi bật (Features)

- **📊 Bảng Điều khiển & Thống kê (Dashboard & Analytics)**
  - Trực quan hóa dữ liệu thống kê cửa hàng với các biểu đồ, thông số rõ ràng.
  - Cung cấp cái nhìn tổng quan, nhanh chóng về doanh số, lượng đơn hàng và chỉ số tăng trưởng.

- **📦 Quản lý Sản phẩm (Product Management)**
  - Thêm mới, chỉnh sửa và quản lý sản phẩm thông qua biểu mẫu (form) chi tiết và trực quan.
  - Phân loại, gán giá tiền, tình trạng kho hàng tiện lợi.

- **📁 Quản lý Danh mục (Category Management)**
  - Thiết lập cấu trúc phân cấp danh mục.
  - Tự động nhóm hoặc sắp xếp thuộc tính sản phẩm dựa trên từng dải phân loại.

- **🚚 Xử lý Đơn hàng (Order Processing)**
  - Theo dõi danh sách các đơn hàng dễ dàng thông qua bảng chi tiết.
  - Quản lý quá trình xác nhận trạng thái (Từ chờ thanh toán, đóng gói, đến hoàn thành).

- **🔐 Xác thực & Phân quyền (Authentication)**
  - Giao diện đăng nhập an toàn để đảm bảo chỉ những quản trị viên hợp lệ mới được tiếp cận luồng dữ liệu của toàn doanh nghiệp.

- **🌐 Tích hợp Ngrok Tunnels (Remote Tunnels)**
  - Public server phát triển tại Localhost của bạn ra bên ngoài dễ dàng bằng Webhook thông qua cấu hình có sẵn của Ngrok cho quá trình kiểm thử dịch vụ từ xa.

---

## 🛠️ Công nghệ sử dụng (Tech Stack)

Hệ thống được thiết kế với kiến trúc hiện đại, bao gồm:
- **Core Framework**: [Next.js](https://nextjs.org/) (Sử dụng kiến trúc App Router tiên tiến).
- **Language**: [TypeScript](https://www.typescriptlang.org/) (Đảm bảo Type-safety cho toàn bộ ứng dụng, code chuẩn xác và ít lỗi).
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) (Hệ thống utility classes, hỗ trợ Responsive & UX tuyệt vời).
- **Tooling**: ESLint, PostCSS.

---

## 🚀 Hướng dẫn cài đặt (Getting Started)

Làm theo các bước dưới đây để bắt đầu khởi chạy ứng dụng trực tiếp trên máy của bạn.

### Cài đặt môi trường
1. Mã nguồn yêu cầu môi trường Node.js. Vui lòng cài đặt ít nhất Node `v18.x`.
2. Clone repository này về máy của bạn:

```bash
git clone <đường-dẫn-repo>
cd ecommerce-dashboard
```

3. Cài đặt toàn bộ các thư viện phụ thuộc của dự án bằng một trong các package manager dưới đây:

```bash
npm install
# hoặc
yarn install
# hoặc
pnpm install
```

4. **Thiết lập biến môi trường**: Sao chép mẫu cấu hình để trỏ vào Database/API và Ngrok.
Bạn cần tạo file `.env.local` ở cùng cấp thư mục gốc dự án (tham khảo thông tin hướng dẫn Ngrok ở `NGROK_SETUP.md` nếu có).

### Khởi chạy môi trường Phát triển (Development)

Trong Terminal của bạn, nhập lệnh sau để khởi chạy:

```bash
npm run dev
# hoặc
yarn dev
```

Sau khi chạy xong, hãy sử dụng trình duyệt của bạn truy cập vào [http://localhost:3000](http://localhost:3000) hoặc địa chỉ Ngrok tùy biến của bạn (ví dụ: `https://abcd-efgh.ngrok-free.dev`) để trải nghiệm bảng điều khiển lập tức!

---

## 📂 Kiến trúc Dự án (Project Structure)

Dự án sử dụng cơ chế chia thư mục quy chuẩn để giúp Maintain code dễ nhất:

```text
ecommerce-dashboard/
├── app/                  # Nền tảng Next.js App Router (Chứa Routing, Layout hệ thống)
├── components/           # Các khối UI module hóa có thể tái sử dụng
│   ├─ auth/              # Giao diện cho đăng nhập & tính năng xác thực
│   └─ dashboard/         # Logic view chính (Thống kê, Quản lý Sản phẩm, Hóa đơn...)
├── hooks/                # React Hooks tùy biến (ví dụ: useAuth, useOrderStats)
├── lib/                  # Nơi định nghĩa các hàm tiện ích, cấu hình chung, constants...
├── types/                # Các Interfaces TypeScript định dạng (Product, Order, Category...)
└── public/               # Thư mục lưu trữ tài nguyên tĩnh (Hình ảnh, Fonts, Favicon...)
```

---

## ☁️ Hướng dẫn Triển khai (Deployment)

Dự án này tương thích tốt nhất với [Vercel](https://vercel.com/new) - Nhà sáng lập Next.js. Thực hiện liên kết trực tiếp Repo Github với Vercel để hệ thống tự động Build & Live site ứng dụng của bạn trong một nốt nhạc!

Để tìm hiểu các nền tảng Host hoặc máy chủ khác, hãy tham khảo [Tài liệu triển khai App Next.js](https://nextjs.org/docs/app/building-your-application/deploying).
