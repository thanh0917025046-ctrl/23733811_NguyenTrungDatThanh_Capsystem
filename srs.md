Bước 1: Đọc và phân tích sơ khởi của khách hàng: hiểu đc ngữ cảnh của nghiệp vụ ,xác định vấn đề nghiệp vụ(Khách hàng gặp vấn đề gì , tại sao lại chọn lựa hệ thống mới, ai là người)
## Bước 1: Đọc và phân tích sơ khởi yêu cầu của khách hàng

1. Hiểu ngữ cảnh nghiệp vụ

Công ty ABC kinh doanh dịch vụ đặt xe trực tuyến. Khách hàng đặt xe thông qua tổng đài hoặc ứng dụng, sau đó hệ thống tìm tài xế, thực hiện chuyến đi, tính cước, thanh toán và đánh giá.

Công ty muốn xây dựng CAB System trong 7 tuần để tự động hóa quy trình và hỗ trợ 3 nhóm người dùng chính:

Khách hàng: đặt và theo dõi chuyến xe, thanh toán, đánh giá.
Tài xế: nhận chuyến, cập nhật trạng thái và vị trí.
Nhân viên vận hành: quản lý khách hàng, tài xế, chuyến đi, giao dịch và báo cáo.
2. Xác định vấn đề nghiệp vụ

Qua phân tích yêu cầu, các vấn đề chính của hệ thống hiện tại là:

Phân công tài xế còn thủ công, chưa tự động tìm tài xế phù hợp.
Khách hàng khó theo dõi chuyến đi, trạng thái và thời gian tài xế đến chưa được cập nhật đầy đủ.
Thanh toán chưa được quản lý tập trung, gây khó khăn trong quản lý giao dịch.
Khó xử lý khi tài xế từ chối hoặc không phản hồi, chưa có cơ chế tự động tìm tài xế khác.
Nhân viên vận hành khó quản lý và xử lý sự cố liên quan đến chuyến đi, tài xế và giao dịch.
Khó mở rộng hệ thống khi số lượng khách hàng, tài xế và chuyến đi tăng.
Thiếu khả năng báo cáo, thống kê về doanh thu, số chuyến, tỷ lệ hoàn thành/hủy và hiệu quả tài xế.
Yêu cầu về bảo mật và phân quyền cần được tăng cường để bảo vệ dữ liệu khách hàng, tài xế và giao dịch.
###  Khách hàng đang gặp vấn đề gì?

* Việc **tìm kiếm và phân công tài xế còn thủ công**.
* Khách hàng **khó theo dõi trạng thái chuyến đi** và thời gian tài xế đến.
* **Thông tin thanh toán chưa được quản lý tập trung**.
* Khi tài xế **từ chối hoặc không phản hồi**, việc tìm tài xế khác còn hạn chế.
* Nhân viên vận hành **khó quản lý tài xế, khách hàng, chuyến đi và giao dịch**.
* Khó xử lý các trường hợp **chuyến bị lỗi hoặc phát sinh sự cố**.
* Khó thống kê **doanh thu, số lượng chuyến, tỷ lệ hoàn thành/hủy và hiệu quả tài xế**.
* Hệ thống hiện tại **khó mở rộng** khi số lượng khách hàng và tài xế tăng.
* Cần cải thiện **bảo mật, phân quyền và lưu vết thao tác**.

### Tại sao cần lựa chọn hệ thống mới?

Công ty ABC cần xây dựng hệ thống mới để:

* **Tự động hóa** việc tìm kiếm và phân công tài xế.
* Giúp khách hàng **đặt xe và theo dõi chuyến đi dễ dàng**.
* **Quản lý tập trung** chuyến đi và thanh toán.
* Hỗ trợ nhân viên vận hành **quản lý và xử lý sự cố hiệu quả**.
* Cung cấp **báo cáo và thống kê** phục vụ quản lý.
* Nâng cao **tính bảo mật và phân quyền**.
* Đảm bảo hệ thống **ổn định, dễ mở rộng và dễ bảo trì**.
* Cho phép bổ sung **dịch vụ, phương thức thanh toán và kênh thông báo mới** trong tương lai.



### 5. Vấn đề nghiệp vụ tổng quát

> **Công ty ABC đang gặp khó khăn trong việc quản lý và vận hành dịch vụ đặt xe do quy trình phân công tài xế còn thủ công, khách hàng khó theo dõi chuyến đi, thanh toán chưa được quản lý tập trung và hệ thống khó mở rộng. Vì vậy, công ty cần xây dựng CAB System để tự động hóa quy trình đặt xe, nâng cao hiệu quả vận hành, cải thiện trải nghiệm khách hàng và tạo nền tảng có khả năng mở rộng trong tương lai.**
> 
Bước 2 : 2 bảng , 1 bên stackhoder, vai trò
mục 2 : vẽ ma trận stackgoder meatreat
tầm ảnh hưởng vai trò
 Stakeholder     
| STT | Stakeholder                     | Vai trò                                                                      |
| --- | ------------------------------- | ---------------------------------------------------------------------------- |
| 1   | **Ban giám đốc**                | Đưa ra định hướng, phê duyệt dự án, theo dõi doanh thu và hiệu quả hoạt động |
| 2   | **Khách hàng**                  | Đặt xe, theo dõi chuyến đi, thanh toán và đánh giá tài xế                    |
| 3   | **Tài xế**                      | Nhận chuyến, thực hiện chuyến và cập nhật trạng thái, vị trí                 |
| 4   | **Nhân viên vận hành**          | Quản lý khách hàng, tài xế, phương tiện, chuyến đi và xử lý sự cố            |
| 5   | **Nhân viên quản trị hệ thống** | Quản lý tài khoản, phân quyền, bảo mật và cấu hình hệ thống                  |
| 6   | **Nhà cung cấp thanh toán**     | Cung cấp dịch vụ và xử lý thanh toán điện tử                                 |
| 7   | **Nhà cung cấp thông báo**      | Cung cấp các kênh gửi thông báo cho khách hàng và tài xế                     |
| 8   | **Business Analyst (BA)**       | Thu thập, phân tích và làm rõ yêu cầu nghiệp vụ                              |
| 9   | **Đội phát triển hệ thống**     | Thiết kế, xây dựng, kiểm thử và triển khai hệ thống                          |


