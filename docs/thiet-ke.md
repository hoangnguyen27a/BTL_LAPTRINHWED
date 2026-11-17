# Tài liệu Thiết kế — Website CLB Kết Nối

> **Môn:** Lập trình Web và triển khai phần mềm, Khóa 20
> **Người thực hiện:** Nguyễn Huy Hoàng

---

## 1. Cấu trúc trang (Layout)

Trang web gồm một file HTML duy nhất (`index.html`) với bố cục theo thứ tự từ trên xuống:

```
┌──────────────────────┐
│  HEADER (sticky)            │  ← logo + nav 6 mục
├──────────────────────────┤
│  HERO                       │  ← logo lớn + tiêu đề + 2 nút CTA
├──────────────┤
│  GIỚI THIỆU  (#gioi-thieu)  │  ← mô tả CLB + 3 giá trị cốt lõi
├──────────────────┤
│  HOẠT ĐỘNG  (#hoat-dong)    │  ← 3 card hoạt động
├────────────────────┤
│  LỊCH SINH HOẠT  (#lich)    │  ← bảng 3 hàng
├─────────────────────────┤
│  CƠ CẤU TỔ CHỨC  (#co-cau) │  ← sơ đồ 4 cấp
├─────────────────┤
│  TUYỂN THÀNH VIÊN           │  ← quy trình 3 bước + form đăng ký
├──────────────────┤
│  LIÊN HỆ  (#lien-he)        │  ← email, SĐT, fanpage
├──────────────────────┤
│  FOOTER                     │  ← bản quyền + link về đầu trang
└───────────────────────┘
```

---

## 2. Hệ thống màu sắc

Màu được định nghĩa qua CSS variables trong `:root`, áp dụng nhất quán toàn trang:

| Biến | Gi Vai trò |
|---|---|---|
| `--mau-xanh` | `#3058a8` | Màu chủ đạo (nút, link, header) |
| `--mau-xanh-dam` | `#203888` | Hover state, nhấn mạnh |
| `--mau-vang` | `#f2c200` | Màu nhấn phụ (accent) |
| `--mau-trang` | `#ffffff` | Nền sáng, chữ trên nền tối |
| `--mau-nen-nhat` | `#f3f6fb` | Nền section xen kẽ (section-alt) |
| `--mau-chu` | `#1c2540` | Chữ chính |
| `--mau-chu-phu` | `#55607a` | Chữ phụ, mô tả |
| `--mau-vien` | `#d6deee` | Viền card, bảng |
| `--bo-goc` | `14px` | Độ bo tròn góc thống nhất |

---

## 3. Typography

- **Font stack:** `system-ui, -apple-system, "Segoe UI", Roboto, Arial, sans-serif` — dùng font hệ thống, không cần tải thêm.
- Màu chữ mặc định: `var(--mau-chu)` (#1c2540).
- Màu chữ phụ: `var(--mau-chu-phu)` (#55607a).

---

## 4. Các thành phần giao diện (Components)

### 4.1 Header
- `position: sticky; top: 0` — dính đầu trang khi cuộn.
- Nền xanh chủ đạo (`--mau-xanh`), chữ trắng.
- Flexbox căn chỉnh logo trái, nav phải.

### 4.2 Nút bấm (Button)
- `.btn-primary`: nền vàng (`--mau-vang`), chữ tối — dùng cho CTA chính.
- `.btn-ghost`: viền trắng, nền trong suốt — dùng trên nền tối (hero).

### 4.3 Card hoạt động
- 3 thẻ `<article class="card">` đặt trong `.cards` (CSS Grid 3 cột trên desktop).
- Bo góc `--bo-goc`, đổ bóng nhẹ, nền trắng.
- Trên điện thoại tự động xếp 1 cột.

### 4.4 Bảng lịch sinh hoạt
- Bọc trong `.table-wrap` có `overflow-x: auto` để cuộn ngang trên màn hình nhỏ.
- `<thead>` nền xanh, chữ trắng; hàng xen kẽ màu nền nhạt.
- `<th scope="col">` và `<caption>` đảm bảo tính tiếp cận.

### 4.5 Sơ đồ cơ cấu tổ chức
- 4 hàng `.org-level` xếp bằng Flexbox, căn giữa.
- `.role-top` (Chủ nhiệm): viền màu vàng nhấn, nổi bật nhất.
- `.role-pho` (Phó chủ nhiệm): viền xanh đậm.
- `.role-ban` (3 ban chức năng): đồng đều, nền nhạt.

### 4.6 Form đăng ký
- Mỗi trường dùng `.form-nhom`: `<label>` trên, `<input>` dưới.
- Viền input đổi sang xanh khi focus.
- Trường bắt buộc có `<span class="bat-buoc">*</span>` màu đỏ.
- Nút gửi full-width trên di động.

---

## 5. Responsive Breakpoints

| Breakpoint | Áp dụng cho |
|---|---|
| `min-width: 640px` (tablet) | Cards chuyển sang 2 cột, form rộng hơn |
| `min-width: 960px` (desktop) | Cards 3 cột, sơ đồ org đầy đủ ngang |
| `max-width: 520px` (mobile) | Nav ẩn hoặc thu gọn, padding giảm |

---

## 6. Cấu trúc file

```
BTL_LAP TRINH WED/
├── index.html          # Toàn bộ nội dung trang
├── style.css           # Toàn bộ CSS (variables, layout, components, responsive)
├── assets/
│   └── img/
│       └── logo.png    # Logo CLB Kết Nối
├── docs/
│   ├── yeu-cau.md      # Tài liệu yêu cầu
│   ├── thiet-ke.md     # Tài liệu này
│   ├── san-pham.md     # Mô tả sản phẩm
│   └── kiem-thu.md     # Kết quả kiểm thử
├── evidence/           # Ảnh chụp màn hình minh chứng
├── AI_LOG.md           # Nhật ký sử dụng AI
└── README.md           # Hướng dẫn dự án
```
