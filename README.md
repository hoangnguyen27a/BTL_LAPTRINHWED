# BTL_LAP TRINH WED — Website CLB Kết Nối

> **We love and we do** — Trang web giới thiệu CLB Kết Nối, câu lạc bộ tình nguyện trực thuộc Học viện Nông nghiệp Việt Nam.

---

## 📌 Thông tin bài tập lớn
- **Môn học:** Lập trình Web và Triển khai phần mềm (Khóa 20)
- **Học phần quy trình:** A3: Từ ý tưởng đến bàn giao (Khoa CNTT - Đại Nam)
- **Sinh viên thực hiện:** Nguyễn Huy Hoàng — Thành viên CLB Kết Nối
- **Kho lưu trữ (Repository):** [https://github.com/hoangnguyen27a/BTL_LAPTRINHWED](https://github.com/hoangnguyen27a/BTL_LAPTRINHWED)
- **Đường link chạy thực tế (GitHub Pages):** [https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/](https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/)
- **Phiên bản gắn Tag bàn giao:** `v8` (hoàn thiện nộp bài)

---

## 📖 Giới thiệu
Đây là **bài tập lớn môn Lập trình Web**, xây dựng một trang web tĩnh (static website) giới thiệu CLB Kết Nối — nơi hội tụ những trái tim nhiệt huyết, chung tay sẻ chia yêu thương và thực hiện các hoạt động tình nguyện vì cộng đồng sinh viên và xã hội.

---

## 🗂️ Cấu trúc dự án theo chuẩn A3

```
BTL_LAP TRINH WED/
├── index.html            # Trang chủ HTML5 ngữ nghĩa, tối ưu responsive
├── style.css             # Định dạng giao diện toàn trang (CSS Variables, Flexbox, Grid)
├── assets/
│   └── img/
│       └── logo.png      # Logo chính thức của CLB Kết Nối
├── docs/                 # Tài liệu quy trình kỹ thuật phần mềm (A3)
│   ├── yeu-cau.md        # Bước 1 & 2: Xác định chủ đề, 4 câu hỏi cốt lõi, phạm vi
│   ├── thiet-ke.md       # Bước 3: Thiết kế có lý do, Wireframe Desktop & Mobile
│   ├── kiem-thu.md       # Bước 5: Báo cáo kiểm thử "Thử thật, ghi thật" (Test Cases)
│   ├── san-pham.md       # Bước 4 & 6: Mô tả sản phẩm hoàn thiện và hướng dẫn bàn giao
│   └── BAO_CAO_BTL_A3.md # Báo cáo tổng hợp theo Rubric A3 của học phần
├── evidence/             # Minh chứng kiểm tra được (Screenshots)
│   ├── 01_yeu_cau/       # Minh chứng 4 câu hỏi & AI prompt
│   ├── 02_thiet_ke/      # Minh chứng bản vẽ Wireframe & Rationale
│   ├── 03_kiem_thu/      # Minh chứng các ca test thực tế (Responsive, Form, W3C)
│   ├── 04_trien_khai/    # Minh chứng Git log tags, repo & URL GitHub Pages
│   └── README.md         # Mục lục chi tiết các minh chứng
├── AI_LOG.md             # Nhật ký quá trình sử dụng AI có kiểm soát
└── README.md             # Hướng dẫn tổng quan dự án này
```

---

## ✨ Các phần chính của trang web

| Phần | ID | Nội dung |
|---|---|---|
| Header | `#top` | Thanh điều hướng dính cố định (sticky), logo và 6 menu liên kết |
| Hero | `#top` | Banner lớn giới thiệu logo CLB và 2 nút kêu gọi hành động (CTA) |
| Giới thiệu | `#gioi-thieu` | Lịch sử CLB và 3 giá trị cốt lõi: Tâm huyết, Đoàn kết, Trách nhiệm |
| Hoạt động | `#hoat-dong` | 3 thẻ card: Thu gom phế liệu, Thu gom quần áo cũ, Bán hoa quyên góp |
| Lịch sinh hoạt | `#lich` | Bảng lịch họp và hoạt động (hỗ trợ cuộn ngang trên điện thoại `.table-wrap`) |
| Cơ cấu tổ chức | `#co-cau` | Sơ đồ phân cấp 4 tầng: Chủ nhiệm → Phó/Ủy viên → 3 Ban → Thành viên |
| Tuyển thành viên | `#tuyen-thanh-vien` | Quy trình 3 bước + form đăng ký có kiểm tra tính hợp lệ dữ liệu |
| Liên hệ | `#lien-he` | Email, điện thoại, fanpage CLB |
| Footer | N/A | Bản quyền, thông tin sinh viên thực hiện, nút cuộn về đầu trang |

---

## 🛠️ Công nghệ sử dụng
- **HTML5:** Ngữ nghĩa (`header`, `nav`, `main`, `section`, `table`, `footer`), hỗ trợ tiếp cận (skip link, `aria-label`, `scope`).
- **CSS3:** Bố cục Flexbox và Grid responsive, hệ biến CSS `:root`, hiệu ứng mượt mà.
- **JavaScript thuần (Vanilla JS):** Kiểm tra bắt buộc nhập và số điện thoại regex `/^[0-9]{10,11}$/`, phản hồi trực quan.

## 🚀 Cách chạy dự án

### Cách 1: Chạy trực tiếp trên trình duyệt
Mở file `index.html` bằng trình duyệt web bất kỳ:
```powershell
start index.html
```

### Cách 2: Xem qua máy chủ tĩnh (Live Server)
```powershell
python -m http.server 8000
# Mở trình duyệt truy cập: http://localhost:8000
```

### Cách 3: Xem bản trực tuyến công khai (GitHub Pages)
Truy cập trực tiếp: [https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/](https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/)

---

## 🏷️ Các mốc phiên bản (Tags)
- **`v7`**: Mốc hoàn thiện các chức năng cơ bản và cấu trúc ban đầu.
- **`v8`**: Phiên bản hoàn thiện quy trình A3, bổ sung đầy đủ tài liệu `docs/`, minh chứng `evidence/` và triển khai GitHub Pages.

---

## 📄 Bản quyền
© 2026 CLB Kết Nối – Học viện Nông nghiệp Việt Nam. Dự án bài tập lớn phục vụ học tập.
