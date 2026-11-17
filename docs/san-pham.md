# Tài liệu Sản phẩm — Website CLB Kết Nối

> **Môn:** Lập trình Web và triển khai phần mềm, Khóa 20
> **Người thực hiện:** Nguyễn Huy Hoàng — Thành viên CLB Kết Nối
> **Học viện:** Học viện Nông nghiệp Việt Nam

---

## 1. Mô tả sản phẩm

**Website CLB Kết Nối** là trang web tĩnh một trang (single-page) giới thiệu toàn diện về Câu lạc bộ tình nguyện Kết Nối trực thuộc Học viện Nông nghiệp Việt Nam. Trang web được xây dựng thuần bằng HTML5, CSS3 và JavaScript không dùng thư viện ngoài.

---

## 2. Các tính năng đã hoàn thành

### ✅ Điều hướng
- Header sticky dính đầu trang khi cuộn, chứa logo CLB và menu 6 mục.
- Tất cả anchor link (`#gioi-thieu`, `#hoat-dong`, `#lich`, `#co-cau`, `#tuyen-thanh-vien`, `#lien-he`) hoạt động đúng.
- Skip link "Bỏ qua điều hướng" trỏ đến `#noi-dung` cho người dùng bàn phím.
- Nút "↑ Về đầu trang" ở footer.

### ✅ Hero (Banner)
- Logo CLB hiển thị kích thước lớn (220×220px).
- Tiêu đề: "CLB Kết Nối — We love and we do".
- Mô tả ngắn và 2 nút CTA: **Tham gia CLB** (trỏ `#tuyen-thanh-vien`) và **Xem hoạt động** (trỏ `#hoat-dong`).

### ✅ Giới thiệu
- Đoạn mô tả lịch sử và mục tiêu CLB.
- Danh sách 3 giá trị cốt lõi: Tâm huyết, Đoàn kết, Trách nhiệm.

### ✅ Hoạt động
- 3 card hoạt động chính:
  1. **Thu gom phế liệu** — giấy vụn, chai nhựa gây quỹ.
  2. **Thu gom quần áo cũ** — gửi tặng đồng bào vùng cao.
  3. **Bán hoa, quyên góp tiền** — dịp lễ 20/10, 8/3.

### ✅ Lịch sinh hoạt
- Bảng 3 hàng: Họp thành viên (Thứ 5 hàng tuần), Thu gom phế liệu (Chủ nhật), Bán hoa (ngày lễ lớn).
- Cuộn ngang trên màn hình nhỏ nhờ `.table-wrap`.

### ✅ Cơ cấu tổ chức
Sơ đồ 4 cấp:
- **Chủ nhiệm:** Phạm Thị Diệu Hồng
- **Phó chủ nhiệm:** Phạm Đình Đồng | **Ủy viên:** Ban Điều Hành
- **Ban Hậu cần** | **Ban Văn thể** | **Ban Truyền thông sự kiện**
- **Thành viên**

### ✅ Form tuyển thành viên
- Quy trình 3 bước: Điền thông tin → Phỏng vấn → Nhận kết quả.
- Form 5 trường bắt buộc: Họ tên, Lớp, Khóa học, Mã sinh viên, Số điện thoại.
- Kiểm tra số điện thoại bằng regex `/^[0-9]{10,11}$/`.
- Hiển thị thông báo thành công sau khi gửi, ẩn form.

### ✅ Liên hệ
- Email: `ketnoifamily.vnua@gmail.com`
- Điện thoại: `036 698 2195`
- Fanpage: CLB Kết Nối - VNUA

### ✅ Footer
- Bản quyền © 2026 CLB Kết Nối – Học viện Nông nghiệp Việt Nam.
- Thông tin quản trị web: Nguyễn Huy Hoàng.

---

## 3. Công nghệ sử dụng

| Công nghệ | Phiên bản | Mục đích |
|---|---|---|
| HTML5 | — | Cấu trúc ngữ nghĩa trang web |
| CSS3 | — | Giao diện, layout, responsive |
| JavaScript (ES5+) | — | Xử lý form đăng ký phía client |

Không dùng framework, thư viện ngoài hay CDN.

---

## 4. Cấu trúc file sản phẩm

```
BTL_LAP TRINH WED/
├── index.html          # Trang chủ duy nhất (432 dòng)
├── style.css           # Giao diện toàn trang
├── assets/
│   └── img/
│       └── logo.png    # Logo CLB Kết Nối
├── docs/               # Tài liệu dự án
├── evidence/           # Ảnh chụp minh chứng
├── AI_LOG.md           # Nhật ký sử dụng AI
└── README.md           # Hướng dẫn dự án
```

---

## 5. Hướng dẫn chạy sản phẩm

Không cần cài đặt. Mở file `index.html` bằng bất kỳ trình duyệt hiện đại nào (Chrome, Edge, Firefox):

```powershell
start index.html
```

Hoặc dùng Live Server trong VS Code để xem thay đổi trực tiếp.

---

## 6. Giới hạn hiện tại

- Form đăng ký **chưa gửi dữ liệu thực** đến server hay email — chỉ xử lý phía client.
- Link Fanpage hiện dùng `#` chờ cập nhật URL thực tế.
- Không có trang con riêng (tất cả trên một file HTML).
