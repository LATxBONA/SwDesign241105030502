# Payroll System Analysis 

## 1. Create Administrative Report

### Xác định các lớp phân tích:

#### Boundary (View):
- **AdministrativeReportForm**: Giao diện người dùng để nhập thông tin báo cáo.
- **AdministrativeReportDisplay**: Hiển thị báo cáo đã tạo.

#### Control (Controller):
- **AdministrativeReportController**: Điều khiển luồng xử lý tạo báo cáo.
- **AdministrativeReportGenerator**: Tạo nội dung báo cáo.

#### Entity (Model):
- **Report**: Lưu trữ thông tin báo cáo.
- **Employee**: Thông tin nhân viên liên quan đến báo cáo.

### Biểu đồ sequence:
![Sequence Create Administrative Report](https://www.planttext.com/api/plantuml/png/Z58nRiCm3Dpr2exjq0zeA58qQVO0VO1Y4oq1MJGeke7VbY5FwXTgMNAI8JAwaSVZyIZgztpPH7MYG-UDQvG5FYEAEV8GMYSZlBKT1OegJka73zYpw0TBjyxOKkoz6qt3GONzGyvxhlbfsXfjZm6ddCLWKD8HChnakwxtF28Qatm3mCjhrRC52lsW83C2ZP2Ya3CrVathvjp25se1YzhJyqEzMqzDzRfe4ft3KgWeNlb9C4DssWdl-tAG2CixpOwNP8lgoCV_35YvieNupQTLhuMPXDAPBBG5oASm6mpjz0F_0000__y30000)

### Nhiệm vụ của từng lớp phân tích:
- **AdministrativeReportForm**: Nhận input từ người dùng để tạo báo cáo.
- **AdministrativeReportDisplay**: Hiển thị báo cáo đã tạo cho người dùng.
- **AdministrativeReportController**: Điều phối quá trình tạo báo cáo.
- **AdministrativeReportGenerator**: Tạo nội dung báo cáo dựa trên dữ liệu.
- **Report**: Lưu trữ thông tin về báo cáo.
- **Employee**: Cung cấp thông tin nhân viên cho báo cáo.

### Một số thuộc tính và phương thức của các lớp phân tích:
- **AdministrativeReportForm**:
  - Phương thức: `getReportCriteria()`, `displayReportForm()`
  
- **AdministrativeReportDisplay**:
  - Phương thức: `showReport()`
  
- **AdministrativeReportController**:
  - Phương thức: `createReport()`, `validateReportCriteria()`
  
- **AdministrativeReportGenerator**:
  - Phương thức: `generateReport()`
  
- **Report**:
  - Thuộc tính: `reportId`, `reportData`
  - Phương thức: `createReport()`
  
- **Employee**:
  - Thuộc tính: `employeeId`, `name`
  - Phương thức: `getEmployeeDetails()`

### Quan hệ giữa các lớp:
- **AdministrativeReportController** sử dụng **AdministrativeReportForm** và **AdministrativeReportDisplay** để nhận input và hiển thị báo cáo.
- **AdministrativeReportGenerator** phụ thuộc vào **Report** để tạo nội dung báo cáo.
- **Report** sử dụng thông tin từ **Employee** để tạo báo cáo.

### Biểu đồ lớp
![Class Create Administrative Report ](https://www.planttext.com/api/plantuml/png/d59B2i8m4Dtd55tgebUGYbLnwmq6CsWWdp8PAoAUp8L7yWgsJTCArXRCxhsPzvXvazVZcNa6uhFHug31-sGfZRBACm6h4lTOEEAD8vFSH5A_8t8WLwGOIS5i7WfI-KB3jLTKXRiOSSs381hxaxk4mfHmvIoJqnefQW-4mDYf6wu4hMJ7Vamxwhr5YnLsrE_R4FWzMc3QlfGQj9EVA0U6mG4xZxKfjBiYHXTiSVInOB3BFJRdoA2q3puJ0QNfukT9_zMsXnkKz_dLwi29DgcQYJk83AsiVjqR003__mC0)

> **Giải thích**
- **Actors:** User
- **Boundary Classes:**
  - AdministrativeReportForm: Giao diện để người dùng nhập tiêu chí báo cáo. Nó thu thập dữ liệu từ người dùng và gửi đến controller.
  - AdministrativeReportDisplay: Hiển thị báo cáo sau khi được tạo.
- **Control Classes:**
  - AdministrativeReportController: Điều phối quá trình tạo báo cáo. Nó nhận dữ liệu từ form và gọi generator để tạo báo cáo.
  - AdministrativeReportGenerator: Thực hiện logic tạo báo cáo dựa trên tiêu chí đã nhập.
- **Entity Classes:**
  - Report: Đại diện cho báo cáo được tạo.
  - Employee: Cung cấp thông tin nhân viên cần thiết cho báo cáo.

---

## 2. Create Employee Report

### Xác định các lớp phân tích:

#### Boundary (View):
- **EmployeeReportForm**: Giao diện người dùng để nhập thông tin báo cáo nhân viên.
- **EmployeeReportDisplay**: Hiển thị báo cáo nhân viên đã tạo.

#### Control (Controller):
- **EmployeeReportController**: Điều khiển luồng xử lý tạo báo cáo nhân viên.
- **EmployeeReportGenerator**: Tạo nội dung báo cáo nhân viên.

#### Entity (Model):
- **EmployeeReport**: Lưu trữ thông tin báo cáo nhân viên.
- **Employee**: Thông tin nhân viên.

### Biểu đồ sequence:
![Sequence Create Employee Report](https://www.planttext.com/api/plantuml/png/b98n3i8m34Ltdy8Z35mW0qAYm8x40K9hGQGqgHnNg6TZu4XSWHQY0Wa8iKN-_i_VSgxdooA8Pcbh2xeKpxWBnB3thQiqTxYg6-ixeYqrdcNjkVwc5IOqLdTGUYViRQ8k7rNRipytRCWHwpu0a1CZAJsj0Wmv4N4s_v1HeN5DAqXHGRvBMB8HOgCXj-IWPsI51v94ZAJ95BwvSkAuum2yF-cz8QEDZXoc-cteD-7L-BP7GQAD3V-CZ2TM68x-z6Dkx1qWmwKKLh6Gt0GMvAh-zzq0003__mC0)

### Nhiệm vụ của từng lớp phân tích:
- **EmployeeReportForm**: Nhận input từ người dùng để tạo báo cáo nhân viên.
- **EmployeeReportDisplay**: Hiển thị báo cáo nhân viên đã tạo cho người dùng.
- **EmployeeReportController**: Điều phối quá trình tạo báo cáo nhân viên.
- **EmployeeReportGenerator**: Tạo nội dung báo cáo nhân viên dựa trên dữ liệu.
- **EmployeeReport**: Lưu trữ thông tin về báo cáo nhân viên.
- **Employee**: Cung cấp thông tin nhân viên cho báo cáo.

### Một số thuộc tính và phương thức của các lớp phân tích:
- **EmployeeReportForm**:
  - Phương thức: `getEmployeeReportCriteria()`, `displayEmployeeReportForm()`
  
- **EmployeeReportDisplay**:
  - Phương thức: `showEmployeeReport()`
  
- **EmployeeReportController**:
  - Phương thức: `createEmployeeReport()`, `validateEmployeeReportCriteria()`
  
- **EmployeeReportGenerator**:
  - Phương thức: `generateEmployeeReport()`
  
- **EmployeeReport**:
  - Thuộc tính: `reportId`, `employeeData`
  - Phương thức: `createEmployeeReport()`
  
- **Employee**:
  - Thuộc tính: `employeeId`, `name`
  - Phương thức: `getEmployeeDetails()`

### Quan hệ giữa các lớp:
- **EmployeeReportController** sử dụng **EmployeeReportForm** và **EmployeeReportDisplay** để nhận input và hiển thị báo cáo.
- **EmployeeReportGenerator** phụ thuộc vào **EmployeeReport** để tạo nội dung báo cáo.
- **EmployeeReport** sử dụng thông tin từ **Employee** để tạo báo cáo.

### Biểu đồ lớp
![Class Create Employee Report](https://www.planttext.com/api/plantuml/png/b99D2i8m44RtEKMNkkWLH6XLt7g3eHaqa9yo6PKYdio5H_8ArgO1sxI2sOLvtnicazVZkVOCn6UZHQN1-snZQkqQn0FMZdZho6GtaNtE4NbOB4WnaeB5CW1I-Lf3anfQu2uc_MM8n1R-vAv3O3vQEClaj4QAwOeG69DyLxk0LZAfVaqmqwLtvzJTzZBSi6TAOFZPEx56NpH4emM3oJENoA2q3vxPwVDyDR6rV_X-2wF83YqIi9jAZD018TPePVkXtW000F__0m00)

> **Giải thích**
- **Actors:** User
- **Boundary Classes:**
  - EmployeeReportForm: Giao diện để người dùng nhập tiêu chí báo cáo nhân viên.
  - EmployeeReportDisplay: Hiển thị báo cáo nhân viên.
- **Control Classes:**
  - EmployeeReportController: Điều phối quá trình tạo báo cáo nhân viên. Nó nhận tiêu chí từ form và gọi generator để tạo báo cáo.
  - EmployeeReportGenerator: Thực hiện logic tạo báo cáo nhân viên.
- **Entity Classes:**
  - EmployeeReport: Đại diện cho báo cáo nhân viên.
  - Employee: Cung cấp thông tin nhân viên cần thiết cho báo cáo.


---

## 3. Login

### Xác định các lớp phân tích:

#### Boundary (View):
- **LoginForm**: Giao diện người dùng để nhập thông ```markdown
tin đăng nhập.
- **LoginMessage**: Hiển thị thông báo xác thực đăng nhập.

#### Control (Controller):
- **LoginController**: Điều khiển luồng xử lý đăng nhập.

#### Entity (Model):
- **User **: Thông tin người dùng.

### Biểu đồ sequence:
![Sequence Login](https://www.planttext.com/api/plantuml/png/R9112eCm44NtESKi5TeBk2Y2q5KBtNY0gHbi82QI6IkUhOiUgLUeGQiYtGJ-d_yVa_cytZaB1kaQgx0I7w1a2khkEwSn373njN5d7vgTTILch4bLtadmTZABITWHG4wC31DCnHS0ZgSLbu5nRIVGZIE73G4w3IqozpvejSIMpehEe2OfvrgI7gAypSKaLRjq1CHm1a-qHgDG4KZ7xT3o__ZsVndmm_TRvzUPvShNXbkB0zWuXMQ-JqvEZxVz0W00__y30000)

### Nhiệm vụ của từng lớp phân tích:
- **LoginForm**: Nhận input từ người dùng để thực hiện đăng nhập.
- **LoginMessage**: Hiển thị thông báo xác thực cho người dùng.
- **LoginController**: Điều phối quá trình đăng nhập và xác thực thông tin.
- **User **: Lưu trữ thông tin người dùng và trạng thái đăng nhập.

### Một số thuộc tính và phương thức của các lớp phân tích:
- **LoginForm**:
  - Phương thức: `getUsername()`, `getPassword()`, `displayLoginForm()`
  
- **LoginMessage**:
  - Phương thức: `showLoginMessage()`
  
- **LoginController**:
  - Phương thức: `processLogin()`, `validateCredentials()`
  
- **User **:
  - Thuộc tính: `userId`, `username`, `password`
  - Phương thức: `getUser Details()`

### Quan hệ giữa các lớp:
- **LoginController** sử dụng **LoginForm** để nhận input và **LoginMessage** để hiển thị thông báo.
- **LoginController** phụ thuộc vào **User ** để xác thực thông tin đăng nhập.

### Biểu đồ lớp
![Class Login](https://www.planttext.com/api/plantuml/png/T51B2i8m4Dtd55dgebUGGaKG5DnuWA4PQY1Doang4V5aBZoILp3Hfgs_h2PltdipR-xNMyuUoBUr4QK1PhbnbROhHxKy2nbVXNxFI1PgdCq7Q1UudIEL8AMvCN0Qr06_YAdb5fcXmkJA1zTDyIz-uQmdPmnIaZJaoa1-TjFO8nYjm6D1gD1w3OQdJd7nNfwreLwhiOw1Nh-cp_AMLoxHWqvsdojbsMAyrFzk7-ud8GuHELeLRly0003__mC0)

> **Giải thích**
- **Actors:** User
- **Boundary Classes:**
  - LoginForm: Giao diện để người dùng nhập tên người dùng và mật khẩu.
  - LoginMessage: Hiển thị thông báo xác thực đăng nhập (thành công hoặc thất bại).
- **Control Classes:**
  - LoginController: Xử lý logic xác thực thông tin đăng nhập. Nó kiểm tra tên người dùng và mật khẩu.
- **Entity Classes:**
  - User : Đại diện cho người dùng trong hệ thống.


---

## 4. Maintain Employee Information

### Xác định các lớp phân tích:

#### Boundary (View):
- **EmployeeForm**: Giao diện người dùng để nhập thông tin nhân viên.
- **EmployeeReport**: Hiển thị thông tin nhân viên.

#### Control (Controller):
- **EmployeeController**: Điều khiển luồng xử lý thông tin nhân viên.

#### Entity (Model):
- **Employee**: Thông tin nhân viên.


### Biểu đồ sequence:
![Sequence Maintain Employee Information](https://www.planttext.com/api/plantuml/png/X91B3i8m34JtFeMNiE02MQ1AV0w0n05COq6aDAuILwXdOy6Hk0AjGjiW5YndD6-iyUlnh99IrAxnGBLAn7FY21VfWgNOuw5flVJCHudDhtlYLg92BK6Z-DdUPUs78WxgT040ndf4t6o_gWswq7QA_F7GaXAKYP9O-WrUMITxFp2hDVocIjOWMJk9l-ayq62woNq-mqhEfuBDgP4RrncqBhMU-c9DHg3YO8TFlm400F__0m00)

### Nhiệm vụ của từng lớp phân tích:
- **EmployeeForm**: Nhận input từ người dùng để thêm, sửa hoặc xóa thông tin nhân viên.
- **EmployeeReport**: Hiển thị thông tin nhân viên cho người dùng.
- **EmployeeController**: Điều phối quá trình thêm, sửa hoặc xóa thông tin nhân viên.
- **Employee**: Lưu trữ thông tin nhân viên.

### Một số thuộc tính và phương thức của các lớp phân tích:
- **EmployeeForm**:
  - Phương thức: `getEmployeeData()`, `displayEmployeeForm()`
  
- **EmployeeReport**:
  - Phương thức: `showEmployeeDetails()`
  
- **EmployeeController**:
  - Phương thức: `addEmployee()`, `updateEmployee()`, `deleteEmployee()`
  
- **Employee**:
  - Thuộc tính: `employeeId`, `name`, `employeeType`
  - Phương thức: `getEmployeeDetails()`

### Quan hệ giữa các lớp:
- **EmployeeController** sử dụng **EmployeeForm** để nhận input và **EmployeeReport** để hiển thị thông tin.
- **EmployeeController** phụ thuộc vào **Employee** để thực hiện các thao tác thêm, sửa hoặc xóa thông tin.

### Biểu đồ lớp
![Class Maintain Employee Information](https://www.planttext.com/api/plantuml/png/X55B2i8m4Dtd55dg8bUGWXzmArvWS0OjJ9gGJ94Ydio5H_8ALj98Vz3PpNlp7eytdzUxY091QilgmX2ZtblFhY4wk63rG-dVN4aol0E1rJh1M4RFqFGLBVLK8wSJUHSaUyMRk__DIA3aE2VQkag2OwQGXO2OoHoWzWX2OnI9QO1Ep3jBGzr-nBHNO6d8d1jFqmxwiMS26xCPrBXqamfQkb85LTZ-wGi00F__0m00)

> **Giải thích**
- **Actors:** User
- **Boundary Classes:**
  - EmployeeForm: Giao diện để người dùng nhập và chỉnh sửa thông tin nhân viên.
  - EmployeeReport: Hiển thị thông tin chi tiết về nhân viên sau khi thêm hoặc chỉnh sửa.
- **Control Classes:**
  - EmployeeController: Điều phối quá trình thêm, sửa hoặc xóa thông tin nhân viên. Nó xử lý logic nghiệp vụ liên quan đến nhân viên.
- **Entity Classes:**
  - Employee: Đại diện cho thông tin nhân viên, bao gồm các thuộc tính như mã số, tên, và loại nhân viên.


---

## 5. Maintain Purchase Order

### Xác định các lớp phân tích:

#### Boundary (View):
- **PurchaseOrderForm**: Giao diện người dùng để nhập thông tin đơn hàng.
- **PurchaseOrderReport**: Hiển thị thông tin đơn hàng.

#### Control (Controller):
- **PurchaseOrderController**: Điều khiển luồng xử lý thông tin đơn hàng.

#### Entity (Model):
- **PurchaseOrder**: Thông tin đơn hàng.


### Biểu đồ sequence:
![Sequence Maintain Purchase Order](https://www.planttext.com/api/plantuml/png/b94n2W8n44Nxd69ABRn02bbGR1N10uoRu0PY4YOJPCzcuP6yWXiYI3PiOJl___V3p_lvwY8ZSRfRWJrxWalK9Au-EOKqmYbHFs3KHrAQ3fxk2z9P1qyiUk-OlAsrNJdQYQiT6vv5XSYL0B3PjdKIZ0k98Nm5y5a1XOoYCJU4NxE4c-PAsq-8rLei-1kK15IgklmHBkj8Y8D_r8_GZCR6EQhuCoPF8q6P62oEpGebBJhjrFI17m000F__0m00)

### Nhiệm vụ của từng lớp phân tích:
- **PurchaseOrderForm**: Nhận input từ người dùng để thêm, sửa hoặc xóa thông tin đơn hàng.
- **PurchaseOrderReport**: Hiển thị thông tin đơn hàng cho người dùng.
- **PurchaseOrderController**: Điều phối quá trình thêm, sửa hoặc xóa thông tin đơn hàng.
- **PurchaseOrder**: Lưu trữ thông tin đơn hàng.

### Một số thuộc tính và phương thức của các lớp phân tích:
- **PurchaseOrderForm**:
  - Phương thức: `getPurchaseOrderData()`, `displayPurchaseOrderForm()`
  
- **PurchaseOrderReport**:
  - Phương thức: `showPurchaseOrderDetails()`
  
- **PurchaseOrderController**:
  - Phương thức: `addPurchaseOrder()`, `updatePurchaseOrder()`, `deletePurchaseOrder()`
  
- **PurchaseOrder**:
  - Thuộc tính: `orderId`, `customerName`, `productDetails`, `orderDate`
  - Phương thức: `getOrderDetails()`

### Quan hệ giữa các lớp:
- **PurchaseOrderController** sử dụng **PurchaseOrderForm** để nhận input và **PurchaseOrderReport** để hiển thị thông tin.
- **PurchaseOrderController** phụ thuộc vào **PurchaseOrder** để thực hiện các thao tác thêm, sửa hoặc xóa thông tin đơn hàng.

### Biểu đồ lớp
![Class Maintain Purchase Order](https://www.planttext.com/api/plantuml/png/Z59B2i8m4Dtd55tgebUGWYAuKV46GsQmXRG9amaYuibSU2IlO4jQiQI5PZTvdvbvoUVrBhm0IwYDqWQypyw1TGcUJep4Uyjrzb1PTwua8sm70gjrnB3opi0zqRRuKqqPNyXPbi7Qb_OszYQ1olXP-TOsmjOOui4244UCORBW48Gc8IH3AJJTi6-JswuuO2nqy69huYFK56ySMmnQ-l7_96rOz8inNN5kkJpVf0-od1rJNivN1JNOVeKl0000__y30000)


> **Giải thích**
- **Actors:** User
- **Boundary Classes:**
  - PurchaseOrderForm: Giao diện để người dùng nhập dữ liệu đơn hàng mua.
  - PurchaseOrderReport: Hiển thị thông tin chi tiết về đơn hàng mua sau khi được thêm hoặc chỉnh sửa.
- **Control Classes:**
  - PurchaseOrderController: Điều phối quá trình thêm, sửa hoặc xóa đơn hàng mua. Nó xử lý logic nghiệp vụ liên quan đến đơn hàng.
- **Entity Classes:**
  - PurchaseOrder: Đại diện cho thông tin đơn hàng mua, bao gồm các thuộc tính như mã số đơn hàng, thông tin khách hàng, và sản phẩm đã mua.



---

## 6. Run Payroll

### Xác định các lớp phân tích:

#### Boundary (View):
- **PayrollReport**: Giao diện hiển thị báo cáo lương.
- **PayrollMessage**: Hiển thị thông báo kết quả chạy lương.

#### Control (Controller):
- **PayrollController**: Điều khiển luồng xử lý chạy lương.

#### Entity (Model):
- **Payroll**: Thông tin về lương của nhân viên.
- **Employee**: Thông tin nhân viên liên quan đến lương.


### Biểu đồ sequence:
![Sequence Run Payroll](https://www.planttext.com/api/plantuml/png/Z9512i8m44NtESKiTU45if22k1H4y00n7RGmJK8oGN8s5nx9AzYGj5KAulB_oSkV_BmUpoQmyXnx4agpzN0EwCN5HjCgd-2eahT49tJMyy8-O0ZgYa9RmuCUxLsHD5o4XZkUpezotpko2L68d0O0c-sIbU2ZgUvgBHRp3qY2LgGZASR_WF8U2U5cxr_Mp1MTcRoZXBOBZbG2LyRWIoM_Kcez4_jjpr7LcBFoMbDGNqjkqBJ3Dxq1003__mC0)

### Nhiệm vụ của từng lớp phân tích:
- **PayrollReport**: Hiển thị báo cáo lương cho người dùng.
- **PayrollMessage**: Hiển thị thông báo kết quả chạy lương.
- **PayrollController**: Điều phối quá trình chạy lương và tạo báo cáo.
- **Payroll**: Lưu trữ thông tin về lương của nhân viên.
- **Employee**: Cung cấp thông tin nhân viên cho quá trình chạy lương.

### Một số thuộc tính và phương thức của các lớp phân tích:
- **PayrollReport**:
  - Phương thức: `showPayrollReport()`, `printPayrollReport()`
  
- **PayrollMessage**:
  - Phương thức: `displayPayrollMessage()`
  
- **PayrollController**:
  - Phương thức: `runPayroll()`, `generatePayrollReport()`
  
- **Payroll**:
  - Thuộc tính: `payrollId`, `employeeId`, `totalPay`, `payDate`
  - Phương thức: `calculatePayroll()`
  
- **Employee**:
  - Thuộc tính: `employeeId`, `name`, `salary`
  - Phương thức: `getEmployeeDetails()`

### Quan hệ giữa các lớp:
- **PayrollController** sử dụng **PayrollReport** và **PayrollMessage** để hiển thị kết quả và thông báo.
- **PayrollController** phụ thuộc vào **Payroll** để tính toán lương và tạo báo cáo.
- **Payroll** sử dụng thông tin từ **Employee** để tính toán lương cho từng nhân viên.

### Biểu đồ lớp
![Class Run Payroll](https://www.planttext.com/api/plantuml/png/X9913e8m44Ntd8AbBhY28H4NBaoCDvZ014c6jkaCCSHuCXSUoIi8bb51WsoQwP___hJbVhsbBE2bgIdA2PZZFRJU4XtGMI_nEOhxZu_sD18Moo0uNncPAfTepDeXCvIeiA9YHz2EnH-sjJNIh-ZLwHipQ9fVea4FWlz660Y92-Ms22NMZcoBgBLO0Ueih-QiOuUa72Xlw1tr6R8PC9eonHge0oLX8F2jpYvgp52W8WxCx-CdoMhyBlCzmvNEDwdwtDCveXHDqVqB3m000F__0m00)

> **Giải thích**
- **Actors:** User
- **Boundary Classes:**
  - PayrollReport: Giao diện để hiển thị báo cáo lương sau khi tính toán.
  - PayrollMessage: Hiển thị thông báo xác nhận về việc thực hiện tính lương.
- **Control Classes:**
  - PayrollController: Điều phối quá trình tính lương. Nó gọi các phương thức để tính toán lương và tạo báo cáo.
- **Entity Classes:**
  - Payroll: Đại diện cho thông tin lương được tính toán.
  - Employee: Cung cấp thông tin về nhân viên để tính lương.




--- 
