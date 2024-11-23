# Lab4 Thiết kế các ca sử dụng cho hệ thống "Payroll System"


## 1. Ca sử dụng: Login 
**Mô tả:** Người dùng (nhân viên hoặc quản trị viên) đăng nhập vào hệ thống để truy cập các chức năng khác.

### Tham gia:
- Người dùng (Employee/Admin)

### Tiền điều kiện:
- Người dùng đã có tài khoản trong hệ thống.

### Luồng sự kiện chính:
1. Người dùng mở trang đăng nhập.
2. Người dùng nhập tên đăng nhập và mật khẩu.
3. Hệ thống xác thực thông tin đăng nhập.
   - Nếu thông tin hợp lệ, người dùng được chuyển đến trang chính của hệ thống.
   - Nếu thông tin không hợp lệ, hệ thống hiển thị thông báo lỗi và yêu cầu nhập lại thông tin.

### Hậu điều kiện:
- Người dùng đã đăng nhập thành công và có thể truy cập các chức năng của hệ thống.


### Biểu đồ Sequence

![Squence Login](https://www.planttext.com/api/plantuml/png/b911QWCn34NtFiKd-roWYv95imWKMbgIlHYBOB0rnj8av6nTv4YvGZGp2I6bctfXhA_tlumkF-UL6ZKRIWxKMT-mLMwXkfIwL4aCY_T-dmIVjES5I36LO_LCVP_Kk4p4_0nXZ0AMhmyBNl1HMP2do3g6_0cjnLmTl2LK62JHOTLZts9uS6wQHxbZHpb5CaRNEB9Oego1iisD9nL-RhvVOxyufiQTmNeKkl-Gip8sSlX7q5lIcka4RirNMbXr2f8OLdxvigy0003__mC0)

---

## 2. Ca sử dụng: Maintain Timecard
**Mô tả:** Người dùng (thường là nhân viên hoặc quản lý) duy trì và cập nhật thông tin thời gian làm việc.

### Tham gia:
- Nhân viên
- Quản lý

### Tiền điều kiện:
- Người dùng đã đăng nhập vào hệ thống.

### Luồng sự kiện chính:
1. Người dùng chọn chức năng "Maintain Timecard".
2. Hệ thống hiển thị danh sách các thời gian làm việc hiện có.
3. Người dùng chọn một thời gian cụ thể để chỉnh sửa hoặc thêm mới.
4. Người dùng nhập hoặc cập nhật thông tin thời gian (bắt đầu, kết thúc, giờ làm thêm, v.v.).
5. Hệ thống lưu thông tin đã cập nhật.
6. Hệ thống xác nhận việc lưu thành công và cập nhật danh sách thời gian làm việc.

### Hậu điều kiện:
- Thông tin thời gian làm việc đã được cập nhật thành công trong hệ thống.

### Biểu đồ Sequence

![Squence Maintain Timecard](https://www.planttext.com/api/plantuml/png/X94n2i9G343tVuhGNTmTfA2EdQe72Bzf2VIdvISLUpO7Z-GL_Deg5167G4ZUImAvNs-v6aORGklGMnVXf1HTdqhikKSno8uSo6Eie431XWA9PO0AxthH15iQvQX6uGLDgNFFiG2hxSA23PJKaazAWIoMujFFt89CvZGgENlMliKHwC9gB0tOJEg_DVX1Vv87COhheQ_Gw4K3Izt5WCQT_Bwfn3F1P5KBOoQ-5-qwgJa6qAUfW_UawdAIAltY0G00__y30000)

---

## 3. Ca sử dụng: Run Payroll
**Mô tả:** Quản lý thực hiện quy trình thanh toán lương cho nhân viên.

### Tham gia:
- Quản lý

### Tiền điều kiện:
- Người dùng đã đăng nhập vào hệ thống và có quyền truy cập vào chức năng thanh toán.

### Luồng sự kiện chính:
1. Người dùng chọn chức năng "Run Payroll".
2. Hệ thống hiển thị danh sách nhân viên và thông tin lương tương ứng.
3. Người dùng kiểm tra thông tin lương và xác nhận thông tin.
4. Hệ thống thực hiện tính toán lương dựa trên thông tin thời gian làm việc và các yếu tố khác (thuế, phụ cấp, khấu trừ, v.v.).
5. Hệ thống tạo báo cáo lương và lưu trữ thông tin thanh toán.
6. Hệ thống thông báo hoàn thành quy trình thanh toán.

### Hậu điều kiện:
- Lương của nhân viên đã được tính toán và lưu trữ thành công trong hệ thống.

### Biểu đồ Sequence

![Squence Run Payroll](https://www.planttext.com/api/plantuml/png/V95DJWCn38NtEOKrUoxG1QfK95P5Y9x0IZqeacD7ZcUHix7WI5o102djj5Atpzzx_llw-DnMH_CbSy3eQh17mNUoKBgQOYee3jChDbDcEBJgb2V02aFwKzRq1JNAOQJ2m-FQ21iu45FihhT5JhKfhA7k-iUVKYsC3IWNraO4dAe3oX4gCbg39BFUwxTJcPFbIzmoUbAvqtM771T6fs4BP-Ow_vc4x8SiusX6HSrlmqypRk15FSqDelQTw7UIBScn_-GR003__mC0)

---

## 4. Ca sử dụng: BankSystem Subsystem
**Mô tả:** Subsystem này quản lý các giao dịch ngân hàng, bao gồm việc gửi tiền, kiểm tra số dư và xử lý các giao dịch thanh toán.

### Tham gia:
- Nhân viên kế toán
- Quản lý

### Tiền điều kiện:
- Người dùng đã đăng nhập vào hệ thống và có quyền truy cập vào chức năng ngân hàng.

### Luồng sự kiện chính:
1. Người dùng chọn chức năng "Bank Transactions".
2. Hệ thống hiển thị các tùy chọn giao dịch (gửi tiền, kiểm tra số dư, thanh toán).
3. Người dùng chọn loại giao dịch mong muốn.
   - Nếu là giao dịch gửi tiền:
     - Người dùng nhập thông tin số tiền và tài khoản.
     - Hệ thống xác nhận và thực hiện giao dịch.
   - Nếu là kiểm tra số dư:
     - Hệ thống truy vấn và hiển thị số dư tài khoản.
   - Nếu là giao dịch thanh toán:
     - Người dùng nhập thông tin thanh toán (số tiền, tài khoản đích).
     - Hệ thống xác nhận và thực hiện thanh toán.
4. Hệ thống thông báo kết quả giao dịch.

### Hậu điều kiện:
- Giao dịch ngân hàng đã được thực hiện thành công và thông tin được cập nhật trong hệ thống.


### Biểu đồ Sequence

![Squence BankSystem Subsystem](https://www.planttext.com/api/plantuml/png/f9B1JiCm38RlVWfhTrw00vhOk2BGu05CwefegHF5xY7Fne57uXN8qafqMWMJw2bo_k-ptVRhutEhHjd68G0vYnbVbJEaMlBE9nB3pJt94LyoYTQ4Zw8R9CLJTLayPmv5ZOSMd8u09p7YpTq5YRTuuC1kjHLSfAjXKbPkxpK5AcW_0OnfckUAValCIcAWOBZd5DKRO7sQOrtn85RlQ8XZtPUaGtAkdRtqiS6_JhwBqliyD3Bbw5XrEGvmKCRTExjZzGGIntyxdqVEfHcx-RsypMYpFL4PMAvSB4tXVsmp6u2bWpcutl0nck_Fls5c7OF1jhBrp_m6003__mC0)

---

## 5. Ca sử dụng: PrintService Subsystem
**Mô tả:** Subsystem này quản lý các chức năng in ấn, bao gồm việc gửi tài liệu để in và theo dõi trạng thái in.

### Tham gia:
- Nhân viên
- Quản lý

### Tiền điều kiện:
 - Người dùng đã đăng nhập vào hệ thống và có quyền truy cập vào chức năng in ấn.

### Luồng sự kiện chính:
1. Người dùng chọn chức năng "Print Documents".
2. Hệ thống hiển thị danh sách tài liệu có thể in.
3. Người dùng chọn tài liệu cần in và cấu hình các tùy chọn in (số bản sao, định dạng, v.v.).
4. Người dùng xác nhận yêu cầu in.
5. Hệ thống gửi tài liệu đến máy in và thông báo trạng thái in (đang in, hoàn thành, lỗi).
6. Người dùng có thể kiểm tra trạng thái in và xem lịch sử in ấn.

### Hậu điều kiện:
- Tài liệu đã được gửi để in và trạng thái in được cập nhật trong hệ thống.

### Biểu đồ Sequence

![Squence PrintService Subsystem](https://www.planttext.com/api/plantuml/png/X95D2i8m48NtESNGlHTm8O9TYr0yG4od4iYVoKJesLnu9A_Wj6aBHOghXCVttfjaFg_tCP6CbAqHKf6FS4qOHM19Ansa8wWkKVFHO7ngXHN81ACo2MkswHEX7Q5o5M881DWTLYxOSw11jSJNNcMBZb8bLXpxIX0xQfs2aJs40P0tWz3EhdyjCmZIjQ2yw_GzHmGVI7ktxJuDPBIb4I8-CYRQ7h11Jb-go1SV_-T4_1QSFUbkUX7m9YWdSUGKtiSN003__mC0)

---

## 6. Ca sử dụng: ProjectManagementDatabase Subsystem
**Mô tả:** Subsystem này quản lý thông tin về các dự án, bao gồm việc thêm, sửa đổi và xóa thông tin dự án.

### Tham gia:
- Quản lý dự án
- Nhân viên

### Tiền điều kiện:
- Người dùng đã đăng nhập vào hệ thống và có quyền truy cập vào chức năng quản lý dự án.

### Luồng sự kiện chính:
1. Người dùng chọn chức năng "Manage Projects".
2. Hệ thống hiển thị danh sách các dự án hiện có.
3. Người dùng có thể chọn một dự án để xem chi tiết, sửa đổi hoặc xóa.
   - Nếu người dùng chọn thêm dự án mới:
     - Người dùng nhập thông tin dự án (tên, mô tả, ngày bắt đầu, ngày kết thúc).
     - Hệ thống lưu thông tin dự án mới.
   - Nếu người dùng chọn sửa đổi dự án:
     - Người dùng cập nhật thông tin dự án.
     - Hệ thống lưu thông tin đã cập nhật.
   - Nếu người dùng chọn xóa dự án:
     - Hệ thống yêu cầu xác nhận xóa.
     - Nếu xác nhận, hệ thống xóa dự án khỏi cơ sở dữ liệu.
4. Hệ thống thông báo kết quả thao tác (thêm, sửa, xóa) cho người dùng.

### Hậu điều kiện:
- Thông tin dự án đã được cập nhật thành công trong hệ thống.

### Biểu đồ Sequence

![Squence ProjectManagementDatabase Subsystem](https://www.planttext.com/api/plantuml/png/d991JiCm44NtFiKeUox00hMYB468g0SOnPFAoB6DPmBaR2mu4bV0jPsYKhL4U6ND_FV_b-MlZyyL2qOP1wkm4nzXonHLI2FJcO1Ee7cC_fawWNjqkAE1d3I037NyCpscsec5XgmiLwNsrW1NDwSeN4DBTX_IbE4iuKQTYfD3iKpOnd2mE06z6nRZTX0gk2WDPxb2Ax3MUXOhI2Sxd36uSvAMbGRZUf-HosLRV2Lmz7P89Si4sw1HQ75obVydUioeFexVfAVu5N_PwebUHcA1phlUn075U0VYGMUZF_lV5gp84xeWiLOyr7PQrTsPZ0Slff_01ugbNYGUhQXLGjDN_mO00F__0m00)

