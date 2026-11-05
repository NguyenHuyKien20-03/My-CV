# Nhật ký thay đổi do AI thực hiện

Ghi lại tại đây khi có thay đổi lớn ảnh hưởng đến chức năng, giao diện, cấu trúc hoặc tài liệu quan trọng của dự án. Không cần ghi các chỉnh sửa nhỏ như sửa lỗi chính tả hay định dạng.

Mỗi mục nên nêu ngày, nội dung thay đổi, các tệp liên quan và kết quả kiểm tra. Thêm mục mới lên đầu nhật ký.

## 05/11/2026 — Bổ sung minh chứng kiểm thử responsive

- **Nội dung:** Chụp giao diện bằng Microsoft Edge headless ở viewport mobile (390×844), tablet (820×1180) và desktop (1440×1000); cập nhật báo cáo kiểm thử với liên kết minh chứng và ghi nhận lỗi nội dung hero bị cắt ngang trên mobile.
- **Tệp liên quan:** `docs/test_report.md`, `docs/screenshots/responsive-mobile.png`, `docs/screenshots/responsive-tablet.png`, `docs/screenshots/responsive-desktop.png`.
- **Kết quả:** Ba ảnh PNG đã lưu và xác nhận đúng kích thước viewport. Cần sửa lỗi responsive mobile và kiểm thử lại trước nghiệm thu.

## 05/11/2026 — Ghi nhận phiên bản nền v1.0.0

- **Phạm vi:** Website CV/portfolio tĩnh, responsive.
- **Nội dung:** Hiển thị thông tin cá nhân, kỹ năng, dự án và liên hệ; hỗ trợ điều hướng giữa các mục và bố cục trên nhiều kích thước màn hình.
- **Tệp liên quan:** `index.html`, `assets/css/styles.css`.
- **Nguồn ghi nhận:** Tóm tắt từ `docs/RELEASENOTE.md` và `readme.md`; đây là ghi nhận phiên bản nền, không phải thay đổi được thực hiện trong phiên làm việc này.