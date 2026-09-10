```python
import openpyxl, os

print("Files in current dir:", os.listdir('.'))
# Look for CAB_Test_Cases.xlsx or testcase folder
for root, dirs, files in os.walk('.'):
    for f in files:
        if 'xlsx' in f or 'test' in f.lower():
            print(os.path.join(root, f))


```

```text
Files in current dir: ['srs.md', '23733811_NguyenTrungDatThanh_Capsystem-main.zip', 'CAB_Test_Cases.xlsx']
./CAB_Test_Cases.xlsx


```

```python
import pandas as pd

excel_file = 'CAB_Test_Cases.xlsx'
xls = pd.ExcelFile(excel_file)
print("Sheet names:", xls.sheet_names)

for sheet in xls.sheet_names:
    df = pd.read_excel(excel_file, sheet_name=sheet)
    print(f"\n--- Sheet: {sheet} ---")
    print("Columns:", df.columns.tolist())
    print("Head:\n", df.head(3))


```

```text
Sheet names: ['Mô tả các cột', 'Login Test Cases']

--- Sheet: Mô tả các cột ---
Columns: ['Cột', 'Ý nghĩa', 'Mô tả chi tiết', 'Ví dụ']
Head:
              Cột                              Ý nghĩa                                                                                              Mô tả chi tiết                                      Ví dụ
0   Test Case ID  Mã định danh duy nhất của Test Case                                               Dùng để quản lý, tìm kiếm, truy xuất và tham chiếu Test Case.                               TC_LOGIN_001
1  Test Scenario  Scenario mà Test Case đang kiểm thử  Mô tả chức năng hoặc tình huống cần kiểm thử ở mức tổng quát. Một Test Scenario có thể có nhiều Test Case.               Kiểm tra chức năng đăng nhập
2      Test Case           Trường hợp kiểm thử cụ thể                                      Mô tả chính xác trường hợp cần kiểm thử được phân rã từ Test Scenario.  Đăng nhập với username và password hợp lệ

--- Sheet: Login Test Cases ---
Columns: ['Test Case ID', 'Test Scenario', 'Test Case', 'Preconditions', 'Test Steps', 'Test Data', 'Expected Result', 'Priority']
Head:
   Test Case ID         Test Scenario                                  Test Case                         Preconditions                                                               Test Steps                                    Test Data                                                          Expected Result Priority
0  TC-AUTH-001  Người dùng đăng nhập  Đăng nhập với username và password hợp lệ   Tài khoản đã đăng ký và đang Active           1. Mở Login\n2. Nhập username\n3. Nhập password\n4. Nhấn Login     Username: user01\nPassword: Password@123             Đăng nhập thành công; tạo phiên/token và chuyển vào hệ thống     High
1  TC-AUTH-002  Người dùng đăng nhập       Đăng nhập với username không tồn tại               Hệ thống đang hoạt động           1. Mở Login\n2. Nhập username\n3. Nhập password\n4. Nhấn Login  Username: unknown01\nPassword: Password@123  Đăng nhập thất bại; hiển thị thông báo thông tin đăng nhập không hợp lệ     High
2  TC-AUTH-003  Người dùng đăng nhập          Đăng nhập với password không đúng  Username tồn tại và tài khoản Active  1. Mở Login\n2. Nhập username đúng\n3. Nhập password sai\n4. Nhấn Login        Username: user01\nPassword: Wrong@123                                Đăng nhập thất bại; không tạo phiên/token     High


```

```python
df_login = pd.read_excel(excel_file, sheet_name='Login Test Cases')
print(df_login)


```

