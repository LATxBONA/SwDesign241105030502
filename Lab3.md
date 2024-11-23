# Lab 3. Identify design elements
## Xác định các phần tử thiết kế của hệ thống “Payroll System”
### 1. Subsystem context diagrams
#### 1.1 BankSystem Subsystem
##### Biểu đồ
![diagram BankSystem](https://www.planttext.com/api/plantuml/png/Z59BQiCm4Dtx52AhTf4Sm1WJsfKt8P0JZEL9AgoFaKPGq-PaNVH8lK9bMxHItD9gCp3pFiCRVRozxns19QzaCG3luO9iSuJH6YdPQNI4QiDU2XOUb-0SYxD7escgQEDqUTRh2BYxdzlNOYv24zepS6JD0-X-4SwO7Gx62SffY-KtusZDyvZGgihvrYrYmpIhw_z9XYNv4_8-qq9DWd89L8Cq8sBJ9KrGncjAZO3mvxKRVJPM0GcZ_x9g0_m02bCZpYUdWrSjsZHbuqdeIzAFnklZRBTr5dcvFb4whbvtkrNU9HCX1bHXQJSpRW6JoLUY9VCEVyVTfXBXrsAFkWk_y1C00F__0m00)

##### Giải thích
- PayrollController: Điều khiển hệ thống trả lương, thực thi phương thức runPayroll() để gọi các chức năng liên quan.
- IBankSystem: Giao diện định nghĩa phương thức deposit, đại diện cho quá trình giao tiếp giữa hệ thống Payroll và BankSystem.
- BankSystemProxy: Là lớp trung gian triển khai giao diện IBankSystem, thực hiện chức năng giao tiếp với hệ thống ngân hàng thực tế.
- Paycheck: Thực thể lưu trữ thông tin bảng lương của nhân viên.
- BankInformation: Thực thể lưu trữ thông tin tài khoản ngân hàng, bao gồm tên ngân hàng, số tài khoản, và số định tuyến.

#### 1.2 PrintService Subsystem
##### Biểu đồ

![diagram PrintService](https://www.planttext.com/api/plantuml/png/Z59BJiCm4Dtd55PNPT4U88gYIh3f0gdG4nXdG16EdSwCKIleoLXm9Ax0s0GHf-NZZULvyzuRlV7xwzkAM2E7pXQzDe_w0THiWwrZjJqGGpTJpuMIOwmcKWcvz8xHMmiuO9-dZzYLDw43n_EBX1oBT0a0UAyDg7LIs08-jV8weUUqaUV0sA3V7qQqgg9mHsbG4H2ihlyZ-JNbBUm246U2KcuvrscyMJUZTo30h2167eNrm_0t0G9SQoVXubzUkzYRYSj-ED1OUhg5nQAU15kUtKRUKxqibsV2BLNRzHOYZRxTifReDusmZAdyHZXDOg0SYnMuHZxW1m000F__0m00)

##### Giải thích
- PrintController: Điều khiển yêu cầu in tài liệu, sử dụng phương thức printDocument() để bắt đầu quá trình in.
- IPrintService: Giao diện cung cấp chức năng in, bao gồm phương thức print.
- PrintServiceProxy: Triển khai giao diện IPrintService, thực hiện chức năng in tài liệu thông qua hệ thống in thực tế.
- DocumentRequest: Thực thể lưu trữ thông tin yêu cầu in, như mã tài liệu, người dùng và mức độ ưu tiên.
- PrintQueueManager: Thực thể quản lý hàng đợi in, theo dõi trạng thái và ID hàng đợi.

#### 1.3 ProjectManagementDatabase subsystems
##### Biểu đồ

![diagram ProjectManagementDatabase](https://www.planttext.com/api/plantuml/png/b591QiCm4Bpx5KjExI5vW34cq5voQ0Wa7zZOs-16aers3GrjNjP3dvGlH5OKi2f3g2vYTsPsn6WlFxzB5hJIQvLrM1tnG33RsFQ3Ae4tDAxMP0Is9nRIC_ZAm9rA8JC4sajhnBPAaGtexMWl3fodPu-SCtyrHiY-OqMm2lWh2kwHQMB20CNooFskTENdQIGl2kxtx5yDtO2LvNz7HzDS28t4GxeRRLMdlJLg6dLznCwDKgyTyl6HaJXEvEA4pS5GlMj7pRgdlnRf3ytdPHfwFlbP2QtuNYocOy-XqPtocy9ZuvWrUD-ZpQ5dUi3rqGJYELkIgTsMNW400F__0m00)

##### Giải thích
- ProjectController: Điều khiển quản lý dự án, sử dụng phương thức manageProject() để điều phối công việc liên quan đến dự án.
- IProjectDatabase: Giao diện quản lý dữ liệu liên quan đến dự án.
- ProjectDatabaseProxy: Lớp trung gian triển khai giao diện IProjectDatabase, thực hiện các thao tác với cơ sở dữ liệu dự án thực tế.
- Project: Thực thể lưu trữ thông tin dự án, như ID dự án, tên, và ngày bắt đầu.
- Task: Thực thể lưu trữ thông tin về các nhiệm vụ, như ID nhiệm vụ, người được giao, và hạn chót.


### 2. Analysis class to design element map

| Analysis Class                | Design Element                |
|-------------------------------|-------------------------------|
| LoginForm                     | LoginForm                     |
| MaintainTimecardForm          | MainEmployeeForm              |
| TimecardController             | TimecardController            |
| PayrollController              | PayrollController             |
| Paycheck                      | Paycheck                      |
| BankInformation               | BankInformation               |
| SystemClockInterface          | SystemClockInterface          |
| Employee                      | Employee                      |
| Timecard                      | TimecardEntity                |
| Payroll                       | PayrollProcessor              |
| BankSystem                    | BankSystemProxy               |
| IBankSystem                   | IBankSystem                   |
| PrintService                  | PrinterServiceProxy           |
| IPrinterService               | IPrinterService               |
| ProjectManagementDatabase     | ProjectManagementDatabase     |

### 3. Design element to owning package map

| Design Element                | "Owning" Package                          |
|-------------------------------|-------------------------------------------|
| LoginForm                     | Middleware::Security:GUI Framework        |
| MainEmployeeForm              | Applications::Employee Activities          |
| TimecardForm                  | Applications::Employee Activities          |
| MainApplicationForm           | Middleware::Security:GUI Framework        |
| TimecardController             | Applications::Employee Activities          |
| SystemClockInterface          | Applications::Payroll                     |
| PayrollController              | Applications::Payroll                     |
| Paycheck                      | Business Services::Payroll Artifacts      |
| BankInformation               | Business Services::Payroll Artifacts      |
| TimecardEntity                | Business Services::Employee Data          |
| PayrollProcessor              | Applications::Payroll                     |
| BankSystemProxy               | Middleware::Banking Integration           |
| IBankSystem                   | Middleware::Banking Integration           |
| PrinterServiceProxy           | Middleware::Printing Integration           |
| IPrinterService               | Middleware::Printing Integration           |
| ProjectManagementDatabase     | Applications::Project Management          |

### 4. Architectural layers and their dependencies

![diagram layer](https://www.planttext.com/api/plantuml/png/R9BFRi8m3CRlUOg8Eo_GmmJiZpG992IuJJjugIaPYOES55QXFTaEUwIzmff0fhJQgV9d-_lPJd--lcS-08VM6i6e0b1ZK4xMZ1ufGD2Ev18wv8a4BmVoHKZvidIDfYV7zZL6Az0qFnwDLgbae3_Qet4TubNy52Mkw2befPfWQ-ZO6NFlACGlSZBVQeiAk1x9j-8rEuNUEnup5wtNr6Va1lca5HRWdCgP35TxL8TalW0wFDEkNoMDbxIyu1Zq007aNCKf2aPKR-8bEsuw7z3s4tzqrnLOKq2-ZL7gxhttNm51WxP_a6Zs1lvVTDH7t2GbwbzqHQV-mIDFQtUcwTtWBIgfdBKjnHYzFEkm5sK-zupFMCaQ3JQfAJWnJkUsuZALR3rwKIXbKHgyaeo1DPvwqpfUUiVEYXbI7N_fNm000F__0m00)
