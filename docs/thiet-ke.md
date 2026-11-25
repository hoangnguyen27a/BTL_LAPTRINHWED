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

| Biến | Giá trị | Vai trò |
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
- Nền trắng (`#fff`), viền dưới vàng 3px (`--mau-vang`), chữ xanh đậm (`--mau-xanh-dam`).
- Flexbox căn chỉnh logo trái, nav phải (tự căn giữa xuống dòng trên màn hình hẹp).

### 4.2 Nút bấm (Button)
- `.btn-primary`: nền vàng (`--mau-vang`), chữ xanh đậm (`--mau-xanh-dam`) — dùng cho CTA chính.
- `.btn-ghost`: viền trắng, nền trong suốt — dùng trên nền tối (hero).

### 4.3 Card hoạt động
- 3 thẻ `<article class="card">` đặt trong `.cards` (CSS Grid: 1 cột trên mobile, 2 cột trên tablet, 3 cột trên desktop).
- Bo góc `--bo-goc` (14px), viền xám nhạt (`--mau-vien`), viền vàng 4px trên đầu (`--mau-vang`), nền trắng.
- Trên điện thoại tự động xếp 1 cột.

### 4.4 Bảng lịch sinh hoạt
- Bọc trong `.table-wrap` có `overflow-x: auto` để cuộn ngang trên màn hình nhỏ (`table { min-width: 520px; }`).
- `<th>` tiêu đề cột nền xanh (`--mau-xanh`), chữ trắng; viền ô đồng bộ (`--mau-vien`).
- `<th scope="col">` và `<caption>` đảm bảo tính tiếp cận.

### 4.5 Sơ đồ cơ cấu tổ chức
- 4 hàng `.org-level` xếp bằng CSS Grid (`display: grid`), tự co 1 cột trên mobile và mở rộng 2–3 cột trên tablet/desktop.
- `.role-top` (Chủ nhiệm): nền xanh đậm (`--mau-xanh-dam`), chữ trắng, tên `.ten-noi-bat` nền vàng nổi bật nhất.
- `.role-pho` (Phó chủ nhiệm): nền xanh nhạt (`#eef2fc`), viền xanh 2px (`--mau-xanh`), tên nền xanh đậm.
- `.role-ban` (3 ban chức năng): đồng đều 3 cột, viền vàng 4px trên đầu.

### 4.6 Form đăng ký
- Mỗi trường dùng `.form-nhom`: `<label>` trên, `<input>` dưới.
- Viền input đổi sang xanh và có hào quang focus nhẹ khi chọn.
- Trường bắt buộc có `<span class="bat-buoc">*</span>` màu đỏ.
- Nút gửi rộng 100% khung form (`.btn-gui { width: 100%; }`).

---

## 5. Responsive Breakpoints

| Breakpoint | Áp dụng cho |
|---|---|
| `min-width: 640px` (tablet) | Cards và bước quy trình chuyển sang 2 cột, cơ cấu tổ chức 2–3 cột, `.form-box` tối đa 480px |
| `min-width: 960px` (desktop) | Hero chia 2 cột (`auto 1fr`), Cards 3 cột, Liên hệ 3 cột ngang |
| `max-width: 520px` (mobile) | Header & nav căn giữa xuống dòng gọn gàng, tăng `scroll-padding-top: 120px`, giảm padding section & form |

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
│   ├── kiem-thu.md     # Kết quả kiểm thử
│   └── BAO_CAO_BTL_A3.md # Báo cáo tổng hợp Rubric A3
├── evidence/           # Ảnh chụp màn hình minh chứng
├── AI_LOG.md           # Nhật ký sử dụng AI
└── README.md           # Hướng dẫn dự án
```
