# VEO 3 Video Generator

Ứng dụng desktop chuyên nghiệp để tạo video AI sử dụng công nghệ VEO 3, được xây dựng bằng Electron.js với giao diện tiếng Việt thân thiện.

## Tính năng chính

### 🎬 Tạo Video AI
- Tạo video từ prompt text với công nghệ VEO 3
- Hỗ trợ đa luồng xử lý (tối đa 10 luồng)
- Cài đặt chất lượng video: HD, Full HD, 4K
- Điều chỉnh độ dài video (1-30 giây)
- Import danh sách prompt từ file TXT
- Chọn prompt muốn tạo video với checkbox

### 🍪 Quản lý Cookie
- Thêm, sửa, xóa cookie
- Kiểm tra trạng thái và credit của cookie
- Chọn cookie cho từng lần tạo video
- Theo dõi lịch sử sử dụng cookie
- Import/Export danh sách cookie

### 📱 Thư viện Video
- Xem danh sách video đã tạo
- Thumbnail và thông tin chi tiết
- Phát video, mở thư mục chứa file
- Tìm kiếm và lọc video theo thời gian
- Xóa video không cần thiết
- Xuất danh sách video

### 🔐 Quản lý License
- Kiểm tra license với mã máy tính
- Kích hoạt license key
- Theo dõi thời hạn license
- Cảnh báo khi license sắp hết hạn

### ⚙️ Cài đặt
- Chọn thư mục lưu video
- Cài đặt API endpoint và timeout
- Tự động tải video khi hoàn thành
- Kiểm tra cập nhật tự động
- Thu nhỏ vào system tray
- Xuất/Nhập cài đặt

### 🌐 Google Labs Projects
- Kết nối và đồng bộ với Google Labs
- Xem danh sách projects và video
- Quản lý video theo từng project
- Tải xuống video từ projects
- Tạo video mới trong project

### 🤖 ChatGPT AI Assistant
- Tích hợp ChatGPT để tạo prompt
- Hỗ trợ GPT-3.5 và GPT-4
- Lịch sử chat và context
- Template prompt có sẵn
- Xuất prompt về generator

### 📊 Dashboard
- Thống kê tổng quan
- Hoạt động gần đây  
- Truy cập nhanh các chức năng
- Hiển thị credit còn lại
- Loading screen với progress bar

## Cài đặt

### Yêu cầu hệ thống
- Windows 10/11, macOS 10.14+, hoặc Linux
- RAM: 4GB trở lên
- Dung lượng: 500MB trống
- Kết nối Internet

### Cài đặt từ source
```bash
# Clone repository
git clone https://github.com/suncodevn/veo3-generator.git
cd video-generator

# Cài đặt dependencies
npm install

# Chạy ứng dụng
npm start

# Build ứng dụng
npm run build
```

### Cài đặt từ file binary
1. Tải file installer từ [Releases](https://github.com/suncodevn/veo3-generator/releases)
2. Chạy file installer
3. Làm theo hướng dẫn cài đặt

## Sử dụng

### Lần đầu sử dụng
1. **Kích hoạt License**: Nhập license key tại trang Cài đặt
2. **Thêm Cookie**: Thêm cookie VEO 3 tại trang Cookie  
3. **Cài đặt thư mục**: Chọn thư mục lưu video tại trang Cài đặt
4. **Tạo video đầu tiên**: Vào trang Tạo Video và bắt đầu

### Tạo video
1. Chọn cookie có credit
2. Nhập prompt mô tả video hoặc import từ file TXT
3. Chọn các prompt muốn tạo video
4. Cài đặt chất lượng và độ dài
5. Thiết lập số luồng xử lý
6. Nhấn "Bắt đầu tạo video"

### Quản lý cookie
1. Lấy cookie từ trình duyệt khi đăng nhập VEO 3
2. Thêm cookie vào ứng dụng với tên và số credit
3. Kiểm tra trạng thái cookie định kỳ
4. Sử dụng cookie có credit > 0 để tạo video

## Phím tắt

- `Ctrl+1`: Trang chủ
- `Ctrl+2`: Tạo video  
- `Ctrl+3`: Thư viện
- `Ctrl+4`: Google Labs Projects
- `Ctrl+5`: Cookie
- `Ctrl+6`: Cài đặt
- `Ctrl+R`: Tải lại trang
- `Ctrl+Shift+I`: Mở DevTools

## Cấu trúc thư mục

```
veo3-video-generator/
├── main.js                 # Main process Electron
├── package.json            # Package configuration
├── assets/                 # App icons and assets
├── src/                    # Source code
│   ├── index.html          # Main HTML file
│   ├── css/
│   │   └── style.css       # Custom styles
│   └── js/
│       ├── app.js                    # Main application logic
│       ├── video-generator.js        # Video generation module
│       ├── cookie-manager.js         # Cookie management
│       ├── gallery.js                # Video gallery
│       ├── google-labs-projects.js   # Google Labs projects integration
│       ├── chatgpt-assistant.js      # ChatGPT AI assistant
│       ├── settings.js               # Settings management
│       └── license.js                # License management
└── dist/                   # Build output
```


## Xử lý sự cố

### Video không tạo được
- Kiểm tra kết nối Internet
- Xác nhận cookie còn credit
- Thử giảm số luồng xử lý
- Kiểm tra API endpoint trong cài đặt

### Cookie không hoạt động
- Đăng nhập lại VEO 3 để lấy cookie mới
- Kiểm tra định dạng cookie
- Xóa cookie cũ không dùng

### License không kích hoạt được
- Kiểm tra kết nối Internet
- Xác nhận license key chính xác
- Liên hệ support nếu vẫn lỗi

## Cập nhật

Ứng dụng sẽ tự động kiểm tra cập nhật khi khởi động (nếu bật trong cài đặt). Khi có bản cập nhật mới, sẽ hiện popup thông báo.

Để tự động cập nhật:
1. Nhấn "Cập nhật ngay" trong popup
2. Ứng dụng sẽ tải và cài đặt tự động
3. Khởi động lại để sử dụng phiên bản mới

## Hỗ trợ

- Email: ngockushinfo@gmail.com
- Website: https://suncodevn.com

## License

Copyright © 2025 SUNCODEVN. All rights reserved.

Ứng dụng này yêu cầu license hợp lệ để sử dụng. Vui lòng liên hệ để mua license tại https://suncodevn.com

## Changelog

### v1.0.0 (2025-01-01)
- Phiên bản đầu tiên
- Tính năng tạo video AI đa luồng
- Quản lý cookie và license
- Thư viện video với đầy đủ chức năng
- Giao diện tiếng Việt chuyên nghiệp

---

Được phát triển với ❤️ bởi SUNCODEVN