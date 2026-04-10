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

- Sự cố A (sinh viên không đăng nhập được) -> **A (Availability)** - Hệ thống không khả dụng
- Sự cố B (điểm bị đổi 8.0 → 5.0) -> **I (Integrity)** - Dữ liệu bị thay đổi trái phép
- Sự cố C (danh sách điểm bị lộ) -> **C (Confidentiality)** - Dữ liệu bị tiết lộ trái phép

---

## 3. Phân tích sự cố B
- **Threat:** Unauthorized modification - Kẻ tấn công hoặc người dùng nội bộ (giảng viên, quản trị) thay đổi trái phép điểm của sinh viên
- **Vulnerability:** 
  - Thiếu access control (RBAC) - không phân quyền rõ ràng giữa giảng viên và admin
  - Không có audit log - không ghi nhận lịch sử thay đổi để truy vết
  - Hệ thống thừa tin tài khoản - không xác thực danh tính khi thực hiện thay đổi quan trọng
  - Input validation yếu - có thể nhập giá trị lạ
- **Mitigation:**
  - Implement 

Nếu là quản trị viên hệ thống, tôi sẽ ưu tiên xử lý **sự cố B (Integrity)** trước. Lý do: Sự cố B ảnh hưởng trực tiếp đến tính chính xác và công bằng của kết quả học tập - đây là vấn đề nghiêm trọng liên quan đến quyền lợi của sinh viên. Nguy hiểm từ sự cố B là lâu dài (ảnh hưởng điểm GPA, học bổng, tốt nghiệp), trong khi đó A là sự cố tạm thời. C cũng cần xử lý nhưng ít ảnh hưởng trực tiếp hơn. Cần triển khai ngay RBAC, MFA, audit logging và backup để ngăn chặn tương lai.Role-Based Access Control (RBAC) - giảng viên chỉ có quyền sửa điểm của lớp mình
  - Bắt buộc Multi-Factor Authentication (MFA) cho các tài khoản có quyền chỉnh sửa
  - Implement audit logging - ghi nhận mọi thay đổi điểm (ai, khi nào, từ giá trị nào sang giá trị nào)
  - Require approval workflow - thay đổi điểm cần phê duyệt từ quản trị viên
  - Regular backup và integrity checking - sao lưu định kỳ và kiểm tra tính toàn vẹn dữ liệu

---

## 4. Reflection
Viết 5-7 dòng.



---

## 5. Bonus Flag
`FIT4012{A-? `FIT4012{A-A-B-I-C-C}`
(Sự cố A → Availability, Sự cố B → Integrity, Sự cố C → Confidentiality)-B-?-C-?}`

Flag của em:

