| Chức năng | Tiền điều kiện | Mô tả | Dữ liệu Test | Kết quả mong muốn |
| --- | --- | --- | --- | --- |
| **Đăng ký / Đăng nhập (UC01)** | Người dùng có tài khoản hợp lệ trên hệ thống.

 | Kiểm tra đăng nhập thành công với tài khoản hợp lệ (AC01).

 | Tên đăng nhập: khachhang123<br>

<br>Mật khẩu: Password@123 | Đăng nhập thành công, chuyển hướng đến màn hình chính của người dùng.

 |
| **Đăng ký / Đăng nhập (UC01)** | Người dùng ở màn hình đăng nhập.

 | Kiểm tra đăng nhập với thông tin sai (AC01).

 | Tên đăng nhập: khachhang123<br>

<br>Mật khẩu: SaiMatKhau | Hệ thống từ chối đăng nhập và hiển thị thông báo lỗi yêu cầu nhập lại.

 |
| **Đặt chuyến (UC02)** | Khách hàng đăng nhập thành công.

 | Kiểm tra đặt chuyến khi để trống điểm đón hoặc điểm đến (TC01).

 | Điểm đón: [Trống]<br>

<br>Điểm đến: "123 Lê Lợi, Q1" | Yêu cầu đặt chuyến không thành công, hệ thống thông báo lỗi thiếu thông tin hợp lệ.

 |
| **Đặt chuyến (UC02)** | Khách hàng đăng nhập thành công.

 | Kiểm tra đặt chuyến thành công với đầy đủ thông tin hợp lệ (TC01, TC02, TC03, TC04).

 | Điểm đón: "Chợ Bến Thành"<br>

<br>Điểm đến: "Sân bay Tân Sơn Nhất"<br>

<br>Loại xe: "4 chỗ" | Chuyến đi được tạo thành công, hệ thống xác nhận đặt chuyến và chuyển sang trạng thái tìm tài xế.

 |
| **Tìm và phân công tài xế (UC03)** | Hệ thống nhận yêu cầu đặt chuyến hợp lệ.

 | Kiểm tra hệ thống tìm và phân công tài xế hợp lệ đang ở trạng thái sẵn sàng (TC05, TC06, TC07).

 | TX A (Sẵn sàng, cách 1km)<br>

<br>TX B (Đang bận, cách 500m) | Hệ thống bỏ qua TX B, gửi yêu cầu nhận chuyến cho TX A (sẵn sàng và phù hợp).

 |
| **Tìm và phân công tài xế (UC03)** | Hệ thống đã gửi yêu cầu cho tài xế đầu tiên.

 | Kiểm tra hệ thống tự động tìm tài xế khác khi tài xế ban đầu từ chối hoặc quá hạn (TC08).

 | TX A nhấn "Từ chối" hoặc hết thời gian đếm ngược | Hệ thống tự động tìm và gửi yêu cầu cho tài xế sẵn sàng tiếp theo.

 |
| **Thực hiện và Theo dõi chuyến đi (UC04, UC05)** | Tài xế đã chấp nhận chuyến đi.

 | Kiểm tra tài xế cập nhật trạng thái và vị trí (TC09, TC10, TC15).

 | Tài xế nhấn: "Đã đến điểm đón", "Đã đón khách" | Trạng thái cập nhật thành công, khách hàng nhận thông báo trạng thái và thấy vị trí tài xế.

 |
| **Thực hiện chuyến đi (UC05)** | Chuyến đi đang ở trạng thái "Đang di chuyển".

 | Kiểm tra tài xế xác nhận hoàn thành chuyến đi (TC11).

 | Tài xế nhấn "Hoàn thành chuyến" tại điểm đến | Trạng thái chuyến chuyển thành "Hoàn thành", hệ thống chuyển sang tính cước.

 |
| **Tính cước và Thanh toán (UC06)** | Chuyến đi được xác nhận hoàn thành.

 | Kiểm tra hệ thống tính cước (TC12).

 | Quãng đường: 8km<br>

<br>Loại xe: "4 chỗ" | Hệ thống tính toán và hiển thị chính xác số tiền dựa trên loại dịch vụ và chuyến đi.

 |
| **Tính cước và Thanh toán (UC06)** | Khách hàng ở màn hình thanh toán.

 | Kiểm tra chọn phương thức và thanh toán thành công (TC13, TC14, TC16).

 | Phương thức: "Tiền mặt"<br>

<br>Xác nhận thanh toán thành công | Trạng thái thanh toán cập nhật thành công, khách hàng nhận thông báo kết quả thanh toán.

 |
| **Đánh giá tài xế (UC07)** | Chuyến đi đã hoàn tất quá trình thanh toán.

 | Kiểm tra khách hàng gửi đánh giá tài xế hợp lệ (TC17).

 | Đánh giá: 5 sao<br>

<br>Nội dung: "Nhiệt tình" | Đánh giá được lưu thành công vào hệ thống.

 |
| **Đánh giá tài xế (UC07)** | Chuyến đi chưa hoàn thành (Ví dụ: Đang di chuyển).

 | Kiểm tra quy định hệ thống không cho phép đánh giá tài xế khi chuyến chưa hoàn thành (TC17).

 | Khách hàng mở chi tiết chuyến đang diễn ra | Tính năng đánh giá bị ẩn hoặc hệ thống không cho phép thực hiện.

 |
| **Quản lý khách hàng (UC08)** | Nhân viên vận hành đăng nhập thành công.

 | Kiểm tra quyền tìm kiếm và cập nhật thông tin khách hàng (TC18).

 | Chọn Khách hàng Y, thay đổi số điện thoại mới | Thông tin khách hàng Y được cập nhật thành công và lưu vào CSDL.

 |
| **Quản lý tài xế (UC09)** | Nhân viên vận hành đăng nhập thành công.

 | Kiểm tra quyền cập nhật trạng thái hoạt động của tài xế (TC19, TC20).

 | Chọn Tài xế X, đổi trạng thái sang "Không hoạt động" | Trạng thái tài xế được cập nhật, tài xế X không thể nhận thêm yêu cầu chuyến mới.

 |
| **Quản lý vận hành (UC10)** | Nhân viên vận hành đăng nhập thành công.

 | Kiểm tra chức năng theo dõi chuyến đi đang diễn ra (TC21).

 | Truy cập mục "Theo dõi chuyến đi" | Hiển thị danh sách các chuyến đi cùng trạng thái và vị trí tài xế.

 |
| **Quản lý vận hành (UC10)** | Chuyến đi gặp sự cố.

 | Kiểm tra khả năng xử lý chuyến bị lỗi (TC22).

 | Nhân viên chọn chuyến đi bị lỗi, ghi nhận sự cố và hủy/chuyển trạng thái | Hệ thống cập nhật kết quả xử lý sự cố thành công.

 |
| **Xem báo cáo (UC11)** | Nhân viên quản lý đăng nhập thành công.

 | Kiểm tra tra cứu báo cáo hoạt động (TC23).

 | Chọn khoảng thời gian: 01/10 đến 31/10 | Hệ thống hiển thị báo cáo chính xác về số chuyến, doanh thu, tỷ lệ hoàn thành/hủy.

 |
