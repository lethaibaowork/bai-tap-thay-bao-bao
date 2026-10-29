# Git Cheat Sheet – FIT Đại Nam

## Cấu hình ban đầu
```
git config --global user.name "Họ Tên"
git config --global user.email "email@example.com"
git config --global init.defaultBranch main
```

## Repo cục bộ
| Lệnh | Mô tả |
|-------|--------|
| `git init` | Tạo repo mới |
| `git status` | Xem trạng thái (DÙNG SAU MỌI THAO TÁC) |
| `git add <file>` | Đưa file vào vùng chờ (staging) |
| `git add .` | Đưa tất cả file đã thay đổi |
| `git commit -m "..."` | Lưu snapshot vào repo |
| `git log --oneline` | Xem lịch sử commit |
| `git diff` | Xem thay đổi chưa add |
| `git diff --staged` | Xem thay đổi đã add, chưa commit |

## Sửa sai
| Lệnh | Mô tả |
|-------|--------|
| `git restore <file>` | Bỏ thay đổi chưa add |
| `git restore --staged <file>` | Rút file khỏi vùng chờ |
| `git commit --amend` | Sửa commit vừa tạo (CHƯA push) |
| `git revert <hash>` | Hoàn tác 1 commit đã có (an toàn) |

## Nhánh
| Lệnh | Mô tả |
|-------|--------|
| `git branch` | Liệt kê nhánh |
| `git switch -c <tên>` | Tạo + chuyển nhánh mới |
| `git switch <tên>` | Chuyển nhánh |
| `git merge <tên>` | Gộp nhánh vào nhánh hiện tại |
| `git log --oneline --graph --all` | Xem đồ thị nhánh |

## GitHub
| Lệnh | Mô tả |
|-------|--------|
| `git remote add origin <url>` | Kết nối repo local với GitHub |
| `git push -u origin main` | Đẩy code lên GitHub lần đầu |
| `git push` | Đẩy code (các lần sau) |
| `git pull` | Kéo code mới từ GitHub về |
| `git clone <url>` | Tải repo từ GitHub về máy |

## Xử lý xung đột (conflict)
1. `git pull` hoặc `git merge` → báo CONFLICT
2. Mở file, tìm dấu `<<<<<<<`, `=======`, `>>>>>>>`
3. Sửa tay: giữ nội dung đúng, xóa các dấu conflict
4. `git add <file>` → `git commit`
