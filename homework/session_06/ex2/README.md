# Bài 2: Cấu hình phân quyền Nhóm và sudoers bằng visudo

## 1. Mục tiêu

- Tạo nhóm `devops-admin`.
- Tạo user `deployer`.
- Thêm user `deployer` vào nhóm `devops-admin`.
- Cấu hình sudoers bằng `visudo`.
- Cho phép thành viên nhóm thực hiện các lệnh `systemctl start`, `stop`, `restart`, `status` mà không cần nhập mật khẩu.
- Kiểm tra quyền sudo và khả năng quản lý dịch vụ.

## 2. Tạo nhóm devops-admin

```bash
sudo groupadd devops-admin
sudo adduser deployer
sudo usermod -aG devops-admin deployer
