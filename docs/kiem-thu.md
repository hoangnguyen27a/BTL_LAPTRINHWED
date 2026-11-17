# Tài liệu Kiểm thử — Website CLB Kết Nối
> **Môn:** Lập trình Web và triển khai phần mềm, Khóa 20  
> **Người thực hiện:** Nguyễn Huy Hoàng  
> **Nguyên tắc kiểm thử (Slide 6):** *"Thử thật, ghi thật — Chưa thử thì ghi 'Chưa kiểm tra'"*

---

## 1. Môi trường kiểm thử
- **Thiết bị:** Máy tính Windows 11.
- **Trình duyệt:** Google Chrome, Microsoft Edge.
- **Công cụ giả lập di động:** Chrome DevTools (Responsive Mode: iPhone 12/14, Samsung Galaxy S20).
- **Công cụ kiểm tra chuẩn:** W3C HTML Validator.

---

## 2. Bảng ca kiểm thử chi tiết ("Thử thật, ghi thật")

| Mã TC | Chức năng kiểm thử | Thao tác thử nghiệm | Kết quả mong đợi | Kết quả thực tế | Trạng thái | Minh chứng | Ghi chú & Sửa lỗi |
|:---:|:---|:---|:---|:---|:---:|:---|:---|
| **TC-01** | **Chuẩn W3C HTML5** | Nạp toàn bộ code `index.html` vào [validator.w3.org](https://validator.w3.org/) | Không có lỗi cú pháp HTML nghiêm trọng. | Không có lỗi cú pháp, cấu trúc ngữ nghĩa chuẩn. | **ĐẠT** | `evidence/03_kiem_thu/tc07_w3c_validator.png` | Đã bổ sung thuộc tính `alt` đầy đủ cho ảnh. |
| **TC-02** | **Hiển thị Logo** | Tải lại trang web và kiểm tra logo tại Header và Hero banner. | Ảnh logo hiển thị sắc nét, không bị vỡ link ảnh. | Logo hiển thị chuẩn nét trên cả Header (48px) và Banner (220px). | **ĐẠT** | `evidence/03_kiem_thu/tc01_desktop_view.jpg` | **Sửa lỗi:** Tên file cũ có dấu backtick `KẾ`T` làm hỏng link -> Đã đổi về `assets/img/logo.png`. |
| **TC-03** | **Menu điều hướng** | Nhấp chuột vào lần lượt 6 mục menu: Giới thiệu, Hoạt động, Lịch, Cơ cấu, Tuyển thành viên, Liên hệ. | Cuộn mượt mà (`smooth scroll`) đến đúng mục tương ứng; không bị Header che mất tiêu đề. | Cuộn chính xác; thuộc tính `scroll-padding-top: 76px` giúp tiêu đề không bị che lấp. | **ĐẠT** | `evidence/03_kiem_thu/tc01_desktop_view.jpg` | Đã kiểm tra hoạt động tốt. |
| **TC-04** | **Phím tắt Skip link** | Vừa tải trang, nhấn phím `Tab` trên bàn phím. | Hiện nút "Bỏ qua điều hướng", nhấn `Enter` nhảy thẳng vào nội dung chính `#noi-dung`. | Nút xuất hiện viền rõ nét; nhảy đúng vào `#noi-dung`. | **ĐẠT** | `evidence/03_kiem_thu/tc01_desktop_view.jpg` | Hỗ trợ tốt accessibility. |
| **TC-05** | **Giao diện di động** | Mở F12 DevTools, chuyển sang kích thước màn hình 375px (iPhone). | Giao diện tự động co về 1 cột dọc, không bị tràn thanh cuộn ngang toàn trang. | Bố cục dọc ngay ngắn, chữ và nút bấm to rõ ràng. | **ĐẠT** | `evidence/03_kiem_thu/tc02_mobile_view.jpg` | CSS Media Query hoạt động tốt. |
| **TC-06** | **Cuộn bảng lịch** | Trên màn hình 375px, dùng ngón tay/chuột vuốt ngang bảng Lịch sinh hoạt. | Bảng cuộn ngang trơn tru bên trong `.table-wrap`, trang web không bị xô lệch. | Bảng cuộn ngang độc lập, chữ không bị co dúm. | **ĐẠT** | `evidence/03_kiem_thu/tc03_mobile_bang_lich.jpg` | Đã kiểm tra hoạt động tốt. |
| **TC-07** | **Validate: Bỏ trống** | Bỏ trống ô Họ tên hoặc Mã SV rồi bấm nút "Gửi đăng ký". | Trình duyệt chặn lại và báo lỗi yêu cầu điền trường bắt buộc. | Trình duyệt chỉ vào ô trống và yêu cầu nhập dữ liệu. Form không gửi. | **ĐẠT** | `evidence/03_kiem_thu/tc04_form_de_trong.jpg` | Thuộc tính `required` hoạt động chuẩn. |
| **TC-08** | **Validate: Sai SĐT** | Nhập số điện thoại là chữ `abcde` hoặc chỉ có 6 chữ số rồi bấm Gửi. | Bật cảnh báo yêu cầu nhập đúng 10-11 chữ số, form không gửi. | Popup alert hiện: *"Số điện thoại không hợp lệ. Vui lòng nhập 10-11 chữ số."*. | **ĐẠT** | `evidence/03_kiem_thu/tc05_form_sai_sdt.jpg` | Regex `/^[0-9]{10,11}$/` bắt lỗi chính xác. |
| **TC-09** | **Gửi form hợp lệ** | Nhập đầy đủ 5 trường hợp lệ, SĐT đúng 10 số rồi bấm Gửi. | Form ẩn đi, hiện thông báo thành công; in dữ liệu ra F12 Console. | Form ẩn ngay lập tức; thông báo thành công hiện rõ ràng; console log đầy đủ thông tin. | **ĐẠT** | `evidence/03_kiem_thu/tc06_form_thanh_cong.jpg` | Hoàn thành xuất sắc. |
| **TC-10** | **Trình duyệt Safari** | Thử nghiệm trên thiết bị iPhone thực tế chạy trình duyệt Safari. | Giao diện và form hoạt động tương đương trên Chrome máy tính. | *Chưa có máy iPhone vật lý để đối soát trực tiếp lúc này.* | **Chưa kiểm tra** | N/A | Sẽ kiểm tra thêm khi có thiết bị. |

---

## 3. Kết luận
- Toàn bộ các chức năng cốt lõi đã được kiểm thử thực tế và đạt tiêu chí chấp nhận (Acceptance Criteria).
- Ca kiểm thử chưa có điều kiện thử nghiệm được ghi nhận minh bạch là **"Chưa kiểm tra"** theo đúng tinh thần Slide 6.
