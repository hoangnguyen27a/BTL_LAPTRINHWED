# Tài liệu Yêu cầu — Website CLB Kết Nối

> **Môn:** Lập trình Web và triển khai phần mềm, Khóa 20  
> **Học viện:** Học viện Nông nghiệp Việt Nam  
> **Người thực hiện:** Nguyễn Huy Hoàng  

---

## 1. Chủ đề, yêu cầu và tiêu chí thiết kế (Theo mẫu quy định)

- **Tên chủ đề và lý do chọn:** [Website CLB Kết Nối VNUA, lý do tôi chọn đó là muốn tạo ra một website để mọi người có thể biết đến CLB và lan tỏa tình yêu thương đẹp đến tất cả mọi người.]
- **Người xem chính:** [Các sinh viên tại trường và các mạnh thường quân quan tâm đến CLB.]
- **Mục tiêu quan sát được:** [Mọi người có thể quan sát được những nội dung như: giới thiệu CLB và những hoạt động của CLB và các sinh viên khi muốn tham gia có thể nhìn thấy đơn đăng ký tại website.]
- **Phạm vi và ràng buộc:** [Xây dựng và thiết kế front-end thuần túy từ HTML5 và CSS3 (kèm JavaScript thuần xử lý form phía client).]

---

## 2. Trước khi code: Trả lời 4 câu hỏi cốt lõi (Theo Slide 3 A3)

### Câu 1: Ai sẽ xem? (Target Audience)
- **Trả lời:**
  1. **Sinh viên tại trường (đặc biệt là tân sinh viên):** Vào tìm hiểu thông tin CLB, các hoạt động tình nguyện ý nghĩa và tìm form đăng ký tham gia.
  2. **Các mạnh thường quân & nhà hảo tâm:** Quan tâm đến các chiến dịch thiện nguyện (thu gom quần áo cũ, gây quỹ) và tìm thông tin liên hệ tài trợ.
  3. **Thành viên hiện tại của CLB:** Tra cứu lịch họp, theo dõi cơ cấu tổ chức và phân công công việc.
  4. **Giảng viên chấm bài BTL:** Kiểm tra tính ngữ nghĩa HTML5, giao diện responsive, khả năng truy cập (a11y) và quy trình A3.

### Câu 2: Họ cần làm gì? (User Tasks / Use Cases)
- **Trả lời:**
  - Nắm bắt được tôn chỉ hoạt động và 3 giá trị cốt lõi của CLB (*Tâm huyết, Đoàn kết, Trách nhiệm*).
  - Xem danh sách và hình ảnh/nội dung các hoạt động thiện nguyện chính.
  - Tra cứu thời gian, địa điểm qua bảng Lịch sinh hoạt hàng tuần.
  - Xem sơ đồ Cơ cấu tổ chức bộ máy CLB (Chủ nhiệm, Phó chủ nhiệm, các ban chức năng).
  - Điền và gửi thông tin vào Form đăng ký tham gia CLB trực tiếp trên trang web.
  - Lấy thông tin liên hệ (Email, Số điện thoại, Fanpage) và điều hướng nhanh qua menu.

### Câu 3: Website có gì? (Sitemap & Cấu trúc nội dung)
- **Trả lời:**
  - **Header (`<header>`):** Logo CLB, tên CLB và menu điều hướng 6 mục cố định (`position: sticky`).
  - **Hero Banner (`<section id="top">`):** Logo lớn 220px, slogan *"We love and we do"*, giới thiệu ngắn và 2 nút kêu gọi hành động (CTA).
  - **Giới thiệu (`#gioi-thieu`):** Lịch sử thành lập, mục tiêu và 3 giá trị cốt lõi.
  - **Hoạt động (`#hoat-dong`):** 3 thẻ Card trực quan (Thu gom phế liệu, Thu gom quần áo cũ, Bán hoa quyên góp).
  - **Lịch sinh hoạt (`#lich`):** Bảng biểu (`<table>`) hiển thị thời gian, hoạt động, nội dung; có khung `.table-wrap` cuộn ngang trên mobile.
  - **Cơ cấu tổ chức (`#co-cau`):** Sơ đồ 4 cấp phân tầng rõ ràng từ Chủ nhiệm đến Thành viên.
  - **Tuyển thành viên (`#tuyen-thanh-vien`):** Quy trình 3 bước ứng tuyển + Form đăng ký trực tuyến (5 trường bắt buộc).
  - **Liên hệ (`#lien-he`):** Danh sách định nghĩa (`<dl>`) gồm Email, Hotline, Fanpage.
  - **Footer (`<footer>`):** Bản quyền, thông tin quản trị viên web và nút cuộn về đầu trang.

### Câu 4: Kiểm tra bằng cách nào? (Tiêu chí chấp nhận & Phương pháp kiểm thử)
- **Trả lời:**
  - **Kiểm tra chuẩn cú pháp W3C:** Nạp code `index.html` vào công cụ W3C HTML Validator, đảm bảo không có lỗi cú pháp.
  - **Kiểm tra khả năng tiếp cận (Accessibility):** Dùng phím `Tab` để kiểm tra nút "Bỏ qua điều hướng" (Skip link) và viền focus trên nút bấm/input.
  - **Kiểm tra Responsive:** Mở Chrome DevTools (F12) kiểm tra trên màn hình điện thoại (375px - 430px), đảm bảo bố cục tự co về 1 cột dọc và không bị tràn thanh cuộn ngang toàn trang.
  - **Kiểm tra cuộn bảng lịch:** Trên màn hình hẹp, vuốt ngang bảng lịch để kiểm tra thanh cuộn ngang độc lập của `.table-wrap`.
  - **Kiểm tra Form Validation:**
    + Bỏ trống trường bắt buộc -> Trình duyệt kích hoạt cảnh báo `required`.
    + Nhập sai định dạng số điện thoại -> Hệ thống báo lỗi yêu cầu nhập đủ 10-11 số.
    + Nhập đầy đủ thông tin hợp lệ -> Form ẩn đi, hiển thị khung thông báo thành công và in log dữ liệu ra console.
  - **Kiểm tra triển khai Git & URL:** Kiểm tra lịch sử git có tag phiên bản (`v7`, `v8`), kiểm tra trang web chạy công khai trên GitHub Pages khớp phiên bản nộp.

---

## 3. Yêu cầu chức năng

### 3.1 Điều hướng
- Header cố định (sticky) ở đầu trang, chứa logo và menu điều hướng.
- Menu gồm 6 mục: Giới thiệu, Hoạt động, Lịch, Cơ cấu, Tuyển thành viên, Liên hệ.
- Mỗi mục menu khi nhấn cuộn đến đúng phần tương ứng (anchor link với smooth scroll).
- Có nút "Bỏ qua điều hướng" hỗ trợ người dùng bàn phím.

### 3.2 Nội dung các phần

| Phần | Yêu cầu nội dung |
|---|---|
| Hero | Logo CLB lớn, tên CLB, slogan, 2 nút CTA |
| Giới thiệu | Mô tả CLB, 3 giá trị cốt lõi (Tâm huyết, Đoàn kết, Trách nhiệm) |
| Hoạt động | 3 thẻ (card) mô tả các hoạt động chính |
| Lịch sinh hoạt | Bảng lịch họp và hoạt động hàng tuần |
| Cơ cấu tổ chức | Sơ đồ 4 cấp: Chủ nhiệm → Phó/Ủy viên → 3 Ban → Thành viên |
| Tuyển thành viên | Quy trình 3 bước + Form đăng ký |
| Liên hệ | Email, số điện thoại, fanpage |

### 3.3 Form đăng ký thành viên
- Các trường bắt buộc: Họ và tên, Lớp, Khóa học, Mã sinh viên, Số điện thoại.
- Kiểm tra số điện thoại: chỉ chấp nhận 10–11 chữ số.
- Khi gửi thành công: ẩn form, hiện thông báo cảm ơn.
- Khi số điện thoại sai định dạng: trình duyệt chặn bằng `pattern` HTML5 và có lớp kiểm tra dự phòng `alert` bằng JS.

---

## 4. Yêu cầu phi chức năng

### 4.1 Giao diện
- Responsive: hiển thị đúng trên máy tính (≥1024px), tablet (768px), điện thoại (≤480px).
- Bảng lịch sinh hoạt cuộn ngang trên màn hình nhỏ (không bị vỡ layout).
- Font và màu sắc nhất quán, dùng CSS variables.

### 4.2 Hiệu năng & Chuẩn mực
- Toàn bộ HTML dùng thẻ ngữ nghĩa (semantic HTML5).
- Có `meta charset`, `meta viewport`, `meta description`.
- Có favicon (`assets/img/logo.png`).
- Ảnh có thuộc tính `alt` đầy đủ.
- Bảng có `caption`, `thead`, `scope="col"`.
- JavaScript đặt cuối `<body>` để không chặn tải trang.

### 4.3 Khả năng tiếp cận (Accessibility)
- Skip link `#noi-dung` cho người dùng bàn phím.
- `aria-label` trên `<nav>`.
- Label liên kết với input qua `for` / `id`.
- Trường bắt buộc được đánh dấu rõ bằng `*` và `required`.

---

## 5. Phạm vi ngoài dự án

- Không cần backend hoặc lưu dữ liệu thực; form chỉ xử lý phía client.
- Không cần đăng nhập, quản trị, hay trang con riêng.
- Không yêu cầu tích hợp mạng xã hội thực tế (Fanpage link tạm dùng `#`).
