# Git Workflow

## 🆕 Khi bắt đầu làm việc với một folder/project mới

Mở Terminal tại folder đó.

### 1. Khởi tạo Git

Nếu folder chưa có Git:

```bash
git init
```

### 2. Cấu hình Git cho project

Đặt tài khoản Git identity cho **riêng project này**:

```bash
git config --local user.name "BaoTran3103"
git config --local user.email "tranngoctran3103@gmail.com"
```

Kiểm tra lại:

```bash
git config --local --list
```

Hoặc kiểm tra riêng:

```bash
git config --local user.name
git config --local user.email
```

Kết quả mong muốn:

```text
BaoTran3103
tranngoctran3103@gmail.com
```

---

## 📤 Commit & Push

### 3. Kiểm tra thay đổi

```bash
git status
```

### 4. Add code

```bash
git add .
```

### 5. Commit

```bash
git commit -m "initial commit"
```

Hoặc mô tả thay đổi cụ thể:

```bash
git commit -m "update readme"
```

### 6. Đặt branch là `main`

```bash
git branch -M main
```

### 7. Kết nối GitHub repository

```bash
git remote add origin git@github-baotran:BaoTran3103/REPOSITORY_NAME.git
```

Ví dụ:

```bash
git remote add origin git@github-baotran:BaoTran3103/first-project.git
```

### 8. Push lần đầu

```bash
git push -u origin main
```

Sau lần push đầu tiên, những lần sau chỉ cần:

```bash
git add .
git commit -m "mô tả thay đổi"
git push
```

---

# 🔁 Quy trình hằng ngày

Sau khi đã setup project:

```text
Sửa code
   ↓
git status
   ↓
git add .
   ↓
git commit -m "message"
   ↓
git push
   ↓
GitHub
```

## 👤 GitHub Account

Project mặc định sử dụng:

```text
GitHub account: BaoTran3103
Email: tranngoctran3103@gmail.com
```

## ⚠️ Lưu ý

`user.name` và `user.email` xác định **thông tin tác giả của commit**.

SSH remote:

```text
git@github-baotran:...
```

xác định **GitHub account được dùng để xác thực khi push**.

Vì vậy, với project sử dụng BaoTran3103, nên cấu hình **cả hai**.