```text
   Test Case ID         Test Scenario                                             Test Case                            Preconditions                                                                                                Test Steps                                     Test Data                                                                  Expected Result Priority
0   TC-AUTH-001  Người dùng đăng nhập             Đăng nhập với username và password hợp lệ      Tài khoản đã đăng ký và đang Active                                            1. Mở Login\n2. Nhập username\n3. Nhập password\n4. Nhấn Login      Username: user01\nPassword: Password@123                     Đăng nhập thành công; tạo phiên/token và chuyển vào hệ thống     High
1   TC-AUTH-002  Người dùng đăng nhập                  Đăng nhập với username không tồn tại                  Hệ thống đang hoạt động                                            1. Mở Login\n2. Nhập username\n3. Nhập password\n4. Nhấn Login   Username: unknown01\nPassword: Password@123          Đăng nhập thất bại; hiển thị thông báo thông tin đăng nhập không hợp lệ     High
2   TC-AUTH-003  Người dùng đăng nhập                     Đăng nhập với password không đúng     Username tồn tại và tài khoản Active                                   1. Mở Login\n2. Nhập username đúng\n3. Nhập password sai\n4. Nhấn Login         Username: user01\nPassword: Wrong@123                                        Đăng nhập thất bại; không tạo phiên/token     High
3   TC-AUTH-004  Người dùng đăng nhập                                     Username để trống                    Đang ở màn hình Login                                                     1. Để trống username\n2. Nhập password\n3. Nhấn Login       Username: empty\nPassword: Password@123                          Không cho đăng nhập; hiển thị lỗi yêu cầu nhập username     High
4   TC-AUTH-005  Người dùng đăng nhập                                     Password để trống                    Đang ở màn hình Login                                                     1. Nhập username\n2. Để trống password\n3. Nhấn Login             Username: user01\nPassword: empty                          Không cho đăng nhập; hiển thị lỗi yêu cầu nhập password     High
5   TC-AUTH-006  Người dùng đăng nhập                     Username và password đều để trống                    Đang ở màn hình Login                                             1. Không nhập username\n2. Không nhập password\n3. Nhấn Login              Username: empty\nPassword: empty                           Không cho đăng nhập; hiển thị lỗi validation tương ứng     High
6   TC-AUTH-007  Người dùng đăng nhập                    Username có định dạng không hợp lệ                    Đang ở màn hình Login                                            1. Nhập username không hợp lệ\n2. Nhập password\n3. Nhấn Login     Username: user@@@\nPassword: Password@123                            Từ chối dữ liệu và hiển thị lỗi username không hợp lệ   Medium
7   TC-AUTH-008  Người dùng đăng nhập                    Password có định dạng không hợp lệ      Quy tắc password đã được định nghĩa                                      1. Nhập username\n2. Nhập password không đáp ứng rule\n3. Nhấn Login               Username: user01\nPassword: 123                            Từ chối dữ liệu và hiển thị lỗi password không hợp lệ   Medium
8   TC-AUTH-009  Người dùng đăng nhập                      Đăng nhập bằng tài khoản bị khóa     Tài khoản user01 ở trạng thái Locked                                                    1. Nhập username\n2. Nhập password đúng\n3. Nhấn Login      Username: user01\nPassword: Password@123                                  Đăng nhập thất bại; thông báo tài khoản bị khóa     High
9   TC-AUTH-010  Người dùng đăng nhập                     Đăng nhập bằng tài khoản Inactive         Tài khoản tồn tại nhưng Inactive                                                    1. Nhập username\n2. Nhập password đúng\n3. Nhấn Login  Username: inactive01\nPassword: Password@123                          Đăng nhập thất bại; thông báo tài khoản không hoạt động     High
10  TC-AUTH-011  Người dùng đăng nhập                 Username phân biệt chữ hoa/chữ thường       Quy tắc xử lý username đã xác định                                    1. Nhập username khác hoa/thường\n2. Nhập password đúng\n3. Nhấn Login      Username: User01\nPassword: Password@123                             Xử lý đúng theo rule case-sensitive/case-insensitive   Medium
11  TC-AUTH-012  Người dùng đăng nhập                 Password phân biệt chữ hoa/chữ thường                         Tài khoản Active                                    1. Nhập username đúng\n2. Nhập password khác hoa/thường\n3. Nhấn Login      Username: user01\nPassword: password@123                             Đăng nhập thất bại nếu password phân biệt hoa/thường     High
12  TC-AUTH-013  Người dùng đăng nhập                       Nhập password chứa khoảng trắng                         Tài khoản Active                                         1. Nhập username\n2. Nhập password có khoảng trắng\n3. Nhấn Login    Username: user01\nPassword:  Password@123                                        Xử lý khoảng trắng đúng theo Business Rule   Medium
13  TC-AUTH-014  Người dùng đăng nhập            Kiểm tra password không hiển thị plaintext                    Đang ở màn hình Login                                                                     1. Click ô Password\n2. Nhập password                        Password: Password@123                                                           Password được che/mask   Medium
14  TC-AUTH-015  Người dùng đăng nhập  Đăng nhập thành công và truy cập chức năng được phép             Tài khoản Active và có quyền  1. Nhập username hợp lệ\n2. Nhập password hợp lệ\n3. Login\n4. Truy cập chức năng yêu cầu authentication      Username: user01\nPassword: Password@123              Authentication thành công và truy cập được chức năng được cấp quyền     High
15  TC-AUTH-016  Người dùng đăng nhập                  Đăng nhập nhiều lần với password sai  Có cơ chế giới hạn số lần đăng nhập sai                              1. Nhập username đúng\n2. Nhập password sai\n3. Lặp lại theo số lần quy định         Username: user01\nPassword: Wrong@123  Sau số lần sai theo Business Rule, tài khoản bị khóa hoặc áp dụng cơ chế bảo vệ     High
16  TC-AUTH-017  Người dùng đăng nhập                             Request không có username                 API Login đang hoạt động                                                               1. Gửi request Login\n2. Bỏ trường username                    { password: Password@123 }                                     API trả lỗi validation; không authentication     High
17  TC-AUTH-018  Người dùng đăng nhập                             Request không có password                 API Login đang hoạt động                                                               1. Gửi request Login\n2. Bỏ trường password                          { username: user01 }                                     API trả lỗi validation; không authentication     High
18  TC-AUTH-019  Người dùng đăng nhập            Request với username/password không hợp lệ                 API Login đang hoạt động                                                        1. Gửi request Login\n2. Nhập dữ liệu không hợp lệ            Username: unknown\nPassword: wrong                                    API trả response lỗi phù hợp; không tạo token     High
19  TC-AUTH-020  Người dùng đăng nhập                        Response không trả về password                     Đăng nhập thành công                                                         1. Gửi request Login hợp lệ\n2. Kiểm tra response      Username: user01\nPassword: Password@123                             Response không chứa password hoặc thông tin nhạy cảm     High


```

