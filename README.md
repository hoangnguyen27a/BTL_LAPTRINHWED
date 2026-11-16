# BTL_LAP TRINH WED — Website CLB Kết Nối

> **We love and we do** — Trang web giới thiệu CLB Kết Nối, câu lạc bộ tình nguyện trực thuộc Học viện Nông nghiệp Việt Nam.

## 📖 Giới thiệu

Đây là **bài tập lớn môn Lập trình Web** (khóa 20), xây dựng một trang web tĩnh (static website) giới thiệu CLB Kết Nối — nơi hội tụ những trái tim nhiệt huyết, chung tay sẻ chia yêu thương và thực hiện các hoạt động tình nguyện vì cộng đồng sinh viên và xã hội.

## 🗂️ Cấu trúc dự án

```
BTL_LAP TRINH WED/
├── index.html      # Trang chủ (HTML ngữ nghĩa, có chú thích tiếng Việt)
├── style.css       # Toàn bộ định dạng giao diện (responsive)
├── assets/
│   └── img/        # Hình ảnh (logo CLB, ...)
├── AI_LOG.md       # Nhật ký quá trình làm việc với AI
└── README.md       # Tài liệu này
```

## ✨ Các phần chính của trang web

| Phần | ID | Nội dung |
|---|---|---|
| Hero | `#top` | Banner giới thiệu với logo CLB và nút kêu gọi hành động |
| Giới thiệu | `#gioi-thieu` | Về CLB và 3 giá trị cốt lõi: Tâm huyết, Đoàn kết, Trách nhiệm |
| Hoạt động | `#hoat-dong` | Thu gom phế liệu, thu gom quần áo cũ, bán hoa quyên góp |
| Lịch sinh hoạt | `#lich` | Bảng lịch họp và hoạt động hàng tuần |
| Cơ cấu tổ chức | `#co-cau` | Sơ đồ Ban Chủ nhiệm, các ban chức năng và thành viên |
| Tuyển thành viên | `#tuyen-thanh-vien` | Quy trình tham gia + form đăng ký có kiểm tra dữ liệu |
| Liên hệ | `#lien-he` | Email, điện thoại, fanpage |

## 🛠️ Công nghệ sử dụng

- **HTML5** — ngữ nghĩa, có chú thích chi tiết bằng tiếng Việt, hỗ trợ tiếp cận (skip link, `aria-label`, `scope`).
- **CSS3** — bố cục responsive, hiển thị tốt trên điện thoại và máy tính.
- **JavaScript thuần (vanilla JS)** — xử lý form đăng ký thành viên: kiểm tra số điện thoại (10–11 chữ số) và hiển thị thông báo thành công.

## 🚀 Cách chạy

Không cần cài đặt gì, chỉ cần mở file `index.html` bằng trình duyệt:

```powershell
# Cách 1: Mở trực tiếp
start index.html

# Cách 2: Dùng Live Server (VS Code) hoặc chạy server tĩnh
python -m http.server 8000
# Sau đó truy cập http://localhost:8000
```

## 📝 Form đăng ký thành viên

Form thu thập: Họ tên, Lớp, Khóa học, Mã sinh viên, Số điện thoại. Các trường đều bắt buộc, số điện thoại được kiểm tra bằng regex `/^[0-9]{10,11}$/`. Hiện tại dữ liệu chỉ được xử lý phía client (hiển thị thông báo thành công) — có thể mở rộng kết nối backend hoặc Google Form sau.

## 👤 Thành viên thực hiện

- **Quản trị web:** Nguyễn Huy Hoàng — Thành viên CLB Kết Nối
- Môn học: Lập trình Web và triển khai phần mềm, khóa 20

## 📄 Bản quyền

© 2026 CLB Kết Nối – Học viện Nông nghiệp Việt Nam. Trang web phục vụ học tập.
