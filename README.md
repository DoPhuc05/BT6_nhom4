# 📘 BÁO CÁO THỰC HÀNH: QUẢN LÝ LỖI PHẦN MỀM (DEFECT MANAGEMENT)

**Dự án:** Student Management System (SMS)  
**Đơn vị:** CMC University  
**Nhóm thực hiện:** Nhóm 4 - BTC6  

---

# 📑 Mục lục

1. [Thông tin chung](#1-thông-tin-chung)  
2. [Giới thiệu dự án](#2-giới-thiệu-dự-án)  
3. [Danh sách Bug](#3-danh-sách-bug)  
4. [Phân tích 2 Bug nghiêm trọng](#4-phân-tích-2-bug-nghiêm-trọng)  
5. [Thống kê Bug (Jira Dashboard)](#5-thống-kê-bug-jira-dashboard)  
6. [So sánh GitHub Issues và Jira](#6-so-sánh-github-issues-và-jira)  
7. [Nhận xét quy trình Defect Management](#7-nhận-xét-quy-trình-defect-management)  
8. [Sản phẩm nộp (Deliverables)](#8-sản-phẩm-nộp-deliverables)  

---

# 1. Thông tin chung

## Thành viên & Vai trò

| Thành viên | Vai trò |
|---|---|
| Nguyễn Thị Tâm | QA Lead / Tester |
| Đỗ Thị Phúc | Developer / Project Manager |
| Nguyễn Thị Thanh Ngân | Tester / Developer |
| Hoàng Minh Thiện | QA / Tester |
| Nguyễn Thị Xinh | Developer / QA |

---

# 2. Giới thiệu dự án

Dự án mô phỏng **Student Management System (SMS)** – một hệ thống web đơn giản giúp quản lý thông tin sinh viên.

### Các chức năng chính

- Đăng nhập hệ thống
- Quản lý sinh viên (CRUD)
- Tìm kiếm sinh viên
- Phân quyền người dùng

Sinh viên đóng vai **nhân viên QA trong Sprint kiểm thử** để phát hiện và quản lý lỗi phần mềm.

---

# 3. Danh sách Bug

| ID | Tiêu đề Bug | Priority | Status |
|---|---|---|---|
| BUG-01 | Login fails with correct password | Blocker | To Do |
| BUG-02 | System crashes when deleting student | Blocker | To Do |
| BUG-03 | Search returns incorrect results | High | To Do |
| BUG-04 | Add student form allows empty name | High | To Do |
| BUG-05 | Student list not refreshing after update | Medium | To Do |
| BUG-06 | Duplicate student IDs allowed | Medium | To Do |
| BUG-07 | Unauthorized user can access admin page | High | To Do |
| BUG-08 | UI layout breaks on mobile | Low | To Do |

---

# 4. Phân tích 2 Bug nghiêm trọng

## 🐞 Bug 1: Không thể đăng nhập dù đúng tài khoản

**Priority:** Blocker  
**Module:** Authentication  

### Mô tả

Người dùng không thể đăng nhập vào hệ thống mặc dù nhập đúng username và password.

### Các bước tái hiện lỗi

1. Truy cập trang Login
2. Nhập username và password hợp lệ
3. Nhấn nút **Login**

### Kết quả mong đợi

Hệ thống cho phép đăng nhập thành công và chuyển tới Dashboard.

### Kết quả thực tế

Hệ thống hiển thị thông báo **"Invalid credentials"** và không cho đăng nhập.

---

## 🐞 Bug 2: Hệ thống bị crash khi xóa sinh viên

**Priority:** Blocker  
**Module:** Student Management  

### Mô tả

Hệ thống bị crash khi người dùng xóa một sinh viên trong danh sách.

### Các bước tái hiện lỗi

1. Đăng nhập hệ thống
2. Truy cập trang **Student List**
3. Chọn một sinh viên
4. Nhấn **Delete**

### Kết quả mong đợi

Sinh viên được xóa khỏi hệ thống và danh sách được cập nhật.

### Kết quả thực tế

Hệ thống hiển thị lỗi **Server Error 500** và trang bị crash.

---

# 5. Thống kê Bug (Jira Dashboard)

Các biểu đồ được tạo từ Jira Dashboard.

### 📊 Bug by Status

<img width="1849" height="879" alt="Bug by Status" src="https://github.com/user-attachments/assets/23ac9a84-9625-4dc6-a0d8-4bd820e6bd44" />


### 📊 Bug by Priority

<img width="1839" height="897" alt="Bug by Priority" src="https://github.com/user-attachments/assets/b1661cd9-1e61-44ae-8315-6bbbd215d77e" />


### 📊 Bug Trend theo thời gian

<img width="1858" height="873" alt="Bug Trend theo thời gian" src="https://github.com/user-attachments/assets/13d8e85f-f61e-42e5-9654-f3b4cc9a253b" />


Các biểu đồ này giúp theo dõi:

- Số lượng bug theo trạng thái
- Mức độ ưu tiên của bug
- Xu hướng bug theo thời gian

---

# 6. So sánh GitHub Issues và Jira

| Tiêu chí | GitHub Issues | Jira |
|---|---|---|
| Dễ sử dụng | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| Workflow | Cơ bản | Chuyên nghiệp |
| Báo cáo | Hạn chế | Mạnh |
| Doanh nghiệp | ❌ | ✅ |

---

# 7. Nhận xét quy trình Defect Management

Qua bài thực hành, nhóm nhận thấy quy trình quản lý lỗi phần mềm bao gồm các bước:

1. Phát hiện lỗi
2. Tạo bug report
3. Phân loại mức độ ưu tiên
4. Developer sửa lỗi
5. QA verify bug
6. Đóng bug

Sử dụng Jira giúp:

- Theo dõi bug dễ dàng
- Quản lý workflow chuyên nghiệp
- Thống kê bug bằng dashboard

---

# 8. Sản phẩm nộp (Deliverables)

### GitHub Repository

*[( link GitHub repo)](https://github.com/DoPhuc05/BT6_nhom4.git)*

### Jira Project

*[( link Jira project)](https://btnhomc6.atlassian.net/jira/software/projects/KAN/boards/1?atlOrigin=eyJpIjoiMWJhZGYzZGRmNzE5NGE4N2IzYTQwNWI1ODc0MDM5OWIiLCJwIjoiaiJ9)*

### Nội dung thực hiện

- Tạo ≥ 8 Bug
- Phân loại Priority (Blocker / High / Medium / Low)
- Phân tích 2 Bug nghiêm trọng
- Tạo Dashboard thống kê bug
- So sánh GitHub Issues và Jira

---