Bộ Test Case dưới đây được xây dựng chuẩn theo đúng định dạng mẫu file **`CAB_Test_Cases.xlsx`** (gồm các cột: *Test Case ID, Test Scenario, Test Case, Preconditions, Test Steps, Test Data, Expected Result, Priority*), bám sát các Use Case và ma trận truy xuất (RTM) từ tài liệu **`srs.md`** (từ **TC01** đến **TC23**).

| Test Case ID | Test Scenario | Test Case | Preconditions | Test Steps | Test Data | Expected Result | Priority |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **TC-BOOK-001** *(TC01)* | Khách hàng đặt chuyến xe | Đặt chuyến xe thành công với đầy đủ thông tin hợp lệ | Khách hàng đã đăng nhập tài khoản hợp lệ trên ứng dụng CAB | 1. Mở màn hình Đặt chuyến<br>

<br>2. Nhập điểm đón hợp lệ<br>

<br>3. Nhập điểm đến hợp lệ<br>

<br>4. Chọn loại xe khả dụng<br>

<br>5. Bấm Xác nhận đặt chuyến | Điểm đón: "123 Lê Lợi, Q.1"<br>

<br>Điểm đến: "Landmark 81, Bình Thạnh"<br>

<br>Loại xe: "4 chỗ" | Hệ thống tạo chuyến xe mới thành công, hiển thị mã chuyến đi và chuyển sang trạng thái tìm tài xế | High |
| **TC-BOOK-002** *(TC01)* | Khách hàng đặt chuyến xe | Đặt chuyến khi để trống điểm đón | Khách hàng đang ở màn hình Đặt chuyến | 1. Để trống trường điểm đón<br>

