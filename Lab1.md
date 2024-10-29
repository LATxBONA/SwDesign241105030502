# PHÂN TÍCH KIẾN TRÚC, CƠ CHẾ, CA SỬ DỤNG
**1. Phân tích kiến trúc**
* Đề xuất kiến trúc MVC cho hệ thống Payroll:
  - Model: Chứa dữ liệu và logic nghiệp vụ
  - View: Giao diện người dùng
  - Controller: Điều khiển luồng xử lý, kết nối Model và View
* Giải thích
  - Kiến trúc MVC phù hợp với hệ thống Payroll vì:
    - Tách biệt rõ ràng giữa dữ liệu, giao diện và xử lý
    - Dễ dàng bảo trì và mở rộng
    - Hỗ trợ tái sử dụng code và phát triển song song
  - Ý nghĩa từng thành phần:
    - Model: Chứa các đối tượng dữ liệu như Employee, Timecard, Payment và logic nghiệp vụ
    - View: Chứa các form, màn hình hiển thị cho người dùng
    - Controller: Xử lý yêu cầu từ người dùng, tương tác với Model và cập nhật View
   
* Biểu đồ UML Package cho Hệ thống Payroll

![Package MVC](https://www.planttext.com/api/plantuml/png/R95DQiCm44RtEiNW0-G0MHI32La5kZ2bMo4FiR0ikRASO4eNeSiUeuj2m1UmA5da93f1hr3v1zV5NWdUz_5c6FtOMrWQgasL2r9Gbj4Zma4bAE2L0311on9sUI5KZJY1cEV8g4ucy4Zh7AKXRsIIF74yhpWwlF3yWwEhPpDVfAJHIWZKAzQ_SE5UYSO9iyJFwVVTR1xcWxOGx9rjEDJtQmNCjLzLG6PvLn-EvPlFlWdY_Wr27JaBo10iZR5sxIUSdBr0vjgRWPVAWuMttyVN8zSs1SZKFmPIxkox19Cw-n6G46NI_Til0000__y30000)

**2. Cơ chế phân tích**
* Cơ chế bảo mật (Security Mechanism)
  - Xác thực người dùng (Authentication)
  - Phân quyền truy cập (Authorization)
  - Mã hóa dữ liệu nhạy cảm (Data Encryption)
  - Ghi nhật ký hệ thống (System Logging)
* Cơ chế lưu trữ (Persistence Mechanism)
  - Lưu trữ dữ liệu vào cơ sở dữ liệu
  - Truy xuất dữ liệu từ cơ sở dữ liệu
  - Đồng bộ hóa dữ liệu (Data Synchronization)
  - Sao lưu và phục hồi dữ liệu (Backup and Recovery)
 
* Cơ chế xử lý nghiệp vụ (Business Logic Mechanism)
  - Tính toán lương (Salary Calculation)
  - Quản lý thời gian làm việc (Time Management)
  - Xử lý các quy tắc nghiệp vụ (Business Rules Processing)
  - Quản lý chu kỳ thanh toán (Payment Cycle Management)
 
* Cơ chế giao tiếp (Communication Mechanism)
  - Gửi thông báo nội bộ (Internal Notifications)
  - Kết nối với hệ thống ngân hàng (Bank System Integration)
  - Tương tác với hệ thống bên ngoài (External System Interaction)
  - Gửi email tự động (Automated Email Sending)
 
* Cơ chế báo cáo (Reporting Mechanism)
  - Tạo báo cáo động (Dynamic Report Generation)
  - Xuất báo cáo đa định dạng (Multi-format Report Export)
  - Lập lịch báo cáo tự động (Automated Report Scheduling)
  - Trực quan hóa dữ liệu (Data Visualization)
 
* Cơ chế xử lý lỗi và ngoại lệ (Error Handling and Exception Mechanism)
  - Ghi nhận lỗi (Error Logging)
  - Xử lý ngoại lệ (Exception Handling)
  - Thông báo lỗi cho người dùng (User Error Notification)
  - Cơ chế khôi phục sau lỗi (Error Recovery)
 
* Cơ chế quản lý giao diện người dùng (UI Management Mechanism)
  - Tùy chỉnh giao diện (UI Customization)
  - Đa ngôn ngữ (Internationalization)
  - Hỗ trợ đa nền tảng (Cross-platform Support)
  - Quản lý trạng thái giao diện (UI State Management)
 
* Cơ chế quản lý cấu hình (Configuration Management Mechanism)
  - Lưu trữ cấu hình hệ thống (System Configuration Storage)
  - Cập nhật cấu hình động (Dynamic Configuration Update)
  - Quản lý phiên bản (Version Control)
  - Tùy chỉnh cấu hình theo người dùng (User-specific Configuration)

 **3. Phân tích ca sử dụng Payment**
* **Xác định các lớp phân tích:**
   - Boundary (View):
     - PaymentForm: Giao diện người dùng để nhập thông tin thanh toán
     - PaymentReport: Hiển thị báo cáo thanh toán
     - BankSystemInterface: Giao diện kết nối với hệ thống ngân hàng
    - Control (Controller):
      - PaymentController: Điều khiển luồng xử lý thanh toán
      - PaymentCalculator: Tính toán các khoản thanh toán
      - PaymentValidator: Kiểm tra tính hợp lệ của thông tin thanh toán
    - Entity (Model):
      - Employee: Thông tin nhân viên
      - Payment: Thông tin thanh toán
      - BankAccount: Thông tin tài khoản ngân hàng
* **Biểu đồ sequence:**

  ![UML Sequence Payment](https://www.planttext.com/api/plantuml/png/X9F1JiGW48RlF0N7RkA-00Upgz5aRsOtyJxIgI5I832OzDay-4Y-WjIMsbgsdiem_D_mpz2lZyz38F0KMyr0alNy2ReM3JrQtpANCaeg1uRo_hqrvAtMw1VPXzPfso6M9C-WLGs9NUI1bb5Vooxsxi2yNRf0s9uCeMz05ikTqLbFZCsCyFtj-lw2AwD80U6Ogd0qSQftR7MyPsINWhyYvU1a6lk_z6yl17yVbhdw4fE2RT1ltmINutfjP86P53DC4dkSAITKVMnjD7Jb4eLH24uUJ6ZGPvORlZVy9Pq-IZdm2bA-Byyd0yyOegRDTWWUtQoP5mAAeLe2jXiwF9j-iWPz8WrnDh6jxT-OuBKAJaCtyVgQbV_1x1WxeAdxl-mR003__mC0)

* **Nhiệm vụ của từng lớp phân tích:**
  - Boundary:
    - PaymentForm: Nhận input từ người dùng và hiển thị kết quả thanh toán
    - PaymentReport: Tạo và hiển thị báo cáo thanh toán
    - BankSystemInterface: Xử lý giao tiếp với hệ thống ngân hàng
   
  - Control:
    - PaymentController: Điều phối quá trình thanh toán, xử lý logic nghiệp vụ
    - PaymentCalculator: Thực hiện các tính toán liên quan đến thanh toán
    - PaymentValidator: Kiểm tra tính hợp lệ của dữ liệu thanh toán
   
  - Entity:
    - Employee: Lưu trữ và cung cấp thông tin nhân viên
    - Payment: Đại diện cho một giao dịch thanh toán
    - BankAccount: Lưu trữ thông tin tài khoản ngân hàng
   
* **Một số thuộc tính và phương thức của các lớp phân tích**
- Thuộc tính chính của các lớp:
  - PaymentForm:
    - Không có thuộc tính đặc biệt, chủ yếu là các phương thức để tương tác với người dùng.
  - PaymentReport:
    - Có thể có thuộc tính để lưu trữ thông tin báo cáo tạm thời.
  - BankSystemInterface:
    - Có thể có thuộc tính để lưu trữ thông tin kết nối với ngân hàng.
  - PaymentController:
    - currentPayment: Payment - lưu trữ thông tin về giao dịch thanh toán hiện tại.
  - PaymentCalculator:
    - Không có thuộc tính đặc biệt, chủ yếu là các phương thức tính toán.
  - PaymentValidator:
    - Có thể có các thuộc tính để lưu trữ các quy tắc xác thực.
  - Employee:
    - employeeId: int - mã số nhân viên
    - name: String - tên nhân viên
    - employeeType: EmployeeType - loại nhân viên (enum)
    - salary: double - lương cơ bản
  - Payment:
    - paymentId: int - mã số giao dịch thanh toán
    - employeeId: int - mã số nhân viên được thanh toán
    - amount: double - số tiền thanh toán
    - date: Date - ngày thanh toán
    - status: PaymentStatus - trạng thái thanh toán (enum)
  - BankAccount:
    - accountId: int - mã số tài khoản
    - accountNumber: String - số tài khoản
    - bankName: String - tên ngân hàng
    - accountType: String - loại tài khoản
- Quan hệ giữa các lớp:
  - PaymentController có quan hệ sử dụng (uses) với:
    - PaymentForm: để lấy input và hiển thị output
    - PaymentReport: để tạo báo cáo thanh toán
    - BankSystemInterface: để thực hiện giao dịch với ngân hàng
    - PaymentCalculator: để tính toán số tiền thanh toán
    - PaymentValidator: để xác thực thông tin thanh toán
    - Employee: để lấy thông tin nhân viên
    - Payment: để tạo và cập nhật thông tin thanh toán
  - Employee có quan hệ kết hợp (association) 1-1 với BankAccount:
    - Mỗi nhân viên có một tài khoản ngân hàng
  - Payment có quan hệ phụ thuộc (dependency) với BankAccount:
    - Payment sử dụng thông tin từ BankAccount để thực hiện giao dịch
  - PaymentCalculator có quan hệ phụ thuộc với Employee:
    - PaymentCalculator sử dụng thông tin từ Employee để tính toán lương
  - PaymentValidator có quan hệ phụ thuộc với Employee và BankAccount:
    - PaymentValidator sử dụng thông tin từ cả Employee và BankAccount để xác thực
  - PaymentForm và PaymentReport có quan hệ phụ thuộc với Payment:
    - Các lớp này sử dụng thông tin từ Payment để hiển thị

* **Biểu đồ lớp**

![UML class payment](https://www.planttext.com/api/plantuml/png/X5PBRjim4Dth54GsaHTUTEj5aVXJD9iqY8tkQMba4-578AcqGj6JTT4ZzGebnOz9MNAyCA6PHywRcSUH_ltv-w0qbhfZjBX7Qz7n6iiURIXM2bHHsHMzu9u1rr-4PEXNWUol9ggbk4yyvS9vJg1thAMY1tYgoyKA4QwZn-Ete36XodfpYmEgi_Yn4RmXac5D10z7-w0xAOKi6IY5Jx12Uoq9FosAtqLEznLQ8VKquNt7cCcpRDrZfE43jUP4lp_4Xf_soTiQOPbDX5vZ_hRlbGRsn3N81bSG211EDC4Q3X9prO2SYssg521xZNKtL2ctEE0Pyvh6urnH1Yhto1HFIq6ds-YT5AIdjgmwAOtZPKGer49KfjJULaBixT1PJ_eTKrARv0BAK3uAGG5pvwymhJfw0JmoexG1LelkIC6XkZOv8oJlA7AXITF730m9q51UDttZ0ucGt2Nq6YlOOshR7f9OeI3L4PEuQGjrLraDgZ7P2Fds3b8J1hE0Wz2O9fNne37rxww62VCpL6-1u8wI4paIIlGC_QpUetxuSkDX2GJczbWDFrQLs-7M5KgCoRv1R3kk3QcHrWAn8B6HR7nJCOltDuST-ZR9pZuvlnhwbzLvURnGotXUZQDawenC4_BxIfHfnTI46FSjfEYHMOQJQUTjS3ORUOMsvjydEgW_HatlVIKXlMafTtzd9ZTVnik7GpWRPxwQ8KklY3mXPtlks15atb3RdEUhDliDhik98semw6-iKSFUknBskSM9yXNeyEfGPzAgudhoBPUVqzVQROIR-ZEOYP5_-xJBYBgDY_DW1XOqVFkK8jx4kqztWyEkwJK9CWx917ln0BostmN_0G00__y30000)
  > Giải thích
  a. Các lớp Boundary:
  - PaymentForm
    - Mục đích: Giao diện người dùng để nhập và hiển thị thông tin thanh toán
    - Trách nhiệm:
      - Hiển thị form nhập liệu
      - Thu thập thông tin thanh toán
      - Hiển thị thông báo xác nhận/lỗi
    - Thuộc tính và phương thức chính:
      - displayPaymentForm()
      - getEmployeeId()
      - showConfirmation()
  - PaymentReport
    - Mục đích: Hiển thị báo cáo thanh toán
    - Trách nhiệm:
      - Hiển thị thông tin thanh toán
      - In và xuất báo cáo
    - Thuộc tính và phương thức chính:
      - displayPaymentSummary()
      - printReport()
      - exportReport()
   
  - BankSystemInterface
    - Mục đích: Giao diện kết nối với hệ thống ngân hàng
    - Trách nhiệm:
      - Xử lý giao dịch với ngân hàng
      - Theo dõi trạng thái giao dịch
    - Thuộc tính và phương thức chính:
      - initiateTransfer()
      - getTransferStatus()
     
  b. Các lớp Control:
  - PaymentController
    - Mục đích: Điều khiển luồng xử lý thanh toán
    - Trách nhiệm:
      - Điều phối quy trình thanh toán
      - Xử lý logic nghiệp vụ
    - Thuộc tính và phương thức chính:
      - processPayment()
      - validatePayment()
      - calculatePaymentAmount()
  - PaymentCalculator
    - Mục đích:  Tính toán các khoản thanh toán
    - Trách nhiệm:
      - Tính lương cơ bản
      - Tính các khoản khấu trừ
      - Tính tổng thanh toán
    - Thuộc tính và phương thức chính:
      - calculateBaseSalary()
      - calculateDeductions()
      - calculateTotalPayment()
  - PaymentValidator
    - Mục đích: Kiểm tra tính hợp lệ của thanh toán
    - Trách nhiệm:
      - Xác thực thông tin nhân viên
      - Kiểm tra số tiền thanh toán
    - Thuộc tính và phương thức chính:
      - checkEmployeeEligibility()
      - validatePaymentAmount()
     
  c. Các lớp Entity:
  - Employee
    - Mục đích: Lưu trữ thông tin nhân viên
    - Thuộc tính chính:
      - employeeId
      - name
      - employeeType
      - salary
    - Phương thức chính:
      - getEmployeeDetails()
      - updatePaymentHistory()
      
  - Payment
    - Mục đích: Lưu trữ thông tin thanh toán
    - Thuộc tính chính:
      - paymentId
      - amount
      - date
      - status
    - Phương thức chính:
      - createPayment()
      - updateStatus()
      
  - BankAccount
    - Mục đích: Lưu trữ thông tin tài khoản ngân hàng
    - Thuộc tính chính:
      - accountNumber
      - bankName
      - accountType
    - Phương thức chính:
      - validateAccount()
      - getAccountDetails()

**4. Phân tích ca sử dụng Maintain Timecard**
  
* **Xác định các lớp phân tích:**
  - Boundary (View):
    - TimecardForm: Giao diện người dùng để nhập thông tin thời gian làm việc.
    - TimecardReport: Hiển thị báo cáo thời gian làm việc.
    - TimecardValidationMessage: Hiển thị thông báo xác thực thông tin thời gian.
  - Control (Controller):
    - TimecardController: Điều khiển luồng xử lý thông tin thời gian làm việc.
    - TimecardCalculator: Tính toán tổng số giờ làm việc.
    - TimecardValidator: Kiểm tra tính hợp lệ của thông tin thời gian làm việc.
  - Entity (Model):
    - Employee: Thông tin nhân viên.
    - Timecard: Thông tin thời gian làm việc.
    - Project: Thông tin dự án mà nhân viên làm việc.

* **Biểu đồ sequence:**

![UML Squeren Maintain Timecard](https://www.planttext.com/api/plantuml/png/b5HBJiCm4Dtx55x2WWjaWIe1XGqIAbNtWpDj3PFOyWVKix7WI5o1QHFd0mvjlRBVlFV6Cvxa-_DhvWEu42iIe89nygwoP7Q8mZAibRPG1xdK5IfmvTouAXkuCNLmXWXTDhm2qYMmVLuCf29DXaVWapElg4AMk41hN10YbI2lhaStBwInM5zSYY6u9oL18KljBS5kI63-jA6FBvKE2Rk501dxlqqgf7L6eVSfD53rhA6sws0XtvijPhGTQoWjfDgYUdimqVafRj-1v9wGl6AYgbQiJRr07udV0YZ8LOVAvwZsPQyZ2Sdh_vhvuWx7XHuNzSF4ydQFInE0KWD67XrxigRGQK_8tenW8JTOe-F4pVbNqWQScWntYDwt1kK9ITjHt9eFZg-rgmwzvgH87eVTduEcCnrxzIE_6spsyu1rAOv_Gyq4C7t6VFw__0000F__0m00)
* **Nhiệm vụ của từng lớp phân tích:**
  - Boundary:
    - TimecardForm: Nhận input từ người dùng và hiển thị kết quả thời gian làm việc.
    - TimecardReport: Tạo và hiển thị báo cáo thời gian làm việc.
    - TimecardValidationMessage: Hiển thị thông báo xác thực thông tin thời gian.

  - Control:
    - TimecardController: Điều phối quá trình nhập và xử lý thông tin thời gian làm việc, xử lý logic nghiệp vụ.
    - TimecardCalculator: Thực hiện các tính toán liên quan đến tổng số giờ làm việc.
    - TimecardValidator: Kiểm tra tính hợp lệ của dữ liệu thời gian làm việc.

  - Entity:
    - Employee: Lưu trữ và cung cấp thông tin nhân viên.
    - Timecard: Đại diện cho thông tin thời gian làm việc của nhân viên.
    - Project: Lưu trữ thông tin về dự án mà nhân viên tham gia.

* **Một số thuộc tính và phương thức của các lớp phân tích**
  - Thuộc tính chính của các lớp:
    - TimecardForm:
      - Không có thuộc tính đặc biệt, chủ yếu là các phương thức để tương tác với người dùng.
    - TimecardReport:
      - Có thể có thuộc tính để lưu trữ thông tin báo cáo tạm thời.
    - TimecardValidationMessage:
      - Có thể có thuộc tính để lưu trữ thông tin xác thực.
    - TimecardController:
      - currentTimecard: Timecard - lưu trữ thông tin về thời gian làm việc hiện tại.
    - TimecardCalculator:
      - Không có thuộc tính đặc biệt, chủ yếu là các phương thức tính toán.
    - TimecardValidator:
      - Có thể có các thuộc tính để lưu trữ các quy tắc xác thực.
    - Employee:
      - employeeId: int - mã số nhân viên.
      - name: String - tên nhân viên.
      - employeeType: EmployeeType - loại nhân viên (enum).
    - Timecard:
      - timecardId: int - mã số thời gian làm việc.
      - employeeId: int - mã số nhân viên.
      - hoursWorked: double - số giờ làm việc.
      - projectId: int - mã số dự án.
      - date: Date - ngày làm việc.
    - Project:
      - projectId: int - mã số dự án.
      - projectName: String - tên dự án.

* **Quan hệ giữa các lớp:**
  - TimecardController có quan hệ sử dụng (uses) với:
    - TimecardForm: để lấy input và hiển thị output.
    - TimecardReport: để tạo báo cáo thời gian làm việc.
    - TimecardValidationMessage: để hiển thị thông báo xác thực.
    - TimecardCalculator: để tính toán tổng số giờ làm việc.
    - TimecardValidator: để xác thực thông tin thời gian làm việc.
    - Employee: để lấy thông tin nhân viên.
    - Timecard: để tạo và cập nhật thông tin thời gian làm việc.
    - Project: để lấy thông tin dự án.
  - Employee có quan hệ kết hợp (association) 1-1 với Timecard:
    - Mỗi nhân viên có một thời gian làm việc.
  - Timecard có quan hệ phụ thuộc (dependency) với Project:
    - Timecard sử dụng thông tin từ Project để xác định dự án làm việc.
  - TimecardCalculator có quan hệ phụ thuộc với Timecard:
    - TimecardCalculator sử dụng thông tin từ Timecard để tính toán tổng số giờ làm việc.
  - TimecardValidator có quan hệ phụ thuộc với Timecard và Employee:
    - TimecardValidator sử dụng thông tin từ cả Timecard và Employee để xác thực.
  - TimecardForm và TimecardReport có quan hệ phụ thuộc với Timecard:
    - Các lớp này sử dụng thông tin từ Timecard để hiển thị.

* **Biểu đồ lớp**

  ![UML class Maintain Timecard](https://www.planttext.com/api/plantuml/png/Z9J1JiCm38RlVOfe9pZqmBK7DCI6s0LDR88Zobgp1PAuSjAD2l5a77WaNe6qIxDsBOmUMiN-RNznd7v_VesDvMGB9QDKScFOLEKIIm3s7Z7tn0oyOPObJ6ZhhPehIDZ2aj3h8-6op9rhsbhL0iRMO1lh12mNqfoTXnmVaGTO2WKffom0M6_e0WnZRR0WyuZq2iwSOR6Iu3qvuGkajYlFk7Me4_VsY2c1MpG85TuMHNQ0c--p1BR1hDvurs-Hzqp0f2HoAr1t17MBvetcP8Tka9GdOImJ9fUyRFi2Vg_zitfh3J5ZPeExQzJFWXIlgFeRR_BUGuvaVwkwA9JYL1uLpXs-tGSUUU2jCXwvUZKTcIMK4YZqFIs8GDj6aGHjA8af6DCxoBrtowN8XixP3m6NQI5R_Yk5XQu1_KZr4Nq8KcZD8GjQBc-hmVmhmyEUgPLWY7A5A87hAZnSrD75YCLn_Gbt9s4RRgAmR4cQ2KxOpbqJyuGw6kXp75zsnonXXG5pIkgd8t6pfe4S-yc8mxR_Lw7LQ1ym1fsvtzSF0000__y30000)

