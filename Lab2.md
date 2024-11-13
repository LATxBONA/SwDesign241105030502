# 1. Ca sử dụng: Create Administrative Report

## Lớp phân tích:

### Boundary (View):
- **AdministrativeReportForm**: Giao diện người dùng để nhập thông tin báo cáo.
- **AdministrativeReportDisplay**: Hiển thị báo cáo cho người dùng.

### Control (Controller):
- **AdministrativeReportController**: Điều khiển luồng xử lý tạo báo cáo.
- **AdministrativeReportGenerator**: Tạo báo cáo dựa trên thông tin đầu vào.

### Entity (Model):
- **Report**: Thông tin báo cáo.
- **Employee**: Thông tin nhân viên.


## Biểu đồ Sequence:

![Sequence Create Administrative Report](https://www.planttext.com/api/plantuml/png/d5DBJiGm3Dtd55x2WWlC0WtYjqVY09d4C96Ik79SKC_6WYDn1JnDIsUaQK0iuxpt_FoSV7ryRejObZv5OvqGmtD1DZlgixSym8rF8OSYR2MyuHDsnF90dDg8kr2wQ0VZA0jJF8kvhNTHkxLWZvXHpyG6imGPe9Rdqttg8Ws8nXny0y3LzQfds82lnfRQnQLPXQlKABg1LvJ9D0T13bPfV-fN-bqA0cwYDNkrGnfTZ55CLolEZnWhcZ-9ggHZ_4rmWQlU7BTINr3S7d0kU2ldnplXrzBHBC1rdVyRPNfdXw3tzDuSOuOkIprv2yhQOlRw3Ru1003__mC0)
## Nhiệm vụ của từng lớp:
### Boundary:
- **AdministrativeReportForm**: Nhận input từ người dùng và hiển thị kết quả báo cáo.
- **AdministrativeReportDisplay**: Hiển thị báo cáo đã tạo.

### Control:
- **AdministrativeReportController**: Điều phối quá trình tạo báo cáo.
- **AdministrativeReportGenerator**: Thực hiện logic tạo báo cáo.

### Entity:
- **Report**: Lưu trữ thông tin báo cáo.
- **Employee**: Cung cấp thông tin nhân viên cho báo cáo.

## Thuộc tính và phương thức chính:
### AdministrativeReportForm:
- **Phương thức**: `displayReportForm()`, `getReportCriteria()`, `showReport()`.
  
### AdministrativeReportDisplay:
- **Phương thức**: `displayReport()`, `printReport()`.
  
### AdministrativeReportController:
- **Phương thức**: `generateReport()`, `validateReportCriteria()`.
  
### AdministrativeReportGenerator:
- **Phương thức**: `createReport()`.
  
### Report:
- **Thuộc tính**: `reportId`, `reportData`, `generatedDate`.
- **Phương thức**: `generateReport()`, `updateReport()`.
  
### Employee:
- Như đã phân tích ở trên.

## Mối quan hệ:
- **AdministrativeReportController** sử dụng **AdministrativeReportForm** và **AdministrativeReportDisplay**.
- **AdministrativeReportGenerator** phụ thuộc vào **Employee** và **Report**.

---

# 2. Ca sử dụng: Create Employee Report

## Lớp phân tích:

### Boundary (View):
- **EmployeeReportForm**: Giao diện người dùng để nhập thông tin báo cáo nhân viên.
- **EmployeeReportDisplay**: Hiển thị báo cáo nhân viên.

### Control (Controller):
- **EmployeeReportController**: Điều khiển luồng xử lý tạo báo cáo nhân viên.
- **EmployeeReportGenerator**: Tạo báo cáo nhân viên.

### Entity (Model):
- **Employee**: Thông tin nhân viên.
- **Report**: Thông tin báo cáo.
## Biểu đồ Sequence:

![Sequence Create Employee Report](https://www.planttext.com/api/plantuml/png/Z98x3i8m38RtdC8Z35oW0qBYjIDnW3Gr42bDAjSLwjaOE19N83IKlbN6sFv-_xRpUZmtEKlY8ZL2AdO4vnn9nAwmYQGIzcbcN8bumimH7nobKxcTpZCZIw6SPNAcbzs6gF7QumL7j4ZI6n1eMNEZNhz3cH0VVm2mMezuWmYIO6EOMop52E1bAi48hiWzowGPIKiFplJCYpZL3EeBJFIPMaZLkneUkoK3norceFVRdvTJXFDY3T3Iyl05MTq0wq0YkJzGXmoXrWmDIk5Y_y_m_KAVZTxSVSP_NTnSSFJqdjkWJVp_VWC00F__0m00)
## Nhiệm vụ của từng lớp:
### Boundary:
- **EmployeeReportForm**: Nhận input từ người dùng và hiển thị kết quả báo cáo nhân viên.
- **EmployeeReportDisplay**: Hiển thị báo cáo nhân viên đã tạo.

### Control:
- **EmployeeReportController**: Điều phối quá trình tạo báo cáo nhân viên.
- **EmployeeReportGenerator**: Thực hiện logic tạo báo cáo nhân viên.

### Entity:
- **Employee**: Cung cấp thông tin nhân viên cho báo cáo.
- **Report**: Lưu trữ thông tin báo cáo nhân viên.

## Thuộc tính và phương thức chính:
### EmployeeReportForm:
- **Phương thức**: `displayEmployeeReportForm()`, `getEmployeeReportCriteria()`, `showEmployeeReport()`.
  
### EmployeeReportDisplay:
- **Phương thức**: `displayEmployeeReport()`, `printEmployeeReport()`.
  
### EmployeeReportController:
- **Phương thức**: `generateEmployeeReport()`, `validateEmployeeReportCriteria()`.
  
### EmployeeReportGenerator:
- **Phương thức**: `createEmployeeReport()`.
  
### Employee:
- Như đã phân tích ở trên.

### Report:
- Như đã phân tích ở trên.

## Mối quan hệ:
- **EmployeeReportController** sử dụng **EmployeeReportForm** và **EmployeeReportDisplay**.
- **EmployeeReportGenerator** phụ thuộc vào **Employee** và **Report**.

---

# 3. Ca sử dụng: Maintain Employee Information

## Lớp phân tích:

### Boundary (View):
- **EmployeeInfoForm**: Giao diện người dùng để nhập và chỉnh sửa thông tin nhân viên.
- **EmployeeInfoDisplay**: Hiển thị thông tin nhân viên.

### Control (Controller):
- **EmployeeInfoController**: Điều khiển luồng xử lý duy trì thông tin nhân viên.
- **EmployeeInfoValidator**: Kiểm tra tính hợp lệ của thông tin nhân viên.

### Entity (Model):
- **Employee**: Thông tin nhân viên.
## Biểu đồ Sequence:

![Sequence Maintain Employee Information](https://www.planttext.com/api/plantuml/png/X99DZi8m38NtEOMNmu8Bi1WXyIEnHipUj0OYqgHAd44z6mkEn1KmBRyXm2xDU_wUxVIuFmm3e-TO6OK5Em-BG5ujNRGb-WOcLMrSGpIpApTrliehOnrgWuqgd6Nlp9CswkwCK7Fo7nfTeWGhigpvpbNgt0a0z7zVke01b5raglpqr8jP02rg06lYHrNC7pD2N5QQWIuAQ95KVhQKS1jBCF_TcPBelFs18wN5XehjzNkCZArHrfJKvniHGAo_9ByVuVAevprit6xHWkQC74E2k1hlUyuyZjGCoPRodvq0003__mC0)
## Nhiệm vụ của từng lớp:
### Boundary:
- **EmployeeInfoForm**: Nhận input từ người dùng và hiển thị thông tin nhân viên.
- **EmployeeInfoDisplay**: Hiển thị thông tin nhân viên đã được cập nhật.

### Control:
- **EmployeeInfoController**: Điều phối quá trình duy trì thông tin nhân viên.
- **EmployeeInfoValidator**: Thực hiện kiểm tra tính hợp lệ của thông tin nhân viên.

### Entity:
- **Employee**: Lưu trữ và cung cấp thông tin nhân viên.

## Thuộc tính và phương thức chính:
### EmployeeInfoForm:
- **Phương thức**: `displayEmployeeInfoForm()`, `getEmployeeInfo()`, `showConfirmation()`.
  
### EmployeeInfoDisplay:
- **Phương thức**: `displayEmployeeInfo()`, `showUpdateStatus()`.
  
### EmployeeInfoController:
- **Phương thức**: `updateEmployeeInfo()`, `validateEmployeeInfo()`.
  
### EmployeeInfoValidator:
- **Phương thức**: `checkEmployeeDataValidity()`.
  
### Employee:
- Như đã phân tích ở trên.

## Mối quan hệ:
- **EmployeeInfoController** sử dụng **EmployeeInfoForm** và **EmployeeInfoDisplay**.
- **EmployeeInfoValidator** phụ thuộc vào **Employee**.

---

# 4. Ca sử dụng: Run Payroll

## Lớp phân tích:

### Boundary (View):
- **PayrollRunForm**: Giao diện người dùng để khởi động quy trình chạy bảng lương.
- **PayrollRunReport**: Hiển thị báo cáo kết quả chạy bảng lương.

### Control (Controller):
- **PayrollRunController**: Điều khiển luồng xử lý chạy bảng lương.
- **PayrollCalculator**: Tính toán các khoản thanh toán cho nhân viên.

### Entity (Model):
- **Payroll**: Thông tin bảng lương.
- **Employee**: Thông tin nhân viên.

## Biểu đồ Sequence:

![Sequence Run Payroll](https://www.planttext.com/api/plantuml/png/X59BJiCm4Dtx5BE41HVe0bMgO8qgSO2fCr1B4piQZmKv6mkEr2jq84cTH14i_NxpFFRbwtkV5KLBomwz9e7NJE9EgSG6fOSNx2Kn7qjyJj9kuKVgagZpAQeXC-8m86nnA_A0x0kZJNCKDUWjRZe-jHsddiYvdpO0yF2uQW8xQ4Bk6FibVdVlLaAp_eRiu9rqraw2aWGqmnypSZcrGS6FuetihVkQaJx95wNABehDf3MYRiNyVZnC2TK-avbtsfHPtaZz6MW26bJyR-Jj-RRMEJ2BtgEuhZIVqmTq0mz2kR1cjwVOs7-w0W00__y30000)

## Nhiệm vụ của từng lớp:
### Boundary:
- **PayrollRunForm**: Nhận input từ người dùng để khởi động quy trình chạy bảng lương.
- **PayrollRunReport**: Hiển thị kết quả của quy trình chạy bảng lương.

### Control:
- **PayrollRunController**: Điều phối quá trình chạy bảng lương.
- **PayrollCalculator**: Thực hiện tính toán cho các khoản thanh toán.

### Entity:
- **Payroll**: Lưu trữ thông tin bảng lương.
- **Employee**: Cung cấp thông tin nhân viên cho bảng lương.

## Thuộc tính và phương thức chính:
### PayrollRunForm:
- **Phương thức**: `displayPayrollRunForm()`, `getPayrollRunCriteria()`, `showPayrollRunStatus()`.
  
### PayrollRunReport:
- **Phương thức**: `displayPayrollRunReport()`, `printPayrollRunReport()`.
  
### PayrollRunController:
- **Phương thức**: `executePayrollRun()`, `validatePayrollRunCriteria()`.
  
### PayrollCalculator:
- **Phương thức**: `calculatePayroll()`.
  
### Payroll:
- **Thuộc tính**: `payrollId`, `totalAmount`, `runDate`.
- **Phương thức**: `generatePayroll()`, `updatePayrollStatus()`.
  
### Employee:
- Như đã phân tích ở trên.

## Mối quan hệ:
- **PayrollRunController** sử dụng **PayrollRunForm** và **PayrollRunReport**.
- **PayrollCalculator** phụ thuộc vào **Employee** và **Payroll**.

---

# 5. Ca sử dụng: Select Payment Method

## Lớp phân tích:

### Boundary (View):
- **PaymentMethodForm**: Giao diện người dùng để chọn phương thức thanh toán.
- **PaymentMethodDisplay**: Hiển thị phương thức thanh toán đã chọn.

### Control (Controller):
- **PaymentMethodController**: Điều khiển luồng xử lý chọn phương thức thanh toán.

### Entity (Model):
- **PaymentMethod**: Thông tin về phương thức thanh toán.

## Biểu đồ Sequence:

![Sequence Select Payment Method](https://www.planttext.com/api/plantuml/png/b99D2i8m48NtESKiTU45kf22uauGn0EapMW3-Id91EdPN7Wahs3w0wK_4TpEc_SzyYQVrpltn1q5hHWloJguUNIiiC48xXguy4QZeJDIPSN9EfsGZjBNYZUij8QSLLFnq0zL1CUPf9cNiJOJ07RxPHva87hsGjfisN8zCZfQ1W-aAoei2SLaBTf-v_bGQ4dWExEqPZqbySBMtnddcQdzEIe2GYquuL0i4fVA_m4OJZ4MbsfXrJNsvolxX7ZFktIQTptaQ4JyA5y0003__mC0)
## Nhiệm vụ của từng lớp:
### Boundary:
- **PaymentMethodForm**: Nhận input từ người dùng để chọn phương thức thanh toán.
- **PaymentMethodDisplay**: Hiển thị phương thức thanh toán đã chọn.

### Control:
- **PaymentMethodController**: Điều phối quá trình chọn phương thức thanh toán.

### Entity:
- **PaymentMethod**: Lưu trữ thông tin về phương thức thanh toán.

## Thuộc tính và phương thức chính:
### PaymentMethodForm:
- **Phương thức**: `displayPaymentMethodForm()`, `getSelectedPaymentMethod()`, `showConfirmation()`.
  
### PaymentMethodDisplay:
- **Phương thức**: `displaySelectedPaymentMethod()`.
 ### PaymentMethodController:
- **Phương thức**: `selectPaymentMethod()`, `validatePaymentMethod()`.
  
### PaymentMethod:
- **Thuộc tính**: `methodId`, `methodName`, `details`.
- **Phương thức**: `updateMethodDetails()`.

## Mối quan hệ:
- **PaymentMethodController** sử dụng **PaymentMethodForm** và **PaymentMethodDisplay**.
- **PaymentMethod** được sử dụng để lưu trữ và cập nhật thông tin phương thức thanh toán.

---

# 6. Ca sử dụng: Submit Grades

## Lớp phân tích:

### Boundary (View):
- **SubmitGradesForm**: Giao diện người dùng để nhập điểm cho sinh viên.
- **SubmitGradesReport**: Hiển thị báo cáo điểm đã nhập.

### Control (Controller):
- **SubmitGradesController**: Điều khiển luồng xử lý nhập điểm.
- **GradesValidator**: Kiểm tra tính hợp lệ của điểm nhập vào.

### Entity (Model):
- **Grade**: Thông tin điểm của sinh viên.
- **Student**: Thông tin sinh viên.

## Biểu đồ Sequence:

![Sequence Submit Grades](https://www.planttext.com/api/plantuml/png/X58xRiCm3Drr2exja0juA08KQ92rHhihbf88bIM3eXhuR1bwf5wXZ1L_8Xlk9hqVAOg_rvzj88aKQojaHHxX8sWK1n-TajX26G-reHrAfSERntgPUTUDHnALTuJUFb2l2RCSsjE9-9JMACaLXNPag4rmVoafAZuASMi703OlirQW06L2OsMRCq_FOYRcW2wgW9E-utlNH6BjQedGGN3giCNOvTSEraHaBKrqd90DXAtVwQm7SoxfNQojphhwcl0yll-hiIysGuLL_VoZnybFqIpaBXtd7ix-0hm3HuEr9EETs6gdUF7-0000__y30000)

## Nhiệm vụ của từng lớp:
### Boundary:
- **SubmitGradesForm**: Nhận input từ người dùng để nhập điểm cho sinh viên.
- **SubmitGradesReport**: Hiển thị báo cáo điểm đã nhập.

### Control:
- **SubmitGradesController**: Điều phối quá trình nhập điểm.
- **GradesValidator**: Thực hiện kiểm tra tính hợp lệ của điểm.

### Entity:
- **Grade**: Lưu trữ thông tin điểm của sinh viên.
- **Student**: Cung cấp thông tin sinh viên cho việc nhập điểm.

## Thuộc tính và phương thức chính:
### SubmitGradesForm:
- **Phương thức**: `displaySubmitGradesForm()`, `getGradesInput()`, `showConfirmation()`.
  
### SubmitGradesReport:
- **Phương thức**: `displayGradesReport()`, `printGradesReport()`.
  
### SubmitGradesController:
- **Phương thức**: `submitGrades()`, `validateGrades()`.
  
### GradesValidator:
- **Phương thức**: `checkGradesValidity()`.
  
### Grade:
- **Thuộc tính**: `gradeId`, `studentId`, `value`, `subject`.
- **Phương thức**: `updateGrade()`.
  
### Student:
- Như đã phân tích ở trên.

## Mối quan hệ:
- **SubmitGradesController** sử dụng **SubmitGradesForm** và **SubmitGradesReport**.
- **GradesValidator** phụ thuộc vào **Grade** và **Student**.

---

# 7. Ca sử dụng: View Report Card

## Lớp phân tích:

### Boundary (View):
- **ReportCardDisplay**: Giao diện người dùng để hiển thị bảng điểm.

### Control (Controller):
- **ReportCardController**: Điều khiển luồng xử lý xem bảng điểm.

### Entity (Model):
- **ReportCard**: Thông tin bảng điểm của sinh viên.
- **Student**: Thông tin sinh viên.

## Biểu đồ Sequence:

![Sequence View Report Card](https://www.planttext.com/api/plantuml/png/Z97D3S8m38NlcS97EB001rIfdG34024nj598AiS5TJOEZCGAk3_GebB4pNhszrxiF6xt9B8chivEQSE1O1-Hr25KtcggOOjb84ursQo8fTErCi4p1JVgf9tYX4FF1O-fbxBZoagfL6CF0AlDr1hMOBjgQ2sMQZht0G_fmX-HJJv3ZmR5e7-GC1Vj2giPU-K7C-Y2dT0Z2VPNshTTOnwkVMQ6h0iNvvPjR_O-3b0x0wOvRuBUojyz0G00__y30000)

## Nhiệm vụ của từng lớp:
### Boundary:
- **ReportCardDisplay**: Hiển thị bảng điểm cho sinh viên.

### Control:
- **ReportCardController**: Điều phối quá trình xem bảng điểm.

### Entity:
- **ReportCard**: Lưu trữ thông tin bảng điểm của sinh viên.
- **Student**: Cung cấp thông tin sinh viên cho bảng điểm.

## Thuộc tính và phương thức chính:
### ReportCardDisplay:
- **Phương thức**: `displayReportCard()`, `showStudentDetails()`.
  
### ReportCardController:
- **Phương thức**: `fetchReportCard()`, `validateStudent()`.
  
### ReportCard:
- **Thuộc tính**: `reportCardId`, `studentId`, `grades`, `semester`.
- **Phương thức**: `generateReportCard()`.
  
### Student:
- Như đã phân tích ở trên.

## Mối quan hệ:
- **ReportCardController** sử dụng **ReportCardDisplay**.
- **ReportCard** phụ thuộc vào **Student**.