<br>2. Nhập điểm đến<br>

<br>3. Chọn loại xe<br>

<br>4. Bấm Xác nhận đặt chuyến | Điểm đón: trống<br>

<br>Điểm đến: "Landmark 81"<br>

<br>Loại xe: "4 chỗ" | Hệ thống chặn yêu cầu, hiển thị thông báo lỗi: "Vui lòng nhập điểm đón" | High |
| **TC-BOOK-003** *(TC02)* | Khách hàng đặt chuyến xe | Đặt chuyến với điểm đón trùng với điểm đến | Khách hàng đang ở màn hình Đặt chuyến | 1. Nhập điểm đón<br>

<br>2. Nhập điểm đến trùng hoàn toàn điểm đón<br>

<br>3. Chọn loại xe<br>

<br>4. Bấm Xác nhận | Điểm đón: "123 Lê Lợi, Q.1"<br>

<br>Điểm đến: "123 Lê Lợi, Q.1"<br>

<br>Loại xe: "4 chỗ" | Hệ thống cảnh báo: "Điểm đến không được trùng với điểm đón", không tạo chuyến | Medium |
| **TC-BOOK-004** *(TC03)* | Khách hàng đặt chuyến xe | Đặt chuyến khi chưa chọn loại xe | Khách hàng đã nhập điểm đón và điểm đến | 1. Nhập điểm đón và điểm đến hợp lệ<br>

<br>2. Bỏ qua bước chọn loại xe<br>

<br>3. Bấm Xác nhận đặt chuyến | Điểm đón: "123 Lê Lợi"<br>

<br>Điểm đến: "Landmark 81"<br>

<br>Loại xe: Không chọn | Hệ thống chặn thao tác và yêu cầu: "Vui lòng chọn loại xe mong muốn" | High |
| **TC-BOOK-005** *(TC04)* | Khách hàng đặt chuyến xe | Hủy thao tác tại bước xác nhận đặt xe | Khách hàng đã nhập đủ thông tin chuyến đi | 1. Nhập thông tin chuyến đi<br>

<br>2. Tại pop-up xác nhận giá và hành trình, chọn "Hủy / Quay lại" | Thông tin lộ trình hợp lệ | Hệ thống không ghi nhận chuyến đi, giữ nguyên màn hình chọn tuyến đường | Low |
| **TC-DISP-001** *(TC05)* | Tìm và phân công tài xế | Hệ thống chỉ gửi yêu cầu cho tài xế đang ở trạng thái sẵn sàng (Active) | Có yêu cầu đặt xe mới; tài xế A đang "Sẵn sàng", tài xế B "Đang bận" | 1. Hệ thống tiếp nhận chuyến đi<br>

<br>2. Quét tài xế khả dụng xung quanh điểm đón | Tài xế A: Status="Available"<br>

<br>Tài xế B: Status="Busy" | Hệ thống chỉ gửi cuốc xe cho tài xế A; tài xế B không nhận được thông báo | High |
| **TC-DISP-002** *(TC06)* | Tìm và phân công tài xế | Ưu tiên gửi cuốc cho tài xế phù hợp ở cự ly gần nhất | Có nhiều tài xế cùng trạng thái sẵn sàng trong khu vực | 1. Tiếp nhận chuyến<br>

<br>2. Tính toán khoảng cách GPS của các tài xế khả dụng | Tài xế A: cách 500m<br>

