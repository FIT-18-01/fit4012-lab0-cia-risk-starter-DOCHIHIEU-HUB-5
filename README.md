[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/x2BSeMc-)
# FIT4012 - Lab 01
## CIA & Risk: Hệ thống lưu điểm

Starter repo này được dùng cho bài lab mở đầu của học phần **FIT4012 - Nhập môn An toàn Bảo mật Thông tin**.

Mục tiêu kép của repo:
1. Giúp sinh viên làm quen với tư duy **CIA - threat - vulnerability - mitigation**.
2. Giúp sinh viên làm quen với workflow nộp bài bằng **GitHub**: fork/clone/edit/commit/push/nộp link repo.

---

## 1. Mục tiêu học tập
Sau khi hoàn thành lab này, sinh viên có thể:
- nhận diện các **assets** cần bảo vệ trong một hệ thống thông tin đơn giản;
- phân biệt **Confidentiality, Integrity, Availability (CIA)**;
- xác định **threat**, **vulnerability** và đề xuất **mitigation** phù hợp;
- sử dụng GitHub ở mức cơ bản để nhận bài, chỉnh sửa bài làm và nộp link repo.

---

## 2. Bối cảnh bài lab
Một hệ thống lưu điểm cho phép:
- giảng viên nhập điểm;
- sinh viên xem điểm.

Trong tháng qua xảy ra 3 sự cố:
- **A)** Một số sinh viên phản ánh **không đăng nhập được** vào tối trước ngày công bố điểm.
- **B)** Có trường hợp điểm của một sinh viên bị đổi từ **8.0** thành **5.0**.
- **C)** Danh sách điểm bị lộ ra một **nhóm chat ngoài lớp**.

---

## 3. Yêu cầu bài làm
Sinh viên hoàn thành các phần sau trong file `answers/lab1_answers.md` và `report-1page.md`:

### Phần 1. Assets
Liệt kê **ít nhất 2 assets** cần được bảo vệ trong hệ thống trên.

### Phần 2. Mapping CIA
Ghép từng sự cố **A/B/C** với một mục tiêu chính trong bộ ba **CIA**:
- **C** - Confidentiality
- **I** - Integrity
- **A** - Availability

### Phần 3. Phân tích sự cố B
Với sự cố **B**, hãy nêu:
- **1 threat**
- **1 vulnerability**
- **1 mitigation**

### Phần 4. Reflection
Viết **5-7 dòng** trả lời câu hỏi:

> Nếu là quản trị viên hệ thống, em sẽ ưu tiên xử lý vấn đề nào trước? Vì sao?

### Phần 5. Bonus (khuyến khích)
Viết flag theo định dạng:

`FIT4012{A-?-B-?-C-?}`

trong đó `?` là một trong ba ký hiệu `C/I/A`.

---

## 4. Cấu trúc repo
```text
fit4012-lab01-cia-risk-starter/
├── README.md
├── report-1page.md
├── answers/
│   └── lab1_answers.md
├── tests/
│   └── checklist.md
├── logs/
│   └── activity_log.md
├── assets/
│   └── context-diagram.md
└── .gitignore
```

---

## 5. Hướng dẫn GitHub cho sinh viên

### Cách 1. Dùng GitHub Classroom (nếu giảng viên cung cấp link assignment)
1. Mở link assignment.
2. Bấm **Accept assignment**.
3. Chờ GitHub tạo repo cá nhân/nhóm.
4. Copy URL repo vừa được tạo.
5. Clone repo về máy.

### Cách 2. Dùng Fork (nếu giảng viên cung cấp starter repo công khai)
1. Mở repo starter.
2. Bấm **Fork** để tạo bản sao trên tài khoản GitHub của mình.
3. Copy URL repo đã fork.
4. Clone repo về máy.

### Clone repo về máy
```bash
git clone <repo-url>
cd fit4012-lab01-cia-risk-starter
```

### Làm bài
- Mở file `answers/lab1_answers.md` và điền đáp án.
- Hoàn thiện file `report-1page.md`.
- Cập nhật `logs/activity_log.md` trong quá trình làm.
- Tự kiểm bằng `tests/checklist.md` trước khi nộp.

### Commit và push
```bash
git add .
git commit -m "Complete Lab 01 answers"
git push origin main
```

### Gợi ý commit message tốt
- `Create initial answers for Lab 01`
- `Update CIA mapping and analysis`
- `Finalize report and checklist`

Không nên dùng các commit message như:
- `abc`
- `test`
- `final final`
- `123`

---

## 6. Quy định nộp bài
Sinh viên nộp:
- **Repo link (GitHub)**
- `README.md`
- `report-1page.md`
- file trả lời trong `answers/`
- minh chứng tự kiểm trong `tests/`
- nhật ký làm việc trong `logs/`

### Tên file quan trọng
- `report-1page.md`
- `answers/lab1_answers.md`
- `tests/checklist.md`
- `logs/activity_log.md`

---

## 7. Ethics & Safe Use
Lab này chỉ là bài tập **phân tích tình huống học thuật**, không yêu cầu tấn công hệ thống thật.

Sinh viên cần lưu ý:
- không thử truy cập trái phép vào hệ thống thực;
- không thu thập, làm lộ, sửa hay chia sẻ dữ liệu thật;
- chỉ thảo luận trên dữ liệu giả lập trong bài tập.

---

## 8. Tiêu chí hoàn thành tối thiểu
Bài làm được xem là đạt khi:
- nêu đúng ít nhất **2 assets**;
- ghép hợp lý các sự cố với CIA;
- nêu được **1 threat**, **1 vulnerability**, **1 mitigation** cho sự cố B;
- có ít nhất **2 commit** có ý nghĩa trên GitHub;
- repo có đầy đủ các file yêu cầu.

---

## 9. Hỗ trợ nhanh
Nếu gặp lỗi khi dùng GitHub, hãy kiểm tra:
- đã đăng nhập đúng tài khoản GitHub chưa;
- repo đang ở trạng thái **public** hay đã add giảng viên/TA nếu dùng private;
- đã `git add`, `git commit`, `git push` đủ chưa;
- link nộp có phải là link repo GitHub không.

Chúc bạn có một khởi đầu gọn gàng và chuyên nghiệp với FIT4012.
