# BÁO CÁO THỰC HÀNH: QUẢN LÝ LỖI PHẦN MỀM (DEFECT MANAGEMENT)

## Dự án: Student Management System (SMS)

**Đơn vị:** CMC University

**Nhóm thực hiện:** Nhóm 4 - BTC6

---

## 1. Thông tin chung

* **Thành viên & Vai trò:**
* **Nguyễn Tâm:** QA Lead / Tester
* **Đỗ Phúc:** Developer / Project Manager
* **Ngân Nguyễn:** Tester / Developer
* **Thien Hoang Minh:** QA / Tester
* **xinha1k5:** Developer / QA



---

## 2. Quản lý lỗi bằng GitHub Issues

* **Repository:** `DoPhuc05/BT6_nhom4`
* **Tổng số issue:** 10 (Đã đóng 100%)
* **Danh sách lỗi tiêu biểu:**
1. `[BUG]` Hệ thống bị crash khi xóa sinh viên (#5)
2. `[BUG]` Thêm sinh viên mới nhưng dữ liệu không được lưu (#2)
3. `[BUG]` Không đăng nhập được dù nhập đúng mật khẩu (#1)
4. `[BUG]` Hệ thống cho phép thêm sinh viên trùng mã sinh viên (#6)
5. `[BUG]` Trang danh sách tải rất chậm khi dữ liệu lớn (#9)



---

## 3. Quản lý lỗi chuyên nghiệp bằng Jira

* **Project:** Nhóm 4 - BTC6 (Key: KAN)
* **Tổng số Bug/Task:** 11 (Tất cả trạng thái: **DONE**)
* **Workflow áp dụng:** `New` $\rightarrow$ `Open` $\rightarrow$ `In Progress` $\rightarrow$ `Fixed` $\rightarrow$ `QA Verify` $\rightarrow$ `Done`

---

### 4. Phân tích 2 Bug nghiêm trọng (Critical Bugs)

#### Bug 01: Đăng nhập thất bại dù nhập đúng tài khoản hệ thống

* **Mã lỗi:** **KAN-5** (Jira) / Issue #1 (GitHub)
* **Severity:** **Critical (Blocker)**
* **Mô tả:** Người dùng nhập đúng Username và Password đã tồn tại trong cơ sở dữ liệu nhưng hệ thống vẫn báo lỗi "Thông tin không chính xác" hoặc không phản hồi.
* **Tác động:** Đây là lỗi **Blocker** vì người dùng hoàn toàn không thể truy cập vào hệ thống để sử dụng các chức năng khác (Quản lý, Tìm kiếm...).
* **Các bước tái hiện:** 1. Truy cập trang Login.
2. Nhập tài khoản hợp lệ.
3. Nhấn "Login" -> Hệ thống từ chối truy cập.
* **Kết quả:** Đã Fix lỗi logic ở tầng Authentication và Verify thành công.

#### Bug 02: Hệ thống bị crash (màn hình trắng/lỗi 500) khi thực hiện xóa sinh viên

* **Mã lỗi:** **KAN-10** (Jira) / Issue #5 (GitHub)
* **Severity:** **Critical (Major)**
* **Mô tả:** Khi nhấn nút "Xóa" trên một sinh viên bất kỳ, hệ thống gặp lỗi runtime và không thể tiếp tục hoạt động.
* **Nguyên nhân:** Lỗi xung đột dữ liệu khi xóa bản ghi có ràng buộc khóa ngoại.
* **Kết quả:** Đã xử lý ngoại lệ (Try-Catch) và thông báo xác nhận trước khi xóa.

---

## 5. So sánh GitHub Issues vs Jira

| Tiêu chí | GitHub Issues | Jira Software |
| --- | --- | --- |
| **Độ phức tạp** | Đơn giản, dễ làm quen ngay. | Phức tạp, cần thời gian thiết lập. |
| **Workflow** | Cơ bản (Open/Closed). | Tùy chỉnh linh hoạt (Professional). |
| **Báo cáo** | Hạn chế, chỉ xem được Pulse/Insight cơ bản. | Mạnh mẽ với Dashboard, biểu đồ tròn, tiến độ. |
| **Phù hợp** | Dự án nhỏ, Open Source. | Dự án doanh nghiệp, Agile/Scrum. |

---

## 6. Nhận xét quy trình Defect Management

* **Ưu điểm:** Việc kết hợp cả hai công cụ giúp nhóm hiểu rõ sự khác biệt giữa quản lý task đơn giản và quy trình chuyên nghiệp trong doanh nghiệp.
* **Bài học:** * Tester cần viết Bug Report rõ ràng các bước (Steps to Reproduce) để Developer tiết kiệm thời gian sửa lỗi.
* Việc gán đúng `Priority` (Độ ưu tiên) giúp Project Manager biết được lỗi nào cần xử lý ngay để không chặn (block) tiến độ của nhóm.