<br>Tài xế B: cách 2km | Hệ thống tự động điều phối gửi yêu cầu chuyến đi tới tài xế A đầu tiên | High |
| **TC-DISP-003** *(TC07)* | Tìm và phân công tài xế | Tài xế đồng ý tiếp nhận chuyến xe | Yêu cầu chuyến đã được gửi đến thiết bị tài xế | 1. Tài xế nhận pop-up cuốc xe mới<br>

<br>2. Nhấn nút "Chấp nhận" trong vòng 30 giây | Thời gian phản hồi: 10 giây | Trạng thái chuyến chuyển sang "Tài xế đã nhận cuốc"; gửi thông tin tài xế cho khách hàng | High |
| **TC-DISP-004** *(TC08)* | Tìm và phân công tài xế | Tự động chuyển tài xế khác khi tài xế ban đầu từ chối hoặc hết hạn nhận | Yêu cầu đã gửi tới tài xế A | 1. Tài xế A bấm "Từ chối" hoặc để hết timeout 30s<br>

<br>2. Hệ thống kiểm tra tài xế tiếp theo | Timeout: 30s không phản hồi | Hệ thống hủy yêu cầu với tài xế A và tự động chuyển cuốc sang tài xế B gần kế tiếp | High |
| **TC-TRIP-001** *(TC09)* | Thực hiện hành trình chuyến đi | Tài xế cập nhật trạng thái theo đúng thứ tự quy trình | Tài xế đã nhận cuốc xe | 1. Bấm "Đã đến điểm đón"<br>

<br>2. Khách lên xe, bấm "Bắt đầu di chuyển"<br>

<br>3. Tới nơi, bấm "Hoàn thành" | Trình tự thao tác chuẩn | Hệ thống cập nhật trạng thái theo đúng luồng: Arrived → In Progress → Completed | High |
| **TC-TRIP-002** *(TC09)* | Thực hiện hành trình chuyến đi | Chặn cập nhật trạng thái nhảy cóc (bỏ bước) | Tài xế mới nhấn nhận cuốc xe | 1. Tài xế cố tình gửi request kết thúc chuyến ngay lập tức khi chưa bấm đón khách | Action: Hoàn thành chuyến | Hệ thống báo lỗi logic: "Không thể hoàn thành chuyến khi chưa bắt đầu di chuyển" | Medium |
| **TC-TRIP-003** *(TC10)* | Theo dõi chuyến đi | Cập nhật và hiển thị vị trí thực tế của tài xế | Chuyến xe đang trong trạng thái "Đến đón" hoặc "Đang di chuyển" | 1. Tài xế di chuyển trên đường<br>

<br>2. Khách hàng mở màn hình theo dõi bản đồ | Tọa độ GPS tài xế thay đổi theo chu kỳ (3-5 giây) | Icon xe trên màn hình khách hàng di chuyển theo đúng vị trí tọa độ GPS gửi về | High |
| **TC-TRIP-004** *(TC11)* | Hoàn thành chuyến đi | Hoàn thành chuyến đi và chốt thông số thực tế | Xe đã đến đúng điểm đến | 1. Tài xế chọn "Hoàn tất chuyến đi"<br>

<br>2. Hệ thống ghi nhận thời gian kết thúc | Thời gian kết thúc = thời điểm bấm nút | Chuyến xe chuyển trạng thái "Completed", lưu trữ lịch sử lộ trình và kích hoạt tính cước | High |
| **TC-PAY-001** *(TC12)* | Tính cước và thanh toán | Tính toán cước phí chính xác theo quãng đường và biểu phí dịch vụ | Chuyến xe đã bấm hoàn tất | 1. Hệ thống ghi nhận quãng đường thực tế<br>

<br>2. Áp công thức tính cước | Quãng đường: 10 km<br>

