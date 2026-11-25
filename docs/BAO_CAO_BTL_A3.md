Tên đề tài: Website tĩnh giới thiệu CLB Kết Nối (Học viện Nông nghiệp Việt Nam)
Sinh viên: Nguyễn Huy Hoàng      Mã SV: 2071020079      Lớp/Ngành: Lớp 20-02 / CNTT
GVGD: ThS Lê Thái Bảo
Repository: https://github.com/hoangnguyen27a/BTL_LAPTRINHWED.git       Website: https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/
Phiên bản/commit được báo cáo: tag: v8 (https://github.com/hoangnguyen27a/BTL_LAPTRINHWED/tree/v8)
Học kỳ/năm học: Học kỳ 1, Năm học 2026 – 2027

---

### Lời cam đoan và khai báo
Tôi xin cam đoan toàn bộ cấu trúc mã nguồn HTML5, bảng định dạng CSS3, mã xử lý form JavaScript, kịch bản kiểm thử và các bản tài liệu kỹ thuật trong bài tập lớn này đều do chính bản thân tôi trực tiếp thực hiện và kiểm chứng.
- **Nguồn nội dung và hình ảnh ngoài:** Biểu trưng Logo CLB Kết Nối và nội dung hoạt động do Ban Điều Hành CLB Kết Nối – Học viện Nông nghiệp Việt Nam cung cấp và cấp phép sử dụng cho mục đích học tập; font chữ sử dụng hệ thống sans-serif có sẵn (`system-ui, -apple-system, Segoe UI, Roboto...`), không sử dụng thư viện/framework bên ngoài.
- **Khai báo công cụ AI:** Tôi có sử dụng công cụ AI (Gemini) nhằm hỗ trợ lên ý tưởng khung sườn ban đầu, gợi ý biểu thức Regex kiểm tra số điện thoại và rà soát lỗi chính tả. Toàn bộ mã nguồn do AI gợi ý đều được tôi đọc hiểu, trực tiếp điều chỉnh theo thực tế và kiểm tra lại trên trình duyệt; quá trình này được ghi chép minh bạch tại tệp tin `AI_LOG.md`.
- **Xác nhận phép thử:** Tôi xác nhận toàn bộ các ca kiểm thử và 19 ảnh chụp minh chứng trong báo cáo này là kết quả thử nghiệm thực tế 100% trên thiết bị cá nhân của tôi.

### Tóm tắt
Website CLB Kết Nối là một trang web tĩnh dạng đơn trang (Single-Page Landing Page) được xây dựng thuần túy bằng HTML5, CSS3 và Vanilla JavaScript nhằm giới thiệu câu lạc bộ tình nguyện trực thuộc Học viện Nông nghiệp Việt Nam. Người xem chính gồm sinh viên tại trường (tìm hiểu và đăng ký gia nhập CLB) cùng các mạnh thường quân (quan tâm theo dõi và tài trợ hoạt động thiện nguyện). Website được thiết kế tương thích đa thiết bị (Responsive trên Desktop 960px+, Tablet 640px+ và Mobile 375px - 520px) với các khối: Header dính cố định, Hero banner, Giới thiệu 3 giá trị cốt lõi, 3 thẻ hoạt động, Bảng lịch sinh hoạt có khung cuộn ngang chống tràn, Sơ đồ tổ chức 4 cấp, Form đăng ký thành viên có kiểm tra hợp lệ dữ liệu và Khối liên hệ. Sản phẩm được kiểm thử đạt chuẩn W3C HTML5 không có lỗi, kiểm thử tương tác form và khả năng tiếp cận (Skip link). Website đã được triển khai công khai tại URL: https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/ khớp với mã nguồn phiên bản gắn mốc tag `v8`. Giới hạn hiện tại: Dữ liệu form mới được kiểm tra và phản hồi phía client, chưa lưu trữ vào cơ sở dữ liệu backend.

### Mục lục
1. [Chủ đề, yêu cầu và tiêu chí thiết kế](#1-chủ-đề-yêu-cầu-và-tiêu-chí-thiết-kế)
2. [Thiết kế giao diện và cấu trúc mã nguồn](#2-thiết-kế-giao-diện-và-cấu-trúc-mã-nguồn)
3. [Phát triển và triển khai](#3-phát-triển-và-triển-khai)
4. [Đánh giá, kiểm thử và hiệu chỉnh](#4-đánh-giá-kiểm-thử-và-hiệu-chỉnh)
5. [Tài liệu bàn giao](#5-tài-liệu-bàn-giao)
6. [Demo và phản biện](#6-demo-và-phản-biện)
7. [Quy cách, nguồn và trách nhiệm](#7-quy-cách-nguồn-và-trách-nhiệm)
- [Phụ lục: Danh mục minh chứng](#phụ-lục-danh-mục-minh-chứng)
- [Bảng đối chiếu rubric A3](#bảng-đối-chiếu-rubric-a3)
- [Tài liệu tham khảo](#tài-liệu-tham-khảo)

---

### Bảng đối chiếu rubric A3

| Mã | Tiêu chí | CLO | Tỷ trọng |
|:---|:---|:---:|:---:|
| **A3.TC1a** | Yêu cầu và tiêu chí thiết kế | CLO1 | 10% |
| **A3.TC1b** | Đánh giá phương án giao diện | CLO2 | 5% |
| **A3.TC2a** | Thiết kế giao diện responsive | CLO1 | 10% |
| **A3.TC2b** | Thiết kế thành phần và tổ chức mã nguồn | CLO3 | 10% |
| **A3.TC3a** | Phát triển website HTML5/CSS3 | CLO4 | 15% |
| **A3.TC3b** | Triển khai và xác minh phiên bản | CLO6 | 10% |
| **A3.TC4a** | Đánh giá giao diện và hiệu chỉnh | CLO2 | 10% |
| **A3.TC4b** | Kiểm thử và minh chứng sửa lỗi | CLO4 | 10% |
| **A3.TC5** | Báo cáo kỹ thuật và tài liệu bàn giao | CLO5 | 10% |
| **A3.TC6a** | Phản biện quyết định giao diện | CLO2 | 2% |
| **A3.TC6b** | Demo và xử lý tình huống triển khai | CLO6 | 3% |
| **A3.TC7** | Quy cách, khai báo nguồn và trách nhiệm bàn giao | Không gán | 5% |

*Tổng trọng số các tiêu chí trong A3: 100%. A3 chiếm 60% điểm học phần. TC7 chỉ tính điểm bài; không tính CLO/PI.*

---

### 1. Chủ đề, yêu cầu và tiêu chí thiết kế
- **Tên chủ đề và lý do chọn:** Website CLB Kết Nối VNUA, lý do tôi chọn là muốn tạo ra một website để mọi người có thể biết đến CLB và lan tỏa tình yêu thương, tinh thần thanh niên tình nguyện vì cộng đồng sinh viên và xã hội.
- **Người xem chính:** Các sinh viên tại trường Học viện Nông nghiệp Việt Nam (đặc biệt là tân sinh viên) và các mạnh thường quân, nhà hảo tâm, cựu thành viên quan tâm đến hoạt động của CLB.
- **Mục tiêu quan sát được:** Mọi người có thể quan sát được những nội dung trực quan như: thông tin giới thiệu CLB, 3 giá trị cốt lõi, các hoạt động thiện nguyện nổi bật, lịch sinh hoạt hàng tuần, sơ đồ phân cấp cơ cấu tổ chức và form đăng ký trực tiếp tại website.
- **Phạm vi và ràng buộc:** Xây dựng và thiết kế front-end thuần túy từ HTML5 và CSS3 (kết hợp JavaScript thuần xử lý form phía client); không sử dụng framework hay thư viện ngoài; hỗ trợ đa thiết bị và đạt chuẩn truy cập cơ bản.

#### Bảng đặc tả yêu cầu người dùng:

| Mã yêu cầu | Người xem cần làm gì? | Tiêu chí chấp nhận | Minh chứng |
|:---:|:---|:---|:---|
| **R1** | Tất cả các sinh viên trường VNUA | Truy cập trang chủ xem phần giới thiệu CLB, 3 giá trị cốt lõi và bấm nút chuyển nhanh đến Form đơn đăng ký tham gia CLB. | `evidence/03_kiem_thu/tc01_desktop_view.jpg` |
| **R2** | Những người quan tâm đến CLB / Mạnh thường quân | Xem được các hoạt động thiện nguyện (Thu gom phế liệu, Thu gom quần áo, Bán hoa gây quỹ) dạng Card trực quan và thông tin liên hệ. | `evidence/03_kiem_thu/tc01_desktop_view.jpg` |
| **R3** | Thành viên và sinh viên | Tra cứu lịch họp và hoạt động cố định trong tuần qua bảng biểu (`<table>`), hỗ trợ cuộn ngang trên điện thoại mà không vỡ layout. | `evidence/03_kiem_thu/tc03_mobile_bang_lich.jpg` |
| **R4** | Sinh viên và đối tác | Xem sơ đồ bộ máy tổ chức của CLB từ Ban Chủ nhiệm đến các ban chuyên môn và khối thành viên. | `evidence/03_kiem_thu/tc03_mobile_bang_lich.jpg` |
| **R5** | Tân sinh viên muốn gia nhập CLB | Điền đầy đủ 5 trường thông tin vào Form, kiểm tra đúng định dạng số điện thoại 10-11 số, gửi thành công và thấy thông báo xác nhận. | `evidence/03_kiem_thu/tc04_form_de_trong.jpg`<br>`evidence/03_kiem_thu/tc05_form_sai_sdt.jpg`<br>`evidence/03_kiem_thu/tc06_form_thanh_cong.jpg` |
| **R6** | Mọi người dùng truy cập web | Nhấn vào thanh menu điều hướng để cuộn trang mượt mà (`smooth scroll`), hoặc dùng phím `Tab` để bỏ qua menu (`skip link`). | `evidence/03_kiem_thu/tc01_desktop_view.jpg` |

#### Đánh giá phương án giao diện (TC1b):
- **Tiêu chí so sánh:** Trải nghiệm cuộn trang di động (UX), tính liền mạch của luồng thông tin, tốc độ nạp trang và mức độ phức tạp khi bảo trì.
- **Phương án đã cân nhắc:**
  1. *Phương án A (Website nhiều trang - Multi-page):* Tách thành các file `index.html`, `gioithieu.html`, `dangky.html`...
  2. *Phương án B (Website trang đơn - Single-Page Landing Page):* Tập trung toàn bộ thông tin trên một trang có Header sticky và điều hướng Anchor Link.
- **Lý do chọn Phương án B:** Nội dung giới thiệu câu lạc bộ có tính cô đọng, mô hình Single-Page giúp sinh viên theo dõi thông tin từ giới thiệu -> hoạt động -> lịch họp -> đăng ký chỉ bằng một lần cuộn chuột/vuốt màn hình, không bị giật lag hay mất thời gian tải trang lại.
- **Phần đã hiệu chỉnh:** Bổ sung `scroll-padding-top: 76px` trên desktop (và `120px` trên mobile `max-width: 520px`) để khi cuộn trang bằng link menu, tiêu đề không bị Header cố định che mất; bổ sung nút Skip Link hỗ trợ người dùng bàn phím.
- **Đính kèm minh chứng:** `evidence/01_yeu_cau/01_tra_loi_4_cau_hoi.jpg`, `evidence/02_thiet_ke/02_thiet_ke_thanh_phan.jpg`.

---

### 2. Thiết kế giao diện và cấu trúc mã nguồn

#### Wireframe màn hình rộng và hẹp (TC2a):
- **Màn hình rộng (Desktop >= 960px):**
  - Thanh Header dính cố định dàn ngang: Logo bên trái, menu 6 liên kết bên phải (đáp ứng R6).
  - Khối Hero chia 2 cột: Logo lớn 220px bên trái, Tiêu đề + Giới thiệu + 2 nút Call-to-Action bên phải theo đường dẫn thị giác chữ Z (đáp ứng R1).
  - Khối Hoạt động: Lưới CSS Grid 3 cột (`repeat(3, 1fr)`) tương ứng 3 chương trình trọng tâm (đáp ứng R2).
  - Khối Cơ cấu tổ chức: Sơ đồ 4 cấp phân nhánh đối xứng cân đối (đáp ứng R4).
- **Màn hình hẹp (Mobile <= 520px):**
  - Header thu gọn, căn giữa cả Logo và Menu để tối ưu diện tích chạm ngón tay.
  - Khối Hero chuyển thành 1 cột dọc trung tâm (Logo ở trên, tiêu đề và nút xếp chồng).
  - Khối Hoạt động: Các thẻ Card tự động xếp chồng 1 cột (`1fr`).
  - Bảng Lịch sinh hoạt: Được đặt trong lớp bọc `.table-wrap` có `overflow-x: auto`, cho phép vuốt ngang độc lập trên điện thoại mà không làm tràn toàn trang (đáp ứng R3).
- **Minh chứng:** `evidence/02_thiet_ke/03_responsive_breakpoints.jpg`, `evidence/02_thiet_ke/04_code_css_responsive_tablet.jpg`, `evidence/02_thiet_ke/05_code_css_responsive_desktop.jpg`.

#### Thành phần/trang, thư mục và tài nguyên (TC2b):
- **Tổ chức thư mục:**
  - Thư mục gốc: Chứa `index.html` (mã nguồn trang duy nhất), `style.css` (toàn bộ định dạng CSS), `README.md` (hướng dẫn dự án), `AI_LOG.md` (nhật ký AI).
  - Thư mục `assets/img/`: Chứa tệp hình ảnh nhận diện chuẩn `logo.png`.
  - Thư mục `docs/`: Chứa các tài liệu kỹ thuật chi tiết (`yeu-cau.md`, `thiet-ke.md`, `kiem-thu.md`, `san-pham.md`, `BAO_CAO_BTL_A3.md`).
  - Thư mục `evidence/`: Phân chia 4 thư mục con chứa 19 ảnh chụp minh chứng thực tế (`01_yeu_cau/`, `02_thiet_ke/`, `03_kiem_thu/`, `04_trien_khai/`).
- **Minh chứng:** `evidence/04_trien_khai/01_cau_truc_du_an_vscode.jpg`.

#### Bảng quyết định thiết kế:

| Quyết định thiết kế | Yêu cầu liên quan | Lý do / Đánh đổi |
|:---|:---:|:---|
| **Sử dụng Header cố định (`position: sticky; top: 0`)** | R1, R6 | **Lý do:** Người dùng có thể nhảy đến bất kỳ phần nào trên trang ngay lập tức.<br>**Đánh đổi:** Chiếm mất khoảng 76px chiều cao màn hình (hơn 100px trên mobile khi menu xuống dòng); phải cấu hình thêm `scroll-padding-top` (76px desktop, 120px mobile) để tránh che tiêu đề. |
| **Bảng màu chủ đạo Xanh dương (`#3058a8`) và Vàng (`#f2c200`)** | R1, R2 | **Lý do:** Thể hiện màu sắc nhận diện chính thức của CLB Kết Nối (nhiệt huyết thanh niên và gắn kết yêu thương).<br>**Đánh đổi:** Phải chọn màu nền xen kẽ xám nhạt (`#f3f6fb`) để chữ không bị chói. |
| **Khung bao bọc bảng `.table-wrap` có `overflow-x: auto`** | R3 | **Lý do:** Giúp bảng lịch có thể cuộn ngang cảm ứng trên màn hình nhỏ mà không làm tràn khung ngang trang web.<br>**Đánh đổi:** Người dùng mobile phải vuốt ngang bảng để xem hết các cột. |
| **Kiểm tra form bằng Regex trực tiếp phía Client** | R5 | **Lý do:** Phản hồi ngay lập tức cho sinh viên khi nhập thiếu hoặc sai số điện thoại.<br>**Đánh đổi:** Chưa lưu được thông tin vào database (phù hợp với phạm vi web tĩnh HTML5/CSS3). |

---

### 3. Phát triển và triển khai

#### Triển khai HTML5/CSS3 (TC3a):
- **Mã nguồn HTML5 ngữ nghĩa:** Sử dụng đầy đủ các thẻ semantic `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<table>` (với `<caption>`, `<thead>`, `<tbody>`, `scope="col"`), `<dl>`, `<footer>`. Các liên kết nội bộ `#id` khớp 100% với danh mục điều hướng.
- **Kỹ thuật CSS3:**
  - Khai báo hệ biến màu CSS `:root` nhất quán (`--mau-xanh`, `--mau-xanh-dam`, `--mau-vang`, `--mau-nen-nhat`, `--mau-chu`, `--mau-vien`, `--bo-goc`).
  - Sử dụng kết hợp Flexbox (cho Header, Footer, Nút CTA) và CSS Grid (cho Hero, Cards, Sơ đồ tổ chức).
  - Định nghĩa Media Queries tại các điểm ngắt: `@media (min-width: 640px)` (Tablet hiển thị 2 cột), `@media (min-width: 960px)` (Desktop hiển thị 3 cột ngang đầy đủ) và `@media (max-width: 520px)` (Mobile co về 1 cột dọc thanh thoát, tăng `scroll-padding-top: 120px`).
- **Minh chứng:** `evidence/02_thiet_ke/01_he_thong_mau_va_font.jpg`, `evidence/02_thiet_ke/04_code_css_responsive_tablet.jpg`, `evidence/02_thiet_ke/05_code_css_responsive_desktop.jpg`.

#### Triển khai và phiên bản (TC3b):
- **URL công khai:** [https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/](https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/)
- **Repository:** [https://github.com/hoangnguyen27a/BTL_LAPTRINHWED.git](https://github.com/hoangnguyen27a/BTL_LAPTRINHWED.git)
- **Commit / Tag được báo cáo:** `tag: v8` (đồng bộ cùng nhánh `main` tại: [https://github.com/hoangnguyen27a/BTL_LAPTRINHWED/tree/v8](https://github.com/hoangnguyen27a/BTL_LAPTRINHWED/tree/v8)).
- **Cách kiểm tra URL khớp phiên bản:** Truy cập URL GitHub Pages trên trình duyệt, kiểm tra biểu tượng Favicon Logo CLB, thanh Header, các khối nội dung và chân trang Footer có hiển thị đúng dòng bản quyền: *"© 2026 CLB Kết Nối – Học viện Nông nghiệp Việt Nam. Quản trị web: Nguyễn Huy Hoàng"* khớp 100% với commit tag `v8` trên GitHub.
- **Minh chứng:** `evidence/04_trien_khai/02_git_tags_log.jpg`, `evidence/04_trien_khai/03_github_repository.jpg`, `evidence/04_trien_khai/04_github_pages_setting.jpg`, `evidence/04_trien_khai/05_live_url_demo.jpg`.

---

### 4. Đánh giá, kiểm thử và hiệu chỉnh

#### Đánh giá giao diện (TC4a):
- **Tính nhất quán:** Tất cả các section đều dùng chung khoảng đệm padding 64px (48px trên mobile), các thẻ card và ô input đều bo góc thống nhất `--bo-goc: 14px`, màu sắc đồng bộ theo hệ thống biến `:root`.
- **Responsive:** Đã kiểm tra thực tế trên 3 chế độ: Màn hình lớn (Desktop 1920x1080), Tablet và Màn hình nhỏ (iPhone 14 - 390x844px qua DevTools). Bố cục chuyển đổi mượt mà, không xuất hiện thanh cuộn ngang ngoài ý muốn (Horizontal scrollbar).
- **Accessibility & Khả dụng:** Tích hợp liên kết ẩn `.skip` hỗ trợ người dùng chỉ dùng bàn phím; trạng thái focus có viền vàng nổi bật (`outline: 3px solid var(--mau-vang)`); tất cả các thẻ ảnh đều có thuộc tính `alt` mô tả rõ ràng.

#### Bảng ca kiểm thử chi tiết ("Thử thật, ghi thật"):

| Yêu cầu | Bước thử / Điều kiện | Kết quả mong đợi | Kết quả thực tế | Kết luận / Minh chứng |
|:---:|:---|:---|:---|:---:|
| **R1, R6** | Nạp toàn bộ code `index.html` vào công cụ W3C HTML Validator. | Báo cáo xanh lá, không có lỗi cú pháp hoặc thẻ mở không đóng. | "Document checking completed. No errors or warnings to show." | **ĐẠT**<br>`evidence/03_kiem_thu/tc07_w3c_validator.png` |
| **R1** | Mở trang web ở chế độ toàn màn hình trên máy tính (Desktop). | Logo Header, Hero banner hiển thị sắc nét; menu dàn ngang cân đối. | Giao diện hiển thị đúng chuẩn; hình ảnh rõ nét. | **ĐẠT**<br>`evidence/03_kiem_thu/tc01_desktop_view.jpg` |
| **R1, R2** | Mở F12 DevTools chọn kích thước iPhone 14 (390x844px). | Giao diện co về 1 cột dọc; không tràn thanh cuộn ngang trang. | Bố cục dọc gọn gàng; nút bấm to dễ thao tác bằng ngón tay. | **ĐẠT**<br>`evidence/03_kiem_thu/tc02_mobile_view.jpg` |
| **R3** | Trên màn hình di động, dùng chuột/ngón tay vuốt ngang bảng Lịch. | Bảng lịch cuộn ngang trơn tru bên trong khung `.table-wrap`. | Bảng cuộn độc lập mượt mà, layout chung không bị co dúm. | **ĐẠT**<br>`evidence/03_kiem_thu/tc03_mobile_bang_lich.jpg` |
| **R5** | Bỏ trống ô "Lớp" và bấm nút "Gửi đăng ký". | Trình duyệt kích hoạt cảnh báo bắt buộc nhập của HTML5. | Hiện popup: *"Please fill out this field."*. Form không cho gửi. | **ĐẠT**<br>`evidence/03_kiem_thu/tc04_form_de_trong.jpg` |
| **R5** | Nhập chữ cái `sfsdhgykuhk` vào ô Số điện thoại rồi bấm Gửi. | Hệ thống chặn lại do vi phạm định dạng số điện thoại. | Trình duyệt chặn bằng `pattern="[0-9]{10,11}"` HTML5, hiện cảnh báo: *"Please match the requested format."* (có lớp regex `/^[0-9]{10,11}$/` + `alert()` JS dự phòng). | **ĐẠT**<br>`evidence/03_kiem_thu/tc05_form_sai_sdt.jpg` |
| **R5** | Nhập đầy đủ 5 trường thông tin hợp lệ (SĐT 10 số) và bấm Gửi. | Form ẩn đi; xuất hiện khung thông báo cảm ơn màu xanh. | Form ẩn ngay; khung thông báo thành công hiển thị trang trọng. | **ĐẠT**<br>`evidence/03_kiem_thu/tc06_form_thanh_cong.jpg` |

#### Sửa lỗi và thử lại (TC4b):
- **Lỗi thực tế phát hiện:** Khi kiểm tra trang web trên GitHub Pages, ảnh biểu trưng Logo tại thanh Header bị mất (hiển thị icon ảnh vỡ).
- **Tệp và nguyên nhân:** Trong file `index.html` cũ, thẻ ảnh header có đường dẫn `assets/LOGO CLB KẾ`T NỐI (1).png` — bị dính ký tự backtick lạc trong từ `KẾ`T`, có dấu cách và tiếng Việt có dấu, khiến máy chủ web trả về lỗi `404 Not Found`.
- **Hành động sửa lỗi:** 
  1. Tạo thư mục chuẩn `assets/img/` và lưu file ảnh chuẩn `logo.png` không dấu.
  2. Sửa lại mã nguồn trong `index.html` thành `<img src="assets/img/logo.png" alt="Logo CLB Kết Nối" width="48" height="48">`.
- **Cùng phép thử chạy lại:** Làm mới trang web bằng tổ hợp `Ctrl + F5`, ảnh Logo lập tức hiển thị sắc nét trên cả Header (48px) và Banner (220px). Kết quả nghiệm thu: **ĐẠT**.
- **Minh chứng:** `evidence/03_kiem_thu/tc01_desktop_view.jpg`, `evidence/04_trien_khai/05_live_url_demo.jpg`.

---

### 5. Tài liệu bàn giao (TC5)
- **Tệp README:** [README.md](https://github.com/hoangnguyen27a/BTL_LAPTRINHWED/blob/main/README.md) — Giới thiệu tổng quan, cây thư mục dự án, mô tả các khối nội dung, công nghệ và hướng dẫn chạy.
- **Tệp AI_LOG:** [AI_LOG.md](https://github.com/hoangnguyen27a/BTL_LAPTRINHWED/blob/main/AI_LOG.md) — Ghi nhận trung thực 5 buổi làm việc với AI từ ý tưởng, viết HTML, CSS, JavaScript đến kiểm thử.
- **Tệp Release Note / Tài liệu kỹ thuật:** Lưu tại thư mục [docs/](https://github.com/hoangnguyen27a/BTL_LAPTRINHWED/tree/main/docs) gồm 5 tệp markdown chi tiết (`yeu-cau.md`, `thiet-ke.md`, `kiem-thu.md`, `san-pham.md`, `BAO_CAO_BTL_A3.md`).
- **Hướng dẫn mở / chạy sản phẩm:**
  - *Cách 1:* Mở trực tiếp tệp `index.html` bằng trình duyệt Google Chrome hoặc Microsoft Edge (`start index.html`).
  - *Cách 2:* Chạy qua máy chủ tĩnh Python (`python -m http.server 8000`) và truy cập `http://localhost:8000`.
  - *Cách 3:* Xem trực tiếp trực tuyến tại GitHub Pages: [https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/](https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/).
- **Giới hạn đã biết:** Trang web là ứng dụng tĩnh front-end; form đăng ký thành viên mới xử lý logic và validate phía client (chưa kết nối cơ sở dữ liệu server để lưu trữ lâu dài); liên kết Fanpage hiện dùng `#` chờ cập nhật URL chính thức.
- **Sự thống nhất:** Mã nguồn tại local, kho lưu trữ Git và phiên bản hiển thị trên URL GitHub Pages hoàn toàn khớp nhau tại mốc **tag: v8**.

---

### 6. Demo và phản biện

#### Kịch bản Demo:
1. **Trình tự mở URL:** Mở trình duyệt truy cập đường link GitHub Pages chính thức [https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/](https://hoangnguyen27a.github.io/BTL_LAPTRINHWED/).
2. **Luồng chính:** Bấm lần lượt các mục trên thanh Menu (*Giới thiệu -> Hoạt động -> Lịch -> Cơ cấu -> Tuyển thành viên -> Liên hệ*) để trình diễn hiệu ứng cuộn mượt mà (`smooth scroll`).
3. **Responsive:** Bấm phím `F12` chuyển đổi kích thước sang màn hình di động (iPhone 14 - 390px); cuộn qua các phần để chứng minh các Card xếp chồng 1 cột và thực hiện thao tác vuốt ngang bảng lịch sinh hoạt bên trong khung `.table-wrap`.
4. **Tương tác Form:** Thao tác thử form (bỏ trống ô bắt buộc ➔ hiện cảnh báo; nhập chữ vào SĐT ➔ hiện tooltip *"Please match the requested format."* từ `pattern` HTML5 và có kiểm tra dự phòng bằng JS; nhập hợp lệ 10 số ➔ ẩn form và hiện thông báo cảm ơn chúc mừng).
5. **Phiên bản:** Cuộn xuống chân trang Footer đối chiếu dòng chữ quản trị web và phiên bản **tag: v8** trên GitHub.

#### Quyết định giao diện cần giải thích (TC6a):
- *Tại sao sử dụng màu xanh dương và màu vàng làm màu chủ đạo?*  
  -> Trả lời: Màu xanh dương tượng trưng cho tuổi trẻ, sức sống và khát vọng tình nguyện; màu vàng mang năng lượng ấm áp của sự kết nối và sẻ chia yêu thương, hoàn toàn khớp với slogan thương hiệu của CLB Kết Nối (*"We love and we do"*).
- *Tại sao bảng biểu trên mobile lại dùng thanh cuộn ngang thay vì co chữ nhỏ lại?*  
  -> Trả lời: Nếu ép kích thước bảng để vừa chiều rộng 375px của điện thoại, cỡ chữ sẽ bị co nhỏ dưới 10px gây khó đọc, vi phạm chuẩn công thái học. Việc dùng `.table-wrap` có `overflow-x: auto` giúp giữ nguyên kích thước font chữ dễ đọc và cho phép cuộn ngang độc lập mà không phá vỡ khung giao diện chung.

#### Cách xác minh hoặc xử lý lỗi triển khai trong phạm vi bài (TC6b):
- *Xử lý lỗi cache trình duyệt (nội dung mới không hiển thị):* Hướng dẫn người dùng nhấn tổ hợp phím `Ctrl + F5` (Hard Reload) hoặc mở bằng tab ẩn danh (`Ctrl + Shift + N`) để ép trình duyệt xóa bộ nhớ đệm và nạp tài nguyên mới từ máy chủ.
- *Xử lý lỗi đường dẫn ảnh 404 trên máy chủ Linux/GitHub Pages:* Tuyệt đối không dùng tên file có dấu tiếng Việt, dấu cách hay ký tự đặc biệt; luôn dùng đường dẫn tương đối và chữ thường không dấu (ví dụ: `assets/img/logo.png`).

---

### 7. Quy cách, nguồn và trách nhiệm
- **Nguồn nội dung và hình ảnh:** Hình ảnh Logo CLB Kết Nối thuộc bản quyền của CLB Kết Nối – Học viện Nông nghiệp Việt Nam, được cấp phép dùng cho bài tập lớn này; các đoạn văn bản giới thiệu do tác giả tự biên soạn dựa trên thông tin thực tế của CLB.
- **Mã nguồn ngoài:** Toàn bộ 100% mã nguồn HTML5, CSS3 và Vanilla JS do sinh viên tự viết, không sử dụng framework, template hoặc thư viện bên thứ ba.
- **Khai báo AI:** Sinh viên sử dụng AI (Gemini) một cách có kiểm soát và minh bạch để hỗ trợ cấu trúc và kiểm tra cú pháp; đã ghi nhận chi tiết tại tệp `AI_LOG.md`.
- **Phần việc cá nhân & Xác nhận hồ sơ nộp:** Sinh viên Nguyễn Huy Hoàng cam đoan tự hoàn thiện bài tập và nộp đầy đủ hồ sơ mã nguồn, báo cáo kỹ thuật và đường dẫn URL công khai lên hệ thống LMS theo đúng quy chế đào tạo của Trường Đại học Đại Nam.

---

### Phụ lục: Danh mục minh chứng

| Mã rubric | Minh chứng | Vị trí / URL | Phiên bản |
|:---:|:---|:---|:---:|
| **A3.TC1a** | Ảnh chụp trả lời 4 câu hỏi cốt lõi, phạm vi và tiêu chí chấp nhận | `evidence/01_yeu_cau/01_tra_loi_4_cau_hoi.jpg` | Tag `v8` |
| **A3.TC1b** | Ảnh chụp phân tích và quyết định phương án giao diện Single-page | `evidence/01_yeu_cau/01_tra_loi_4_cau_hoi.jpg`<br>`evidence/02_thiet_ke/02_thiet_ke_thanh_phan.jpg` | Tag `v8` |
| **A3.TC2a** | Ảnh chụp bản vẽ Wireframe, kích thước Breakpoints (640px, 960px, 520px) | `evidence/02_thiet_ke/03_responsive_breakpoints.jpg` | Tag `v8` |
| **A3.TC2b** | Ảnh chụp cây thư mục mã nguồn và tổ chức tài nguyên trên VS Code | `evidence/04_trien_khai/01_cau_truc_du_an_vscode.jpg` | Tag `v8` |
| **A3.TC3a** | Ảnh chụp mã CSS Media Queries responsive cho Tablet và Desktop | `evidence/02_thiet_ke/04_code_css_responsive_tablet.jpg`<br>`evidence/02_thiet_ke/05_code_css_responsive_desktop.jpg` | Tag `v8` |
| **A3.TC3b** | Ảnh chụp cài đặt GitHub Pages và giao diện website chạy trên URL thật | `evidence/04_trien_khai/04_github_pages_setting.jpg`<br>`evidence/04_trien_khai/05_live_url_demo.jpg` | Tag `v8` |
| **A3.TC4a** | Ảnh chụp giao diện thực tế trên Desktop và màn hình di động iPhone 14 | `evidence/03_kiem_thu/tc01_desktop_view.jpg`<br>`evidence/03_kiem_thu/tc02_mobile_view.jpg` | Tag `v8` |
| **A3.TC4b** | Ảnh chụp kiểm thử Form (bỏ trống, sai SĐT, thành công) và chuẩn W3C | `evidence/03_kiem_thu/tc04_form_de_trong.jpg`<br>`evidence/03_kiem_thu/tc05_form_sai_sdt.jpg`<br>`evidence/03_kiem_thu/tc06_form_thanh_cong.jpg`<br>`evidence/03_kiem_thu/tc07_w3c_validator.png` | Tag `v8` |
| **A3.TC5** | Tệp README, AI_LOG và 4 tài liệu kỹ thuật trong thư mục docs | `README.md`, `AI_LOG.md`, `docs/san-pham.md`, `docs/kiem-thu.md` | Tag `v8` |
| **A3.TC6a** | Luận điểm giải thích quyết định thiết kế màu sắc và cuộn bảng lịch | Mục 6.2 Báo cáo này và file `docs/thiet-ke.md` | Tag `v8` |
| **A3.TC6b** | Ảnh chụp lịch sử Git log có các mốc tag và kịch bản xử lý sự cố web | `evidence/04_trien_khai/02_git_tags_log.jpg` | Tag `v8` |
| **A3.TC7** | Khai báo quyền sở hữu, nguồn tài nguyên, cam đoan và tệp AI_LOG | Mục Lời cam đoan, Mục 7 Báo cáo này và `AI_LOG.md` | Tag `v8` |

---

### Tài liệu tham khảo
1. W3C HTML5 Specification — [https://www.w3.org/TR/html52/](https://www.w3.org/TR/html52/) (Truy cập tháng 11/2026).
2. W3C Markup Validation Service — [https://validator.w3.org/](https://validator.w3.org/) (Truy cập tháng 11/2026).
3. MDN Web Docs: Responsive Web Design Basics — Mozilla Developer Network.
4. Đề cương chi tiết học phần Lập trình Web và Triển khai phần mềm — Khoa Công nghệ Thông tin, Trường Đại học Đại Nam.
