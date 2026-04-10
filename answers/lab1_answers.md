# Lab 01 Answers
## CIA & Risk: Hệ thống lưu điểm

**Họ và tên:** Đỗ Chí Hiếu

**MSSV:** 1871020235

**Lớp/Nhóm:** CNTT18_01

---

## 1. Assets
Liệt kê ít nhất 2 assets cần bảo vệ.

- Asset 1: Database/File điểm của sinh viên (dữ liệu điểm số)
- Asset 2: Tài khoản người dùng (credentials, authentication tokens)
- Asset 3 (nếu có): Hệ thống server lưu điểm (ứng dụng và dữ liệu)

---

## 2. Mapping CIA
Ghép từng sự cố với CIA.

- Sự cố A -> A (Availability) - Hệ thống không khả dụng
- Sự cố B -> I (Integrity) - Dữ liệu bị thay đổi trái phép
- Sự cố C -> C (Confidentiality) - Dữ liệu bị tiết lộ trái phép

---

## 3. Phân tích sự cố B
- Threat: Unauthorized modification - Kẻ tấn công hoặc người dùng nội bộ (giảng viên, quản trị) thay đổi trái phép điểm của sinh viên
- Vulnerability: Thiếu access control (RBAC) - không phân quyền rõ ràng; Không có audit log - không ghi nhận lịch sử; Hệ thống thừa tin - không xác thực danh tính; Input validation yếu - có thể nhập giá trị lạ
- Mitigation: Implement RBAC với quyền riêng biệt; Bắt buộc MFA cho tài khoản có quyền chỉnh sửa; Implement audit logging ghi nhận mọi thay đổi; Require approval workflow cho sự thay đổi; Regular backup và integrity checking

---

## 4. Reflection
Từ bài lab này, em học được rằng mỗi sự cố bảo mật cần được phân tích toàn diện qua bộ ba CIA. Phần khó nhất là hiểu rõ mối liên hệ giữa threat (mối đe dọa), vulnerability (điểm yếu) và mitigation (giải pháp). Em nhận ra rằng cần phải: (1) xác định rõ asset bị ảnh hưởng, (2) phân loại sự cố theo CIA đầu tiên, (3) tìm threat cụ thể, (4) liệt kê vulnerability thực tế, (5) đề xuất mitigation khả thi. Đặc biệt, cần cân nhân ưu tiên xử lý dựa trên mức độ ảnh hưởng. Bài lab này đã giúp em nắm vững quy trình phân tích bảo mật cơ bản.



---

## 5. Bonus Flag
`FIT4012{A-? `FIT4012{A-A-B-I-C-C}`
(Sự cố A → Availability, Sự cố B → Integrity, Sự cố C → Confidentiality)-B-?-C-?}`

Flag của em:

