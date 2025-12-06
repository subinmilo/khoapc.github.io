# 📅 Hướng dẫn sử dụng Calendar - Quản lý người giúp việc

## 🎯 Cách thêm ngày làm việc mới

### Bước 1: Chuẩn bị ảnh
- Chụp ảnh món ăn hoặc ảnh minh chứng người giúp việc đi làm
- Đặt tên file theo định dạng: **`YYYY-MM-DD.jpg`** hoặc **`YYYY-MM-DD.png`**
  - Ví dụ: `2024-12-06.jpg`, `2024-12-15.png`

### Bước 2: Upload ảnh vào thư mục
1. Mở thư mục dự án: `khoapc.github.io`
2. Vào thư mục: `images/calendar/`
3. Copy file ảnh vào đây

### Bước 3: Cập nhật file dữ liệu
1. Mở file: **`calendar-data.json`** (ở thư mục gốc)
2. Thêm dòng mới vào phần `workDays`:

```json
{
  "workDays": {
    "2024-12-06": "images/calendar/2024-12-06.jpg",
    "2024-12-07": "images/calendar/2024-12-07.jpg",
    "2024-12-15": "images/calendar/2024-12-15.png"
  }
}
```

**⚠️ Lưu ý:**
- Mỗi dòng cách nhau bởi dấu phẩy `,`
- Dòng cuối cùng KHÔNG có dấu phẩy
- Ngày phải đúng định dạng: `YYYY-MM-DD`
- Đường dẫn ảnh phải đúng với tên file

### Bước 4: Commit và Push lên GitHub

#### Cách 1: Dùng Git Command Line
```bash
# Di chuyển vào thư mục dự án
cd khoapc.github.io

# Thêm tất cả file thay đổi
git add .

# Commit với message
git commit -m "Add work day photos"

# Push lên GitHub
git push origin main
```

#### Cách 2: Dùng GitHub Desktop
1. Mở GitHub Desktop
2. Chọn repo `khoapc.github.io`
3. Tick chọn các file đã thay đổi
4. Ghi commit message: "Add work day photos"
5. Click **Commit to main**
6. Click **Push origin**

#### Cách 3: Upload trực tiếp trên GitHub.com
1. Vào repo: `https://github.com/khoapc/khoapc.github.io`
2. Vào thư mục `images/calendar/`
3. Click **Add file** > **Upload files**
4. Kéo thả ảnh vào
5. Quay lại thư mục gốc, click vào file `calendar-data.json`
6. Click nút **Edit** (biểu tượng bút chì)
7. Thêm dòng mới cho ngày làm việc
8. Click **Commit changes**

### Bước 5: Kiểm tra kết quả
- Đợi 1-2 phút để GitHub Pages cập nhật
- Mở trang: `https://khoapc.github.io/calendar.html`
- Ngày đã thêm sẽ hiển thị với icon ✓ màu xanh
- Click vào ngày để xem ảnh

## 🗑️ Cách xóa ngày làm việc

1. Mở file `calendar-data.json`
2. Xóa dòng tương ứng với ngày muốn xóa
3. Có thể giữ ảnh trong thư mục `images/calendar/` hoặc xóa luôn
4. Commit và push lên GitHub

## 📊 Tính năng

- ✅ **Lịch theo tháng**: Xem lịch làm việc theo từng tháng
- ✅ **Đánh dấu ngày làm**: Icon ✓ màu xanh cho ngày đã làm
- ✅ **Xem ảnh**: Click vào ngày để xem ảnh chi tiết
- ✅ **Thống kê**:
  - Số ngày làm trong tháng
  - Tổng số ngày làm
  - Tỷ lệ phần trăm trong tháng
- ✅ **Lưu trữ vĩnh viễn**: Dữ liệu lưu trên GitHub, không bao giờ mất

## 💡 Mẹo

1. **Đặt tên file nhất quán**: Luôn dùng `.jpg` hoặc `.png`
2. **Kiểm tra JSON**: Dùng [JSONLint](https://jsonlint.com/) để kiểm tra cú pháp JSON
3. **Nén ảnh**: Nên nén ảnh trước khi upload để trang web load nhanh hơn
4. **Backup**: Có thể tải về file `calendar-data.json` để backup định kỳ

## ❓ Khắc phục sự cố

### Ảnh không hiển thị?
- Kiểm tra tên file trong `calendar-data.json` có khớp với tên file thực tế không
- Kiểm tra đường dẫn có đúng là `images/calendar/` không
- Đảm bảo đã push ảnh lên GitHub

### JSON bị lỗi?
- Kiểm tra có thiếu dấu phẩy `,` giữa các dòng không
- Dòng cuối cùng không được có dấu phẩy
- Tất cả chuỗi phải trong dấu ngoặc kép `"`

### Ngày không xuất hiện trên lịch?
- Kiểm tra định dạng ngày phải là `YYYY-MM-DD`
- Đảm bảo file `calendar-data.json` đã được commit và push

## 📞 Liên hệ

Nếu gặp vấn đề, vui lòng liên hệ qua GitHub Issues hoặc email.

---

**Tạo bởi: Calendar Management System**
**Phiên bản: 1.0**
**Cập nhật: 2024-12-06**
