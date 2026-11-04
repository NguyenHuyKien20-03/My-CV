# Nguyễn Huy Kiên — Portfolio CV

Trang hồ sơ cá nhân (CV/portfolio) giới thiệu Nguyễn Huy Kiên, các kỹ năng, dự án tiêu biểu và thông tin liên hệ. Giao diện được xây dựng theo hướng responsive, ưu tiên trải nghiệm trên điện thoại và mở rộng bố cục cho máy tính bảng, máy tính để bàn.

## Chức năng

- Hiển thị phần giới thiệu, vai trò và ảnh đại diện.
- Trình bày danh sách kỹ năng và các dự án mẫu.
- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Cung cấp các liên kết mạng xã hội và nút quay về đầu trang.
- Tự điều chỉnh bố cục theo kích thước màn hình bằng CSS.

> Đây là website tĩnh. Trang hiện không có backend, không xử lý lưu trữ dữ liệu và không gửi email từ biểu mẫu liên hệ. Một số ảnh minh họa dự án được tải từ Internet.

## Công nghệ

- HTML5.
- CSS3: Flexbox, CSS Grid, custom properties, media queries và responsive design.
- Không sử dụng framework, package manager hoặc bước biên dịch.

## Cấu trúc dự án

```text
My-CV/
├── index.html
├── readme.md
└── assets/
    ├── css/
    │   └── styles.css
    └── img/
        └── avatar.jpg
```

## Yêu cầu môi trường

- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Để mở trực tiếp: không cần cài thêm phần mềm.
- Để chạy máy chủ cục bộ: Python 3 (hoặc một máy chủ tĩnh tương đương).
- Để chạy bằng Docker: Docker Engine hoặc Docker Desktop đang hoạt động.
- Kết nối Internet nếu muốn tải ảnh minh họa từ các địa chỉ bên ngoài.

Không cần cài Node.js/npm vì dự án không có dependencies hoặc bước build.

## Cài đặt

Tải hoặc sao chép repository về máy, sau đó mở terminal tại thư mục dự án:

```bash
git clone https://github.com/NguyenHuyKien20-03/My-CV.git
cd My-CV
```

Nếu đã có mã nguồn trên máy, chỉ cần mở terminal tại thư mục chứa `index.html`.

## Cấu hình và tùy chỉnh

Website không yêu cầu file cấu hình, biến môi trường hay khóa API.

- Chỉnh nội dung giới thiệu, kỹ năng, dự án, liên kết liên hệ và tiêu đề trang trong `index.html`.
- Thay ảnh đại diện tại `assets/img/avatar.jpg` hoặc cập nhật đường dẫn ảnh trong `index.html`.
- Tùy chỉnh màu sắc, kiểu chữ, khoảng cách và breakpoint responsive trong `assets/css/styles.css`.
- Các ảnh dự án hiện tham chiếu đến URL bên ngoài; để sử dụng ngoại tuyến, tải ảnh về thư mục `assets/img/` rồi cập nhật đường dẫn tương ứng.

## Chạy thử

### Windows

**Mở trực tiếp:** dùng File Explorer mở `index.html` bằng trình duyệt.

**Chạy máy chủ cục bộ bằng Python:** mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có nhưng đã cài Python, dùng:

```powershell
python -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000). Nhấn `Ctrl+C` trong PowerShell để dừng máy chủ.

### macOS

Mở Terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Truy cập [http://localhost:8000](http://localhost:8000). Nhấn `Control+C` để dừng máy chủ.

### Linux

Mở terminal tại thư mục dự án và chạy:

```bash
python3 -m http.server 8000
```

Truy cập [http://localhost:8000](http://localhost:8000). Nhấn `Ctrl+C` để dừng máy chủ.

Nếu cổng `8000` đang được sử dụng, thay `8000` trong lệnh bằng một cổng khác, ví dụ `8080`, rồi truy cập đúng cổng đó.

### Docker (Windows, macOS, Linux)

Cài đặt và khởi động Docker Desktop (Windows/macOS) hoặc Docker Engine (Linux). Tại thư mục dự án, chạy container Nginx để phục vụ các file tĩnh:

**PowerShell (Windows):**

```powershell
docker run --rm --name my-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS/Linux:**

```bash
docker run --rm --name my-cv -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Mở [http://localhost:8080](http://localhost:8080). Lần chạy đầu tiên Docker có thể cần tải image `nginx:alpine` từ Internet. Nhấn `Ctrl+C` trong terminal để dừng và xóa container.

## Thông tin liên hệ

- **GitHub:** [NguyenHuyKien20-03](https://github.com/NguyenHuyKien20-03)
- **Facebook:** [Trang cá nhân](https://www.facebook.com/share/1DvXrJbWRL/?mibextid=wwXIfr)
- **Discord:** [Máy chủ Discord](https://discord.gg/7tmRDAwRz8)

## Bản quyền

© 2026 Nguyễn Huy Kiên.