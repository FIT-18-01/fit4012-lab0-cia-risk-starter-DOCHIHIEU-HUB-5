# FIT4012 - Report 1 Page
## Lab 01 - CIA & Risk: Hệ thống lưu điểm

### 1. Mục tiêu bài lab
- Nhận diện tài sản cần bảo vệ trong một hệ thống thông tin đơn giản.
- Phân biệt Confidentiality, Integrity, Availability.
- Xác định threat, vulnerability, mitigation.
- Thực hành workflow GitHub cơ bản để nhận và nộp bài.

### 2. Cách làm
- Đọc bối cảnh và xác định các thành phần quan trọng của hệ thống.
- Phân tích từng sự cố theo bộ ba CIA.
- Chọn sự cố B để phân tích sâu hơn theo threat - vulnerability - mitigation.
- Hoàn thiện bài làm trong repo và commit/push lên GitHub.

### 3. Kết quả chính
**Assets:**
- Database/File điểm của sinh viên
- Tài khoản người dùng (credentials, tokens)
- Hệ thống server lưu điểm

**CIA mapping:**
- Sự cố A (không đăng nhập được) -> **Availability**
- Sự cố B (điểm bị thay đổi) -> **Integrity**
- Sự cố C (danh sách điểm bị lộ) -> **Confidentiality**

**Phân tích sự cố B:**
- **Threat:** Unauthorized modification - Kẻ tấn công hoặc người dùng nội bộ thay đổi điểm sinh viên
- **Vulnerability:** Thiếu RBAC, không có audit log, xác thực yếu, không validate input
- **Mitigation:** Implement RBAC, MFA, audit logging, approval workflow, regular backup & integrity checking 

### 4. Kết luận ngắn
(4-6 dòng: em học được gì từ bài lab này, phần nào khó nhất, điều gì cần chú ý khi phân tích một sự cố an toàn thông tin.)

Từ bài lab này, em học được rằng mỗi sự cố bảo mật có thể được phân loại theo CIA - một framework cơ bản nhưng rất quan trọng trong an toàn thông tin. Phần khó nhất là hiểu mối liên hệ giữa threat, vulnerability và mitigation - chúng không phải lúc nào cũng rõ ràng. Khi phân tích, cần chú ý: (1) xác định rõ asset bị ảnh hưởng, (2) phân loại theo CIA trước, (3) tìm threat cụ thể (không chỉ nói chung chung), (4) liệt kê vulnerability thực tế (không trừu tượng), (5) đề xuất mitigation khả thi và hiệu quả. Đặc biệt, phải cân nhân ưu tiên xử lý dựa trên mức độ ảnh hưởng đến người dùng.
