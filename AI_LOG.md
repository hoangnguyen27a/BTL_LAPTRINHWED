# AI_LOG.md — Nhật ký quá trình sử dụng AI

> Ghi lại quá trình xây dựng website **CLB Kết Nối** (Bài tập lớn môn Lập trình Web, khóa 20) với sự hỗ trợ của AI. Đây là minh chứng cho việc sử dụng AI có kiểm soát: AI chỉ hỗ trợ, người thực hiện vẫn hiểu và kiểm soát toàn bộ code.

---

## 📅 Buổi 1 — Lên ý tưởng và cấu trúc trang

**Mục tiêu:** Xây dựng trang web giới thiệu CLB Kết Nối (câu lạc bộ tình nguyện thuộc Học viện Nông nghiệp Việt Nam).

**Prompt đã dùng:**
- "Hãy giúp tôi lên ý tưởng và cấu trúc một trang web giới thiệu CLB tình nguyện, gồm những phần nào?"
- "Viết nội dung giới thiệu cho CLB với các giá trị cốt lõi: tâm huyết, đoàn kết, trách nhiệm."

**Kết quả AI đề xuất:**
- Cấu trúc trang gồm: Hero, Giới thiệu, Hoạt động, Lịch sinh hoạt, Cơ cấu tổ chức, Tuyển thành viên, Liên hệ, Footer.
- Đoạn nội dung giới thiệu CLB và 3 giá trị cốt lõi.

**Điều chỉnh của tôi:** Chọn lọc nội dung phù hợp với CLB thật, thay tên các hoạt động đúng thực tế (thu gom phế liệu, thu gom quần áo cũ, bán hoa gây quỹ).

---

## 📅 Buổi 2 — Viết HTML

**Mục tiêu:** Tạo file `index.html` với HTML ngữ nghĩa, dễ đọc, có chú thích.

**Prompt đã dùng:**
- "Viết code HTML cho trang web CLB Kết Nối theo cấu trúc trên, mỗi phần có comment giải thích bằng tiếng Việt."
- "Thêm form đăng ký thành viên với các trường: họ tên, lớp, khóa học, mã sinh viên, số điện thoại."

**Kết quả AI đề xuất:**
- Khung HTML hoàn chỉnh dùng các thẻ ngữ nghĩa: `header`, `nav`, `main`, `section`, `article`, `table`, `footer`.
- Bảng lịch sinh hoạt với `caption`, `thead`, `tbody`, `scope="col"`.
- Sơ đồ cơ cấu tổ chức chia 4 cấp: Chủ nhiệm → Phó chủ nhiệm/Ủy viên → 3 ban chức năng → Thành viên.
- Form đăng ký với `required` và `pattern` cho số điện thoại.

**Điều chỉnh của tôi:**
- Sửa tên đúng các chức danh (Chủ nhiệm, Phó chủ nhiệm) và tên thành viên thật.
- Thêm link "Bỏ qua điều hướng" (skip link) để hỗ trợ người dùng bàn phím.
- Kiểm tra lại từng anchor `#id` khớp với menu điều hướng.

---

## 📅 Buổi 3 — Viết CSS

**Mục tiêu:** Giao diện đẹp, responsive, nhất quán.

**Prompt đã dùng:**
- "Viết file CSS cho trang trên, dùng biến màu CSS, giao diện responsive, hiển thị tốt trên điện thoại."
- "Làm nổi bật các thẻ hoạt động (card) và sơ đồ cơ cấu tổ chức."

**Kết quả AI đề xuất:**
- Dùng CSS variables cho màu sắc, bố cục flexbox/grid.
- Class `.table-wrap` để bảng cuộn ngang trên điện thoại.
- Style cho form, nút bấm, thẻ card, sơ đồ tổ chức.

**Điều chỉnh của tôi:** Tinh chỉnh màu sắc theo màu chủ đạo của CLB, kiểm tra trên nhiều kích thước màn hình.

---

## 📅 Buổi 4 — JavaScript xử lý form

**Mục tiêu:** Xử lý form đăng ký khi bấm nút Gửi.

**Prompt đã dùng:**
- "Viết JavaScript kiểm tra số điện thoại 10-11 chữ số, khi gửi thành công thì ẩn form và hiện thông báo cảm ơn."

**Kết quả AI đề xuất:**
- Hàm `guiDangKy(event)` với `event.preventDefault()`.
- Regex `/^[0-9]{10,11}$/` kiểm tra số điện thoại, `alert()` khi không hợp lệ.
- Ẩn form, hiện thông báo thành công `#thongBao`.

**Điều chỉnh của tôi:** Đặt script ở cuối `<body>` để không làm chậm tải trang; thêm `console.log` để kiểm tra dữ liệu.

---

## 📅 Buổi 5 — Kiểm tra và hoàn thiện

**Prompt đã dùng:**
- "Hãy kiểm tra lại trang web: lỗi chính tả, link điều hướng, hiển thị trên điện thoại, tính hợp lệ của form."

**Kết quả AI đề xuất:**
- Danh sách các điểm cần kiểm tra: link anchor, alt của ảnh, `required` của form, responsive.

**Điều chỉnh của tôi:** Tự mở trang bằng trình duyệt kiểm tra từng phần, sửa lỗi chính tả (kiếm → kiểm, điều → điều hướng...).

---

## 🎯 Bài học rút ra khi dùng AI

1. **AI giúp nhanh nhưng không thay thế sự hiểu biết** — cần đọc hiểu từng dòng code AI sinh ra trước khi dùng.
2. **Luôn phải kiểm tra lại** — AI có thể sai chính tả tiếng Việt, sai tên chức danh, hoặc dùng anchor không khớp; cần tự kiểm tra trên trình duyệt.
3. **Chia nhỏ công việc theo buổi** — mỗi buổi một phần (HTML → CSS → JS → kiểm tra) dễ quản lý và dễ sửa lỗi hơn.
