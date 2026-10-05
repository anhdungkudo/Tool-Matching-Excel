# Smart Excel Folder Matcher Pro 📊

Công cụ tự động hóa văn phòng nhẹ, chạy hoàn toàn bằng HTML + JavaScript thuần, hỗ trợ tự động bóc tách tên, đối chiếu và ghép file Excel vào các thư mục con tương ứng, sau đó xuất file báo cáo kết quả chi tiết `.xlsx`.

---

## 🚀 Tính năng nổi bật

1. **Chuẩn hóa & Bóc tách Họ Tên thông minh**:
   - Tự động cắt bỏ số thứ tự ở đầu file: `1. `, `2. `, `183, `, `03 - `...
   - Tự động nhận diện chữ cái phụ sau số thứ tự: `174a. `, `174b. `, `174A. `, `174.1. `...
   - Tự động cắt bỏ mã số CCCD / mã định danh ở tên thư mục: `002077007214_Nguyen Tien Thang` ➔ `Nguyen Tien Thang`.
2. **Khớp chuẩn tiếng Việt**:
   - Tự động đối chiếu tiếng Việt có dấu ↔ không dấu (hỗ trợ đầy đủ các thanh điệu và chữ `đ`/`Đ`).
   - Tích hợp thuật toán so khớp mờ (Fuzzy matching) khi có sai lệch chính tả nhẹ.
3. **Xử lý trùng lặp & bản sao**:
   - Tự động nhận diện hậu tố `(2)`, `(1)` của file bản sao: tự động bỏ số khi chỉ có 1 folder duy nhất.
   - Phát hiện các trường hợp trùng họ tên (khác CCCD) và cung cấp menu thả xuống để người dùng gán thủ công nhanh chóng.
4. **Không cần cài đặt**:
   - Chạy trực tiếp trên Google Chrome hoặc Microsoft Edge qua File System Access API.
   - Hoạt động 100% offline, không cần internet hay máy chủ backend.
5. **Xuất báo cáo Excel chi tiết**:
   - Tích hợp SheetJS để tải về file Excel báo cáo tiến độ và phân loại trạng thái từng file.

---

## 🛠️ Hướng dẫn sử dụng

1. Mở file `index.html` bằng trình duyệt Google Chrome hoặc Microsoft Edge.
2. **Bước 1**: Bấm chọn thư mục chứa các file Excel nguồn.
3. **Bước 2**: Bấm chọn thư mục đích (chứa các thư mục con CCCD_Họ tên) và bấm "Cho phép" (Allow).
4. **Bước 3**: Kiểm tra danh sách đối chiếu và bấm:
   - **Chép File Vào Thư Mục Đích** để tự động copy.
   - **Xuất File Báo Cáo Excel (.xlsx)** để lưu báo cáo.

---

## 📦 Cấu trúc thư mục

```text
Tool-Matching-Excel/
├── index.html           # Ứng dụng chính (HTML + CSS + JS)
├── xlsx.full.min.js     # Thư viện xuất Excel offline (SheetJS)
├── HDSD.txt             # Hướng dẫn sử dụng nhanh
├── README.md            # Tài liệu dự án
└── .vscode/
    └── launch.json      # Cấu hình khởi chạy trên VS Code
```