<br>Đơn giá: 12.000 VNĐ/km | Cước hiển thị chuẩn xác: 120.000 VNĐ; tạo biên lai thanh toán tương ứng | High |
| **TC-PAY-002** *(TC13)* | Tính cước và thanh toán | Chọn phương thức thanh toán tiền mặt (Cash) | Màn hình hiển thị số tiền thanh toán cuối | 1. Khách hàng/Tài xế chọn "Tiền mặt"<br>

<br>2. Tài xế xác nhận "Đã thu tiền" | Phương thức: CASH<br>

<br>Số tiền: 120.000 VNĐ | Hệ thống ghi nhận hóa đơn đã thanh toán xong bằng tiền mặt | High |
| **TC-PAY-003** *(TC14)* | Tính cước và thanh toán | Thanh toán qua cổng điện tử thành công | Khách liên kết thẻ/ví điện tử có đủ số dư | 1. Chọn thanh toán "Ví điện tử / Cổng thanh toán"<br>

<br>2. Hệ thống gửi trừ tiền qua cổng đối tác | Số dư ví > Số tiền cần trả | Cổng trả về mã thành công (Code 200), chuyến xe đánh dấu "Đã thanh toán" | High |
| **TC-PAY-004** *(TC14)* | Tính cước và thanh toán | Xử lý khi cổng thanh toán điện tử trả về thất bại | Tài khoản/thẻ liên kết không đủ số dư hoặc lỗi kết nối cổng | 1. Khách hàng tiến hành thanh toán điện tử<br>

<br>2. Cổng thanh toán trả mã thất bại (Insufficient funds) | Mã phản hồi lỗi từ bên thứ 3 | Hệ thống báo "Thanh toán thất bại", cho phép khách hàng đổi sang tiền mặt | High |
| **TC-NOTI-001** *(TC15)* | Quản lý thông báo | Gửi thông báo đẩy khi tài xế đã đến điểm đón | Tài xế bấm cập nhật "Đã đến điểm đón" | 1. Tài xế xác nhận đã tới nơi<br>

<br>2. Kiểm tra push notification trên máy khách | Sự kiện: Driver Arrived | Thiết bị khách nhận push/SMS: "Tài xế đã đến điểm đón, vui lòng ra xe" | Medium |
| **TC-NOTI-002** *(TC16)* | Quản lý thông báo | Gửi thông báo xác nhận thanh toán thành công | Giao dịch thanh toán được ghi nhận hoàn tất | 1. Thanh toán chuyến xe thành công<br>

<br>2. Kiểm tra chuông thông báo trên máy khách và tài xế | Sự kiện: Payment Success | Cả khách hàng và tài xế đều nhận được thông báo chi tiết số tiền đã thanh toán | Medium |
| **TC-RATE-001** *(TC17)* | Đánh giá tài xế | Khách hàng đánh giá số sao và nhận xét cho chuyến đi đã hoàn thành | Chuyến đi ở trạng thái "Completed" | 1. Khách mở thông tin chuyến đi đã hoàn thành<br>

<br>2. Chọn đánh giá 5 sao<br>

<br>3. Nhập phản hồi "Lái xe an toàn"<br>

<br>4. Bấm Gửi | Rating: 5 sao<br>

<br>Comment: "Lái xe an toàn" | Đánh giá được lưu thành công, điểm đánh giá trung bình của tài xế được cập nhật lại | Medium |
| **TC-RATE-002** *(TC17)* | Đánh giá tài xế | Chặn quyền đánh giá khi chuyến xe chưa hoàn thành hoặc bị hủy | Chuyến xe đang ở trạng thái "In Progress" hoặc "Cancelled" | 1. Khách truy cập vào chi tiết chuyến chưa hoàn tất<br>

<br>2. Kiểm tra nút/chức năng đánh giá | Status = "In Progress" | Nút đánh giá bị ẩn/vô hiệu hóa; hệ thống từ chối cho phép gửi form đánh giá | Low |
| **TC-CUST-001** *(TC18)* | Quản trị thông tin khách hàng | Nhân viên vận hành tìm kiếm và chỉnh sửa thông tin khách hàng | Nhân viên đăng nhập tài khoản có quyền Quản lý khách hàng | 1. Vào menu Quản lý khách hàng<br>

