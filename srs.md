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
mục 2 : vẽ ma trận stackholder meatreat
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
| 8   | **Đội phát triển hệ thống**     | Thiết kế, xây dựng, kiểm thử và triển khai hệ thống                          |

https://mermaidchart.cello.so/Pc5aeqVy89o

graph TD
    subgraph BanLanhDao [Ban Lanh dao / Ban Giam doc]
        A1[Ban Giam doc Cong ty ABC]
        A2[Bo phan Van hanh / Quan tri]
    end

    subgraph NguoiDungTrucTiep [Nguoi dung truc tiep - End Users]
        B1[Khach hang - Passengers]
        B2[Tai xe - Drivers]
    end

    subgraph DoiTac [Doi tac va Ben thu ba]
        C1[Nha cung cap thanh toan dien tu]
        C2[Nha cung cap dich vu thong bao]
    end

    subgraph NhomPhatTrien [Nhom phat trien]
        D1[Business Analyst - BA]
        D2[Nhom phat trien phan mem / Dev & QA]
    end

    %% Mối quan hệ và vai trò
    A1 -->|Dua ra chien luoc & Ky vong 7 tuan| D1
    A2 -->|Su dung giao dien quan tri & Bao cao| D2
    
    B1 -->|Tao yeu cau, thanh toan, danh gia| D2
    B2 -->|Nhan chuyen, cap nhat vi tri, trang thai| D2

    C1 -->|Tich hop cong thanh toan| D2
    C2 -->|Cung cap kenh thong bao| D2

    D1 -->|Lam ro yeu cau nghiep vu TBD| A1
    D1 -->|Cung cap dac ta tai lieu SRS| D2
Bước 3: Mục đích của nhiệm vụ (BG01, BG02..)
| Mã       | Mục đích nhiệm vụ                            | Nội dung                                                                                                          |
| -------- | -------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **BG01** | **Tự động tìm và phân công tài xế**          | Tìm tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành.  
                                  |
| **BG02** | **Tự động hóa quy trình đặt xe**             | Cho phép khách hàng đặt xe trực tuyến và hệ thống tự động xử lý yêu cầu đặt xe.                                   |
| **BG03** | **Nâng cao khả năng theo dõi chuyến đi**     | Cho phép khách hàng và nhân viên vận hành theo dõi trạng thái chuyến và vị trí tài xế.                            |
| **BG04** | **Quản lý tính cước và thanh toán**          | Tính chính xác số tiền phải trả và hỗ trợ thanh toán tiền mặt hoặc điện tử.                                       |
| **BG05** | **Quản lý thông báo**                        | Cung cấp thông báo kịp thời cho khách hàng và tài xế trong quá trình đặt và thực hiện chuyến.                     |
| **BG06** | **Nâng cao hiệu quả vận hành**               | Hỗ trợ nhân viên quản lý khách hàng, tài xế, phương tiện, chuyến đi và xử lý sự cố.                               |
| **BG07** | **Cung cấp báo cáo và thống kê**             | Theo dõi số chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả tài xế.                                    |
| **BG08** | **Đảm bảo an toàn và bảo mật dữ liệu**       | Xác thực người dùng, phân quyền quản trị, bảo vệ dữ liệu cá nhân, vị trí và giao dịch.                            |
| **BG09** | **Đảm bảo tính ổn định và khả năng mở rộng** | Hệ thống hoạt động ổn định khi tải tăng và cho phép mở rộng từng thành phần độc lập.                              |
| **BG10** | **Tạo nền tảng phát triển lâu dài**          | Cho phép bổ sung dịch vụ, phương thức thanh toán, kênh thông báo và thay đổi thành phần kỹ thuật trong tương lai. |
Bước 4: xác định phạm vi yêu cầu :
vd: quản lí khách hàng, quản lí tài xế ... modul cơ bản dưới dạng phần mềm mdp
- Ngoài phạm vi không cần làm
  1. Phạm vi trong hệ thống
| Mã        | Module                          | Nội dung chính                                                                              |
| --------- | ------------------------------- | ------------------------------------------------------------------------------------------- |
| **MDP01** | **Quản lý khách hàng**          | Đăng ký, đăng nhập, cập nhật thông tin, xem lịch sử chuyến                                  |
| **MDP02** | **Quản lý tài xế**              | Quản lý hồ sơ, trạng thái hoạt động, vị trí và thông tin tài xế                             |
| **MDP03** | **Quản lý phương tiện**         | Quản lý thông tin xe, loại xe và phương tiện của tài xế                                     |
| **MDP04** | **Quản lý đặt xe**              | Nhập điểm đón/điểm đến, chọn loại xe, tạo và quản lý yêu cầu đặt xe                         |
| **MDP05** | **Tìm kiếm & phân công tài xế** | Tìm tài xế phù hợp, ưu tiên tài xế gần và xử lý khi tài xế từ chối/không phản hồi           |
| **MDP06** | **Quản lý chuyến đi**           | Theo dõi và cập nhật trạng thái chuyến: đến điểm đón, đón khách, đang di chuyển, hoàn thành |
| **MDP07** | **Tính cước & thanh toán**      | Tính tiền chuyến đi, hỗ trợ tiền mặt và thanh toán điện tử thông qua nhà cung cấp bên ngoài |
| **MDP08** | **Quản lý thông báo**           | Gửi thông báo về đặt xe, nhận chuyến, trạng thái chuyến và thanh toán                       |
| **MDP09** | **Đánh giá chuyến đi**          | Khách hàng đánh giá tài xế sau khi hoàn thành chuyến                                        |
| **MDP10** | **Quản lý vận hành**            | Theo dõi chuyến đang diễn ra, trạng thái tài xế và xử lý sự cố                              |
| **MDP11** | **Quản trị & phân quyền**       | Quản lý tài khoản nhân viên, quyền truy cập và lưu vết thao tác                             |
| **MDP12** | **Báo cáo & thống kê**          | Báo cáo số chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả tài xế                |

2. Ngoài phạm vi dự án

Những nội dung không cần xây dựng trong giai đoạn này:

❌ Tự xây dựng cổng thanh toán điện tử → chỉ tích hợp nhà cung cấp bên ngoài.
❌ Tự xây dựng hệ thống SMS/Email/Push Notification → chỉ tích hợp dịch vụ thông báo bên ngoài.
❌ Phát triển bản đồ/GPS riêng → chỉ sử dụng dịch vụ bản đồ/vị trí bên ngoài nếu cần.
❌ Quản lý bảo dưỡng, sửa chữa phương tiện.
❌ Quản lý lương, thưởng và chấm công tài xế.
❌ Quản lý kế toán, thuế và tài chính doanh nghiệp chuyên sâu.
❌ Xây dựng dịch vụ giao đồ ăn/giao hàng hoặc các dịch vụ khác ngoài đặt xe.
❌ Xây dựng phần cứng GPS hoặc thiết bị theo dõi riêng.
❌ Các tính năng nâng cao chưa được khách hàng yêu cầu trong giai đoạn đầu.
=> Tóm tắt phạm vi

Trong phạm vi: CAB System tập trung vào quản lý khách hàng, tài xế, phương tiện, đặt xe, tìm và phân công tài xế, quản lý chuyến đi, tính cước – thanh toán, thông báo, đánh giá, vận hành, phân quyền và báo cáo thống kê.

Ngoài phạm vi: Các hệ thống/dịch vụ bên ngoài như cổng thanh toán, bản đồ/GPS, SMS/Email/Push Notification chỉ tích hợp, không tự phát triển; đồng thời không xây dựng các nghiệp vụ như bảo dưỡng xe, tính lương tài xế, kế toán chuyên sâu hay dịch vụ giao hàng.
Bước 5 : Xác định Business Requirement (BR) BR 01 là đặt chuyến:  , 02 , 03... 
mã , tên, diễn dãi
| Mã       | Tên Business Requirement         | Diễn giải                                                                                   |
| -------- | -------------------------------- | ------------------------------------------------------------------------------------------- |
| **BR01** | **Đặt chuyến**                   | Khách hàng nhập điểm đón, điểm đến, chọn loại xe và gửi yêu cầu đặt chuyến.                 |
| **BR02** | **Tìm và phân công tài xế**      | Hệ thống tìm tài xế phù hợp, gửi yêu cầu nhận chuyến và xử lý khi tài xế từ chối.           |
| **BR03** | **Thực hiện chuyến đi**          | Tài xế cập nhật trạng thái và vị trí từ khi nhận chuyến đến khi hoàn thành.                 |
| **BR04** | **Tính cước và thanh toán**      | Hệ thống tính cước và hỗ trợ thanh toán bằng tiền mặt hoặc điện tử.                         |
| **BR05** | **Quản lý thông báo**            | Hệ thống gửi thông báo cho khách hàng và tài xế về các sự kiện của chuyến đi và thanh toán. |
| **BR06** | **Đánh giá tài xế**              | Khách hàng đánh giá tài xế sau khi hoàn thành chuyến đi.                                    |
| **BR07** | **Quản lý khách hàng và tài xế** | Hệ thống quản lý thông tin, tài khoản, trạng thái của khách hàng và tài xế.                 |
| **BR08** | **Quản lý vận hành và báo cáo**  | Nhân viên vận hành theo dõi chuyến, xử lý sự cố và xem các báo cáo hoạt động.               |


Bước 6: Xác định Business Process (BP) quy trình nghiệp vụ
vd: khách hàng đặt chuyến: tạo chuyến đi, điểm đón, điểm đến , hệ thống xác nhận, tìm tài xế ...
| Mã BP    | Tên quy trình                       | Diễn giải                                                                                                                                                                          |
| -------- | ----------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BP01** | **Khách hàng đặt chuyến**           | Khách hàng nhập điểm đón, điểm đến, chọn loại xe → hệ thống tiếp nhận và xác nhận yêu cầu → hệ thống tìm tài xế phù hợp → thông báo kết quả cho khách hàng.                        |
| **BP02** | **Tìm và phân công tài xế**         | Hệ thống kiểm tra các tài xế đang sẵn sàng → xác định tài xế phù hợp và gần khách hàng → gửi yêu cầu nhận chuyến → nếu tài xế từ chối/không phản hồi thì tiếp tục tìm tài xế khác. |
| **BP03** | **Thực hiện chuyến đi**             | Tài xế nhận chuyến → đến điểm đón → cập nhật đã đến → đón khách → cập nhật đang di chuyển → đến điểm đến → hoàn thành chuyến.                                                      |
| **BP04** | **Tính cước chuyến đi**             | Khi chuyến hoàn thành, hệ thống lấy thông tin chuyến đi và loại dịch vụ → tính số tiền khách hàng phải trả → hiển thị kết quả.                                                     |
| **BP05** | **Thanh toán chuyến đi**            | Khách hàng chọn phương thức thanh toán → hệ thống xử lý tiền mặt hoặc gửi yêu cầu đến nhà cung cấp thanh toán điện tử → nhận kết quả → cập nhật trạng thái thanh toán.             |
| **BP06** | **Thông báo chuyến đi**             | Hệ thống phát sinh sự kiện → xác định đối tượng nhận thông báo → gửi thông báo về đặt chuyến, nhận chuyến, tài xế đến, hoàn thành chuyến hoặc thanh toán.                          |
| **BP07** | **Đánh giá tài xế**                 | Sau khi chuyến hoàn thành → khách hàng xem thông tin chuyến → đánh giá tài xế → hệ thống lưu kết quả đánh giá.                                                                     |
| **BP08** | **Quản lý khách hàng**              | Khách hàng đăng ký/đăng nhập → cập nhật thông tin cá nhân → hệ thống lưu và quản lý tài khoản → khách hàng có thể xem lịch sử chuyến đi.                                           |
| **BP09** | **Quản lý tài xế**                  | Tài xế đăng ký hoặc được tạo tài khoản → cập nhật hồ sơ và phương tiện → chuyển trạng thái sẵn sàng → hệ thống cập nhật trạng thái và vị trí tài xế.                               |
| **BP10** | **Vận hành và xử lý sự cố**         | Nhân viên vận hành theo dõi các chuyến đang diễn ra → phát hiện chuyến có vấn đề → kiểm tra thông tin → xử lý hoặc hỗ trợ tài xế/khách hàng → cập nhật kết quả.                    |
| **BP11** | **Quản lý tài khoản và phân quyền** | Quản trị viên tạo/quản lý tài khoản nhân viên → phân quyền theo vai trò → hệ thống kiểm tra quyền trước khi cho phép thực hiện chức năng.                                          |
| **BP12** | **Báo cáo và thống kê**             | Hệ thống tổng hợp dữ liệu chuyến đi, doanh thu, hủy chuyến và hiệu quả tài xế → tạo báo cáo → ban quản lý tra cứu và theo dõi.                                                     |
Bước 7: Phân rã yêu cầu nghiệp vụ FR
vd: Pr01 tìm tài xế ... phân rã FR01 xác định vị trí khách hàng FR2 chọn tài xế online FR3 chọn loại xe FR4: chọn những tài xế có đánh giá cao nếu k có khỏi đưa
| BR       | Tên BR                       | Mã FR    | Yêu cầu chức năng                    |
| -------- | ---------------------------- | -------- | ------------------------------------ |
| **BR01** | Đặt chuyến                   | **FR01** | Nhập điểm đón                        |
|          |                              | **FR02** | Nhập điểm đến                        |
|          |                              | **FR03** | Chọn loại xe                         |
|          |                              | **FR04** | Xác nhận đặt chuyến                  |
| **BR02** | Tìm và phân công tài xế      | **FR05** | Xác định tài xế đang sẵn sàng        |
|          |                              | **FR06** | Tìm tài xế phù hợp và gần khách hàng |
|          |                              | **FR07** | Gửi yêu cầu nhận chuyến              |
|          |                              | **FR08** | Tìm tài xế khác khi tài xế từ chối   |
| **BR03** | Thực hiện chuyến đi          | **FR09** | Cập nhật trạng thái chuyến           |
|          |                              | **FR10** | Cập nhật vị trí tài xế               |
|          |                              | **FR11** | Hoàn thành chuyến đi                 |
| **BR04** | Tính cước và thanh toán      | **FR12** | Tính cước chuyến đi                  |
|          |                              | **FR13** | Chọn phương thức thanh toán          |
|          |                              | **FR14** | Xác nhận kết quả thanh toán          |
| **BR05** | Quản lý thông báo            | **FR15** | Thông báo trạng thái chuyến          |
|          |                              | **FR16** | Thông báo kết quả thanh toán         |
| **BR06** | Đánh giá tài xế              | **FR17** | Đánh giá tài xế                      |
| **BR07** | Quản lý khách hàng và tài xế | **FR18** | Quản lý thông tin khách hàng         |
|          |                              | **FR19** | Quản lý thông tin tài xế             |
|          |                              | **FR20** | Quản lý trạng thái tài xế            |
| **BR08** | Quản lý vận hành và báo cáo  | **FR21** | Theo dõi chuyến đang diễn ra         |
|          |                              | **FR22** | Xử lý chuyến bị lỗi                  |
|          |                              | **FR23** | Xem báo cáo hoạt động                |