<br>2. Nhập số điện thoại cần tìm<br>

<br>3. Chỉnh sửa địa chỉ/họ tên<br>

<br>4. Nhấn Lưu | Phone: "0901234567"<br>

<br>Action: Edit Profile | Dữ liệu khách hàng được cập nhật chính xác trong cơ sở dữ liệu | Medium |
| **TC-DRIV-001** *(TC19)* | Quản trị hồ sơ tài xế | Nhân viên vận hành phê duyệt thông tin hồ sơ phương tiện tài xế | Tài xế nộp hồ sơ xe mới | 1. Vào danh sách Chờ duyệt tài xế<br>

<br>2. Kiểm tra biển số xe, loại xe<br>

<br>3. Nhấn "Phê duyệt" | Biển số: 51F-123.45<br>

<br>Loại: 4 chỗ | Hồ sơ tài xế chuyển sang trạng thái "Đã duyệt/Hoạt động", cho phép nhận cuốc | High |
| **TC-DRIV-002** *(TC20)* | Quản trị hồ sơ tài xế | Cập nhật khóa trạng thái tài xế vi phạm | Nhân viên có thẩm quyền vận hành | 1. Chọn tài xế cần khóa<br>

<br>2. Đổi trạng thái từ Active sang Locked<br>

<br>3. Xác nhận lưu | MaTX: 102<br>

<br>Status mới: "Locked" | Trạng thái tài xế chuyển thành Locked; tài xế bị đăng xuất và không thể nhận cuốc xe | High |
| **TC-OPS-001** *(TC21)* | Quản lý vận hành | Nhân viên vận hành theo dõi trực quan các chuyến xe đang diễn ra | Hệ thống đang có các chuyến xe hoạt động | 1. Đăng nhập trang Admin Vận hành<br>

<br>2. Truy cập màn hình Monitor chuyến | Trạng thái lọc: "In Progress" | Danh sách các chuyến đang chạy hiển thị đầy đủ thông tin: Mã cuốc, tài xế, khách, lộ trình | Medium |
| **TC-OPS-002** *(TC22)* | Quản lý vận hành & Xử lý sự cố | Điều phối viên xử lý thủ công hủy/hỗ trợ chuyến xe gặp sự cố hỏng hóc | Chuyến xe đang chạy nhưng tài xế báo hỏng xe giữa đường | 1. Tiếp nhận báo cáo sự cố từ tài xế<br>

<br>2. Mở chuyến xe lỗi trên màn hình quản trị<br>

<br>3. Chọn "Hủy do sự cố kỹ thuật"<br>

<br>4. Tạo cuốc điều phối xe mới thay thế | TripID: 9999<br>

<br>Lý do: "Hỏng phương tiện" | Chuyến cũ kết thúc theo diện sự cố (không phạt khách/tài xế); cuốc xe mới được kích hoạt | High |
| **TC-REP-001** *(TC23)* | Báo cáo và thống kê | Xuất báo cáo tổng hợp doanh thu và số lượng chuyến đi theo ngày | Nhân viên quản lý có quyền xem báo cáo | 1. Vào mục Báo cáo & Thống kê<br>

<br>2. Chọn khoảng ngày từ 01/10 đến 07/10<br>

<br>3. Nhấn "Xem báo cáo" / "Xuất Excel" | Date Range: 01/10/2026 - 07/10/2026 | Hệ thống kết xuất chính xác: Tổng số chuyến thành công, số chuyến hủy, tổng doanh thu | High |

Bạn có thể xuất bảng dữ liệu này trực tiếp vào file Excel nếu cần tích hợp chung vào dự án. Bạn có muốn bổ sung thêm các ca kiểm thử biên (Boundary Value) hay kịch bản kiểm thử bảo mật API cụ thể nào nữa không?