Bước 8: BRule ( luật và qui định) , ngoại lệ
vd:luật và qui định: tài xế nào sẵn sàng mới nhận chuyện, ngoại lệ: tìm tài xế quá thời hạn thì resest qua chuyển tài xế khác....
| Mã       | Business Requirement         | Luật và quy định (Business Rule)                                                                             | Ngoại lệ                                                                                           |
| -------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| **BR01** | Đặt chuyến                   | Khách hàng phải nhập **điểm đón, điểm đến và loại xe** trước khi đặt chuyến.                                 | Thiếu thông tin hoặc thông tin không hợp lệ → hệ thống yêu cầu nhập lại.                           |
| **BR02** | Tìm và phân công tài xế      | Chỉ tài xế **đang sẵn sàng nhận chuyến** mới được hệ thống đề xuất.                                          | Tài xế không phản hồi hoặc từ chối quá thời hạn → hệ thống chuyển sang tìm tài xế khác.            |
| **BR03** | Thực hiện chuyến đi          | Tài xế phải cập nhật trạng thái theo đúng trình tự: **đã đến → đã đón khách → đang di chuyển → hoàn thành**. | Tài xế không cập nhật trạng thái → nhân viên vận hành kiểm tra và xử lý.                           |
| **BR04** | Tính cước và thanh toán      | Số tiền thanh toán được xác định dựa trên **loại dịch vụ và thông tin chuyến đi**.                           | Thanh toán điện tử thất bại → thông báo cho khách hàng và cho phép thanh toán lại theo chính sách. |
| **BR05** | Quản lý thông báo            | Hệ thống phải gửi thông báo khi có **sự kiện quan trọng** của chuyến đi hoặc thanh toán.                     | Kênh thông báo lỗi → hệ thống có thể sử dụng kênh khác nếu được cấu hình.                          |
| **BR06** | Đánh giá tài xế              | Chỉ khách hàng đã **hoàn thành chuyến** mới được đánh giá tài xế.                                            | Chuyến chưa hoàn thành → không cho phép đánh giá.                                                  |
| **BR07** | Quản lý khách hàng và tài xế | Người dùng phải **đăng nhập/xác thực** trước khi sử dụng chức năng yêu cầu tài khoản.                        | Đăng nhập sai hoặc tài khoản không hợp lệ → từ chối truy cập.                                      |
| **BR08** | Quản lý vận hành và báo cáo  | Chỉ nhân viên có **đúng quyền hạn** mới được thực hiện các chức năng quản trị.                               | Không đủ quyền → hệ thống từ chối thao tác và ghi nhận sự kiện nếu cần.                            |
Bước 9: xây dựng moding data (nhìn dô đó xác định thực thể rồi vẽ RD).

1. Xác định các thực thể

Từ hệ thống CAB, có thể xác định các thực thể chính:
| STT   | Thực thể        | Ý nghĩa                             |
| ----- | --------------- | ----------------------------------- |
| **1** | **KHACH_HANG**  | Lưu thông tin khách hàng            |
| **2** | **TAI_XE**      | Lưu thông tin tài xế                |
| **3** | **PHUONG_TIEN** | Lưu thông tin phương tiện           |
| **4** | **CHUYEN_DI**   | Lưu thông tin các chuyến xe         |
| **5** | **LOAI_XE**     | Lưu các loại xe                     |
| **6** | **THANH_TOAN**  | Lưu thông tin thanh toán            |
| **7** | **DANH_GIA**    | Lưu đánh giá của khách hàng         |
| **8** | **THONG_BAO**   | Lưu thông báo cho khách hàng/tài xế |
2. Thuộc tính chính
KHACH_HANG
MaKH (PK)
HoTen
SoDienThoai
Email
MatKhau
DiaChi
TAI_XE
MaTX (PK)
HoTen
SoDienThoai
MatKhau
TrangThai
ViTriHienTai
PHUONG_TIEN
MaPT (PK)
BienSo
MauXe
MaTX (FK)
MaLoaiXe (FK)
LOAI_XE
MaLoaiXe (PK)
TenLoaiXe
MoTa
CHUYEN_DI
MaChuyen (PK)
MaKH (FK)
MaTX (FK)
DiemDon
DiemDen
ThoiGianDat
ThoiGianDon
TrangThai
SoTien
THANH_TOAN
MaTT (PK)
MaChuyen (FK)
PhuongThuc
SoTien
TrangThai
ThoiGianThanhToan
DANH_GIA
MaDG (PK)
MaChuyen (FK)
MaKH (FK)
MaTX (FK)
SoSao
NoiDung
THONG_BAO
MaTB (PK)
NoiDung
ThoiGian
TrangThai
MaKH / MaTX


Quan hệ chính
KHACH_HANG ||--o{ CHUYEN_DI: 1 khách hàng đặt nhiều chuyến
TAI_XE ||--o{ CHUYEN_DI: 1 tài xế thực hiện nhiều chuyến
TAI_XE ||--|| PHUONG_TIEN: 1 tài xế – 1 phương tiện
LOAI_XE ||--o{ PHUONG_TIEN: 1 loại xe có nhiều phương tiện
CHUYEN_DI ||--|| THANH_TOAN: 1 chuyến có 1 thanh toán
CHUYEN_DI ||--o| DANH_GIA: 1 chuyến có thể có 1 đánh giá
KHACH_HANG/TAI_XE ||--o{ THONG_BAO: mỗi người có thể nhận nhiều thông báo.

erDiagram
    KHACH_HANG ||--o{ CHUYEN_DI : dat
    TAI_XE ||--o{ CHUYEN_DI : thuc_hien
    TAI_XE ||--|| PHUONG_TIEN : su_dung
    LOAI_XE ||--o{ PHUONG_TIEN : thuoc
    CHUYEN_DI ||--|| THANH_TOAN : co
    CHUYEN_DI ||--o| DANH_GIA : duoc_danh_gia
    KHACH_HANG ||--o{ THONG_BAO : nhan
    TAI_XE ||--o{ THONG_BAO : nhan

    KHACH_HANG {
        int MaKH PK
        string HoTen
        string SoDienThoai
        string Email
        string MatKhau
        string DiaChi
    }

    TAI_XE {
        int MaTX PK
        string HoTen
        string SoDienThoai
        string MatKhau
        string TrangThai
        string ViTriHienTai
    }

    PHUONG_TIEN {
        int MaPT PK
        string BienSo
        string MauXe
        int MaTX FK
        int MaLoaiXe FK
    }

    LOAI_XE {
        int MaLoaiXe PK
        string TenLoaiXe
        string MoTa
    }

    CHUYEN_DI {
        int MaChuyen PK
        int MaKH FK
        int MaTX FK
        string DiemDon
        string DiemDen
        datetime ThoiGianDat
        datetime ThoiGianDon
        string TrangThai
        decimal SoTien
    }

    THANH_TOAN {
        int MaTT PK
        int MaChuyen FK
        string PhuongThuc
        decimal SoTien
        string TrangThai
        datetime ThoiGianThanhToan
    }

    DANH_GIA {
        int MaDG PK
        int MaChuyen FK
        int MaKH FK
        int MaTX FK
        int SoSao
        string NoiDung
    }

    THONG_BAO {
        int MaTB PK
        string NoiDung
        datetime ThoiGian
        string TrangThai
        int MaKH FK
        int MaTX FK
    }
 Bước 10: xác định các chức năng không yêu cầu
 vd: hệ thông trong giai đoạn mvp không quan tronhj thời gian phản hồi
 | STT | Chức năng không yêu cầu                              | Giải thích                                                                                          |
| --- | ---------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| 1   | **Quản lý bảo dưỡng, sửa chữa xe**                   | Không thuộc quy trình đặt và quản lý chuyến xe.                                                     |
| 2   | **Quản lý lương, thưởng tài xế**                     | Không nằm trong phạm vi vận hành đặt xe.                                                            |
| 3   | **Quản lý kế toán, thuế**                            | Chỉ quản lý thông tin thanh toán chuyến, không xây dựng hệ thống kế toán.                           |
| 4   | **Tự xây dựng cổng thanh toán**                      | Chỉ tích hợp với nhà cung cấp thanh toán bên ngoài.                                                 |
| 5   | **Tự xây dựng hệ thống GPS/Bản đồ**                  | Chỉ sử dụng dịch vụ bản đồ/vị trí bên ngoài.                                                        |
| 6   | **Tự xây dựng hệ thống SMS/Email/Push Notification** | Chỉ tích hợp với nhà cung cấp thông báo bên ngoài.                                                  |
| 7   | **Đặt nhiều chuyến cùng lúc**                        | MVP chỉ tập trung vào một yêu cầu đặt chuyến tại một thời điểm.                                     |
| 8   | **Đặt xe định kỳ**                                   | Chưa được yêu cầu trong giai đoạn hiện tại.                                                         |
| 9   | **Chương trình khuyến mãi/điểm thưởng**              | Chưa nằm trong yêu cầu ban đầu của khách hàng.                                                      |
| 10  | **Chat trực tiếp giữa khách hàng và tài xế**         | Không phải chức năng cốt lõi của hệ thống đặt xe trong MVP.                                         |
| 11  | **Thời gian phản hồi nâng cao**                      | Trong MVP chưa yêu cầu tối ưu chuyên sâu về thời gian phản hồi; chỉ cần hệ thống hoạt động ổn định. |
| 12  | **Dự báo nhu cầu và giá động bằng AI**               | Chưa có yêu cầu và chưa cần triển khai trong giai đoạn đầu.                                         |
Bước 11: Xác định và vẽ UC vd: UC01 custormer...
1. Danh sách Use Case
| Mã       | Tên Use Case            | Tác nhân                      |
| -------- | ----------------------- | ----------------------------- |
| **UC01** | Đăng ký / Đăng nhập     | Khách hàng, Tài xế, Nhân viên |
| **UC02** | Đặt chuyến              | Khách hàng                    |
| **UC03** | Tìm và phân công tài xế | Hệ thống                      |
| **UC04** | Theo dõi chuyến đi      | Khách hàng, Tài xế, Nhân viên |
| **UC05** | Thực hiện chuyến        | Tài xế                        |
| **UC06** | Thanh toán              | Khách hàng                    |
| **UC07** | Đánh giá tài xế         | Khách hàng                    |
| **UC08** | Quản lý khách hàng      | Nhân viên                     |
| **UC09** | Quản lý tài xế          | Nhân viên                     |
| **UC10** | Quản lý vận hành        | Nhân viên                     |
| **UC11** | Xem báo cáo             | Nhân viên quản lý             |
Quan hệ giữa các Use Case
UC02 Đặt chuyến <<include>> UC03 Tìm và phân công tài xế
UC05 Thực hiện chuyến <<include>> UC04 Theo dõi chuyến đi
UC06 Thanh toán <<include>> Tính cước
UC07 Đánh giá tài xế <<extend>> UC05 Thực hiện chuyến
Khi tài xế từ chối/không phản hồi → UC03 thực hiện lại việc tìm tài xế khác.
**Sơ đồ UC**
flowchart LR
    KH([Khách hàng])
    TX([Tài xế])
    NV([Nhân viên])
    QL([Quản lý])

    UC01((UC01<br/>Đăng ký / Đăng nhập))
    UC02((UC02<br/>Đặt chuyến))
    UC03((UC03<br/>Tìm và phân công tài xế))
    UC04((UC04<br/>Theo dõi chuyến đi))
    UC05((UC05<br/>Thực hiện chuyến))
    UC06((UC06<br/>Thanh toán))
    UC07((UC07<br/>Đánh giá tài xế))
    UC08((UC08<br/>Quản lý khách hàng))
    UC09((UC09<br/>Quản lý tài xế))
    UC10((UC10<br/>Quản lý vận hành))
    UC11((UC11<br/>Xem báo cáo))

    KH --- UC01
    KH --- UC02
    KH --- UC04
    KH --- UC06
    KH --- UC07

    TX --- UC01
    TX --- UC04
    TX --- UC05

    NV --- UC01
    NV --- UC08
    NV --- UC09
    NV --- UC10
    NV --- UC11

    QL --- UC11

    UC02 -.->|include| UC03
    UC05 -.->|include| UC04
    UC07 -.->|extend| UC05

Bước 12 : Đặc tả UC
**UC01** Đăng ký/Đăng nhập
**UC02** Đặt chuyến
**UC03** Tìm và phân công tài xế
**UC04** Theo dõi chuyến đi
**UC05** Thực hiện chuyến
**UC06** Thanh toán
**UC07** Đánh giá tài xế
**UC08** Quản lý khách hàng
**UC09** Quản lý tài xế
**UC10** Quản lý vận hành
**UC11** Xem báo cáo


## UC01 – Đăng ký / Đăng nhập

| Nội dung           | Mô tả                                                                                                                                             |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**   | Đăng ký / Đăng nhập                                                                                                                               |
| **Mã**             | UC01                                                                                                                                              |
| **Tác nhân**       | Khách hàng, Tài xế, Nhân viên                                                                                                                     |
| **Mục tiêu**       | Cho phép người dùng đăng ký và đăng nhập vào hệ thống.                                                                                            |
| **Tiền điều kiện** | Người dùng chưa đăng nhập.                                                                                                                        |
| **Hậu điều kiện**  | Người dùng đăng nhập thành công vào hệ thống.                                                                                                     |
| **Luồng chính**    | 1. Người dùng chọn đăng ký/đăng nhập → 2. Nhập thông tin → 3. Hệ thống kiểm tra thông tin → 4. Hệ thống xác thực → 5. Cho phép truy cập hệ thống. |
| **Ngoại lệ**       | Thông tin sai hoặc tài khoản không tồn tại → hệ thống thông báo lỗi và yêu cầu nhập lại.                                                          |

---

## UC02 – Đặt chuyến

| Nội dung           | Mô tả                                                                                                                                                              |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Tên Use Case**   | Đặt chuyến                                                                                                                                                         |
| **Mã**             | UC02                                                                                                                                                               |
| **Tác nhân**       | Khách hàng                                                                                                                                                         |
| **Mục tiêu**       | Cho phép khách hàng tạo yêu cầu đặt xe.                                                                                                                            |
| **Tiền điều kiện** | Khách hàng đã đăng nhập.                                                                                                                                           |
| **Hậu điều kiện**  | Yêu cầu đặt chuyến được tạo.                                                                                                                                       |
| **Luồng chính**    | 1. Khách hàng chọn đặt chuyến → 2. Nhập điểm đón → 3. Nhập điểm đến → 4. Chọn loại xe → 5. Xác nhận đặt chuyến → 6. Hệ thống tạo yêu cầu → 7. Hệ thống tìm tài xế. |
| **Ngoại lệ**       | Thông tin không hợp lệ → yêu cầu nhập lại. Không tìm được tài xế → thông báo cho khách hàng.                                                                       |

---

## UC03 – Tìm và phân công tài xế

| Nội dung           | Mô tả                                                                                                                                                                                   |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**   | Tìm và phân công tài xế                                                                                                                                                                 |
| **Mã**             | UC03                                                                                                                                                                                    |
| **Tác nhân**       | Hệ thống                                                                                                                                                                                |
| **Mục tiêu**       | Tìm tài xế phù hợp cho chuyến đi.                                                                                                                                                       |
| **Tiền điều kiện** | Có yêu cầu đặt chuyến.                                                                                                                                                                  |
| **Hậu điều kiện**  | Tài xế được phân công cho chuyến hoặc thông báo không tìm được tài xế.                                                                                                                  |
| **Luồng chính**    | 1. Hệ thống nhận yêu cầu → 2. Kiểm tra tài xế đang sẵn sàng → 3. Tìm tài xế phù hợp và gần khách hàng → 4. Gửi yêu cầu nhận chuyến → 5. Tài xế chấp nhận → 6. Hệ thống xác nhận tài xế. |
| **Ngoại lệ**       | Tài xế từ chối/không phản hồi → hệ thống tìm tài xế khác. Không có tài xế phù hợp → thông báo khách hàng.                                                                               |

---

## UC04 – Theo dõi chuyến đi

| Nội dung           | Mô tả                                                                                                                                         |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**   | Theo dõi chuyến đi                                                                                                                            |
| **Mã**             | UC04                                                                                                                                          |
| **Tác nhân**       | Khách hàng, Tài xế, Nhân viên                                                                                                                 |
| **Mục tiêu**       | Theo dõi trạng thái và vị trí của chuyến đi.                                                                                                  |
| **Tiền điều kiện** | Chuyến đi đã được tạo.                                                                                                                        |
| **Hậu điều kiện**  | Trạng thái chuyến được cập nhật và hiển thị.                                                                                                  |
| **Luồng chính**    | 1. Người dùng mở thông tin chuyến → 2. Hệ thống hiển thị trạng thái → 3. Hiển thị vị trí tài xế → 4. Cập nhật trạng thái khi chuyến thay đổi. |
| **Ngoại lệ**       | Không cập nhật được vị trí → hệ thống thông báo dữ liệu vị trí tạm thời không khả dụng.                                                       |

---

## UC05 – Thực hiện chuyến

| Nội dung           | Mô tả                                                                                                                                                |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**   | Thực hiện chuyến                                                                                                                                     |
| **Mã**             | UC05                                                                                                                                                 |
| **Tác nhân**       | Tài xế                                                                                                                                               |
| **Mục tiêu**       | Cho phép tài xế thực hiện chuyến và cập nhật trạng thái.                                                                                             |
| **Tiền điều kiện** | Tài xế đã nhận chuyến.                                                                                                                               |
| **Hậu điều kiện**  | Chuyến đi được hoàn thành.                                                                                                                           |
| **Luồng chính**    | 1. Tài xế nhận chuyến → 2. Đến điểm đón → 3. Cập nhật đã đến → 4. Đón khách → 5. Cập nhật đang di chuyển → 6. Đến điểm đến → 7. Cập nhật hoàn thành. |
| **Ngoại lệ**       | Tài xế không thể tiếp tục chuyến → thông báo cho hệ thống/nhân viên vận hành để xử lý.                                                               |

---

## UC06 – Thanh toán

| Nội dung           | Mô tả                                                                                                                                                                             |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**   | Thanh toán                                                                                                                                                                        |
| **Mã**             | UC06                                                                                                                                                                              |
| **Tác nhân**       | Khách hàng                                                                                                                                                                        |
| **Mục tiêu**       | Cho phép khách hàng thanh toán chi phí chuyến đi.                                                                                                                                 |
| **Tiền điều kiện** | Chuyến đi đã hoàn thành và hệ thống đã tính cước.                                                                                                                                 |
| **Hậu điều kiện**  | Kết quả thanh toán được lưu vào hệ thống.                                                                                                                                         |
| **Luồng chính**    | 1. Hệ thống tính cước → 2. Hiển thị số tiền → 3. Khách hàng chọn phương thức thanh toán → 4. Thực hiện thanh toán → 5. Hệ thống nhận kết quả → 6. Cập nhật trạng thái thanh toán. |
| **Ngoại lệ**       | Thanh toán điện tử thất bại → thông báo khách hàng và cho phép thanh toán lại.                                                                                                    |

---

## UC07 – Đánh giá tài xế

| Nội dung           | Mô tả                                                                                                                     |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**   | Đánh giá tài xế                                                                                                           |
| **Mã**             | UC07                                                                                                                      |
| **Tác nhân**       | Khách hàng                                                                                                                |
| **Mục tiêu**       | Cho phép khách hàng đánh giá tài xế sau chuyến đi.                                                                        |
| **Tiền điều kiện** | Chuyến đi đã hoàn thành.                                                                                                  |
| **Hậu điều kiện**  | Đánh giá được lưu vào hệ thống.                                                                                           |
| **Luồng chính**    | 1. Khách hàng chọn chuyến đã hoàn thành → 2. Chọn số sao → 3. Nhập nhận xét → 4. Gửi đánh giá → 5. Hệ thống lưu đánh giá. |
| **Ngoại lệ**       | Chuyến chưa hoàn thành → hệ thống không cho phép đánh giá.                                                                |

---

## UC08 – Quản lý khách hàng

| Nội dung           | Mô tả                                                                                                                                        |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**   | Quản lý khách hàng                                                                                                                           |
| **Mã**             | UC08                                                                                                                                         |
| **Tác nhân**       | Nhân viên                                                                                                                                    |
| **Mục tiêu**       | Cho phép nhân viên quản lý thông tin khách hàng.                                                                                             |
| **Tiền điều kiện** | Nhân viên đã đăng nhập và có quyền quản lý.                                                                                                  |
| **Hậu điều kiện**  | Thông tin khách hàng được cập nhật.                                                                                                          |
| **Luồng chính**    | 1. Nhân viên chọn quản lý khách hàng → 2. Tìm kiếm khách hàng → 3. Xem thông tin → 4. Thêm/sửa thông tin khi cần → 5. Hệ thống lưu thay đổi. |
| **Ngoại lệ**       | Không tìm thấy khách hàng → hệ thống thông báo. Nhân viên không đủ quyền → từ chối thao tác.                                                 |

---

## UC09 – Quản lý tài xế

| Nội dung           | Mô tả                                                                                                                                    |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**   | Quản lý tài xế                                                                                                                           |
| **Mã**             | UC09                                                                                                                                     |
| **Tác nhân**       | Nhân viên                                                                                                                                |
| **Mục tiêu**       | Cho phép nhân viên quản lý thông tin và trạng thái tài xế.                                                                               |
| **Tiền điều kiện** | Nhân viên đã đăng nhập và có quyền quản lý.                                                                                              |
| **Hậu điều kiện**  | Thông tin tài xế được cập nhật.                                                                                                          |
| **Luồng chính**    | 1. Nhân viên chọn quản lý tài xế → 2. Tìm tài xế → 3. Xem thông tin → 4. Thêm/sửa thông tin → 5. Cập nhật trạng thái → 6. Lưu thông tin. |
| **Ngoại lệ**       | Tài xế không tồn tại → thông báo. Không đủ quyền → từ chối thao tác.                                                                     |

---

## UC10 – Quản lý vận hành

| Nội dung           | Mô tả                                                                                                                                                             |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**   | Quản lý vận hành                                                                                                                                                  |
| **Mã**             | UC10                                                                                                                                                              |
| **Tác nhân**       | Nhân viên                                                                                                                                                         |
| **Mục tiêu**       | Theo dõi chuyến và xử lý các vấn đề phát sinh.                                                                                                                    |
| **Tiền điều kiện** | Nhân viên đã đăng nhập.                                                                                                                                           |
| **Hậu điều kiện**  | Vấn đề của chuyến được xử lý hoặc ghi nhận.                                                                                                                       |
| **Luồng chính**    | 1. Nhân viên xem danh sách chuyến → 2. Kiểm tra trạng thái chuyến → 3. Phát hiện chuyến có vấn đề → 4. Kiểm tra thông tin → 5. Xử lý sự cố → 6. Cập nhật kết quả. |
| **Ngoại lệ**       | Không đủ quyền xử lý → hệ thống từ chối thao tác. Sự cố không thể xử lý → chuyển cấp quản lý.                                                                     |

---

## UC11 – Xem báo cáo

| Nội dung           | Mô tả                                                                                                                                                    |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**   | Xem báo cáo                                                                                                                                              |
| **Mã**             | UC11                                                                                                                                                     |
| **Tác nhân**       | Nhân viên quản lý                                                                                                                                        |
| **Mục tiêu**       | Theo dõi tình hình hoạt động của hệ thống.                                                                                                               |
| **Tiền điều kiện** | Người dùng đã đăng nhập và có quyền xem báo cáo.                                                                                                         |
| **Hậu điều kiện**  | Báo cáo được hiển thị.                                                                                                                                   |
| **Luồng chính**    | 1. Người dùng chọn báo cáo → 2. Chọn khoảng thời gian → 3. Hệ thống tổng hợp dữ liệu → 4. Hiển thị số chuyến, doanh thu, tỷ lệ hoàn thành và hủy chuyến. |
| **Ngoại lệ**       | Không có dữ liệu → hệ thống thông báo không có dữ liệu trong khoảng thời gian đã chọn.                                                                   |
Bước 13: Những tiêu chí chấp nhận ( những AC : những qui tắc cụ thể để đáp ứng giúp cho người làm   phần mềm biết kết thúc và nghiệm thu)
| Mã       | Use Case                    | Tiêu chí chấp nhận                                                                                             |
| -------- | --------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **AC01** | **Đăng ký / Đăng nhập**     | Người dùng nhập đúng thông tin thì đăng nhập thành công; nhập sai thì hệ thống thông báo lỗi.                  |
| **AC02** | **Đặt chuyến**              | Khách hàng nhập đầy đủ điểm đón, điểm đến, loại xe và xác nhận thì hệ thống tạo chuyến thành công.             |
| **AC03** | **Tìm và phân công tài xế** | Hệ thống chỉ tìm tài xế đang sẵn sàng; nếu tài xế từ chối/không phản hồi thì hệ thống tự động tìm tài xế khác. |
| **AC04** | **Theo dõi chuyến đi**      | Khách hàng xem được tài xế, trạng thái chuyến và vị trí tài xế trong quá trình thực hiện chuyến.               |
| **AC05** | **Thực hiện chuyến**        | Tài xế có thể cập nhật các trạng thái: đã đến, đã đón khách, đang di chuyển và hoàn thành.                     |
| **AC06** | **Thanh toán**              | Hệ thống tính đúng số tiền và cập nhật kết quả thanh toán thành công/thất bại.                                 |
| **AC07** | **Đánh giá tài xế**         | Chỉ khách hàng có chuyến đã hoàn thành mới được đánh giá và đánh giá được lưu thành công.                      |
| **AC08** | **Quản lý khách hàng**      | Nhân viên có quyền có thể tìm kiếm, xem và cập nhật thông tin khách hàng.                                      |
| **AC09** | **Quản lý tài xế**          | Nhân viên có quyền có thể xem, cập nhật thông tin và trạng thái tài xế.                                        |
| **AC10** | **Quản lý vận hành**        | Nhân viên có thể xem chuyến đang diễn ra và xử lý các chuyến gặp sự cố.                                        |
| **AC11** | **Xem báo cáo**             | Người có quyền có thể xem báo cáo số chuyến, doanh thu, tỷ lệ hoàn thành và tỷ lệ hủy.                         |









