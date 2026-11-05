# BÁO CÁO KIỂM THỬ SẢN PHẨM

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| **Tên dự án** | Nguyễn Huy Kiên — Portfolio CV |
| **Phiên bản** | v1.0.0 (theo `docs/RELEASENOTE.md`) |
| **Ngày lập báo cáo** | 05/11/2026 |
| **Ngày kiểm thử** | 05/11/2026 — rà soát mã nguồn tĩnh và kiểm tra giao diện responsive |
| **Người thực hiện/đánh giá** | Chưa xác định — điền tên người nghiệm thu |
| **Phạm vi** | Rà soát HTML/CSS, tài liệu bàn giao và ảnh giao diện responsive trên Edge |
| **Môi trường** | Microsoft Edge headless; viewport mô phỏng 390×844 (mobile), 820×1180 (tablet), 1440×1000 (desktop) |
| **Loại báo cáo** | Đánh giá sơ bộ trước bàn giao; responsive được kiểm tra bằng viewport mô phỏng, chưa kiểm tra trên thiết bị vật lý |

### Quy ước trạng thái

- **Đạt:** Có thể xác nhận từ phạm vi kiểm tra đã thực hiện.
- **Chưa đạt:** Có lỗi hoặc yêu cầu chưa được đáp ứng.
- **Cần cải thiện:** Có cơ sở triển khai nhưng cần hoàn thiện, làm rõ hoặc xác nhận thêm.
- **Chưa kiểm thử:** Chưa có kết quả chạy thực tế hoặc minh chứng để kết luận.

> Báo cáo gồm rà soát mã nguồn tĩnh và chụp giao diện trên Edge ở ba kích thước viewport mô phỏng. Kết quả này không thay thế kiểm thử trên thiết bị vật lý hoặc các trình duyệt khác; các mục “Chưa kiểm thử” cần được cập nhật sau khi có minh chứng tương ứng.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---:|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | **Cần cải thiện** | Các khu vực nội dung và liên kết điều hướng được khai báo; liên kết dự án còn là `#`, nút gửi biểu mẫu chưa có xử lý. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | **Cần cải thiện** | Đã chụp ở ba viewport Edge; ảnh mobile cho thấy nội dung mô tả hero bị cắt ngang. Chưa kiểm tra trên thiết bị vật lý hoặc trình duyệt khác. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | **Chưa kiểm thử** | Tài liệu có hướng dẫn chạy tĩnh; chưa chạy thử, đo hiệu năng hoặc kiểm tra tình huống lỗi/tài nguyên ngoài mạng. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | **Cần cải thiện** | Trang tĩnh, không thấy luồng backend trong phạm vi rà soát; cần xác nhận rủi ro riêng tư từ liên kết và tài nguyên bên thứ ba. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | **Cần cải thiện** | Có tách HTML/CSS và tài liệu cơ bản; còn chuỗi `ff` thừa, nội dung mẫu/placeholder và cây thư mục trong README chưa phản ánh thư mục `docs/`. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | **Cần cải thiện** | Đã lưu minh chứng responsive mobile/tablet/desktop; chưa xác nhận triển khai thực tế hoặc hoàn tất các kiểm thử khác. |

## 3. Chi tiết kiểm tra

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| F-01 | Có các khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ | **Đạt** | Các section tương ứng được khai báo trong `index.html`; đây là kết quả rà soát mã nguồn, chưa xác nhận trên trình duyệt. |
| F-02 | Menu điều hướng trỏ đến đúng khu vực trên trang | **Cần cải thiện** | Các liên kết `#about`, `#skills`, `#projects`, `#contact` khớp ID section. Tuy nhiên, có chuỗi `ff` thừa ngay sau phần mở đầu của thẻ điều hướng. |
| F-03 | Nút hành động trong phần giới thiệu đưa người dùng đến đúng nội dung | **Đạt** | Liên kết “Xem dự án” và “Liên hệ tôi” lần lượt trỏ đến `#projects` và `#contact`. Chưa thử thao tác thực tế. |
| F-04 | Liên kết chi tiết của từng dự án hoạt động và dẫn đến đích phù hợp | **Chưa đạt** | Cả bốn thẻ dự án đang dùng `href="#"`; cần thay bằng URL thật hoặc trình bày rõ đây là nội dung chưa có liên kết. |
| F-05 | Biểu mẫu liên hệ có hành vi gửi được công bố rõ ràng | **Cần cải thiện** | README và ghi chú phát hành nêu trang không gửi email; trong `index.html`, nút “Gửi” là `type="button"` và không thấy xử lý gửi. Nên bỏ form/nút hoặc ghi rõ trạng thái chưa hoạt động. |
| F-06 | Nội dung hồ sơ đúng với thông tin được duyệt trước bàn giao | **Cần cải thiện** | Tiêu đề hiển thị “Nguyễn Huy Kiên 321” và vai trò “Superracisc & Student”; cần chủ sản phẩm xác nhận/chỉnh nội dung cuối cùng. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| UI-01 | Bố cục có các breakpoint cho điện thoại, máy tính bảng và máy tính để bàn | **Đạt** | CSS có bố cục mobile-first, breakpoint từ 768px và 1280px; đã chụp giao diện ở viewport 390×844, 820×1180 và 1440×1000 (xem các minh chứng bên dưới). |
| UI-02 | Menu, thẻ dự án và nội dung không tràn hoặc chồng lấp trên màn hình nhỏ | **Chưa đạt** | Ở viewport mobile 390×844, dòng mô tả trong hero vượt quá vùng hiển thị và bị cắt ngang. Xem ảnh [mobile](screenshots/responsive-mobile.png); đối chiếu [tablet](screenshots/responsive-tablet.png) và [desktop](screenshots/responsive-desktop.png). Cần sửa bố cục mobile và kiểm tra lại, bao gồm chiều rộng 320–375px. |
| UI-03 | Ảnh đại diện và ảnh dự án tải đúng, có văn bản thay thế | **Cần cải thiện** | Ảnh có thuộc tính `alt`, nhưng ảnh dự án lấy từ các URL bên ngoài; chưa xác minh trạng thái tải hoặc phương án khi mất mạng. |
| UI-04 | Điều khiển có thể sử dụng bằng bàn phím và trạng thái focus dễ nhận biết | **Cần cải thiện** | CSS có `:focus-visible`; riêng input có quy tắc `:focus` đặt `outline: none`. Cần kiểm tra trực tiếp bằng bàn phím và xác nhận chỉ báo focus rõ ràng. |
| UI-05 | Màu sắc, độ tương phản và nội dung hiển thị nhất quán | **Cần cải thiện** | CSS dùng màu viền `#2CFF05`; chú thích biến màu nhấn chưa khớp với giá trị màu. Cần duyệt lại palette/độ tương phản và xác nhận nội dung cuối. |
| UI-06 | Trải nghiệm cuộn và chuyển động tôn trọng tùy chọn giảm chuyển động | **Đạt** | CSS khai báo `prefers-reduced-motion: reduce`; chưa kiểm tra trên trình duyệt có bật tùy chọn này. |
| UI-07 | Hoạt động nhất quán trên các trình duyệt mục tiêu | **Chưa kiểm thử** | Chưa có kết quả kiểm thử Chrome, Edge, Firefox hoặc Safari. |

#### Minh chứng chụp màn hình responsive

Ảnh được chụp bằng Microsoft Edge headless tại các viewport mô phỏng sau; đây là ảnh kiểm thử giao diện, không phải ảnh chụp thiết bị vật lý.

| Thiết bị mô phỏng | Viewport | Minh chứng |
|---|---:|---|
| Mobile | 390×844 | [responsive-mobile.png](screenshots/responsive-mobile.png) |
| Tablet | 820×1180 | [responsive-tablet.png](screenshots/responsive-tablet.png) |
| Desktop | 1440×1000 | [responsive-desktop.png](screenshots/responsive-desktop.png) |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| OP-01 | Có thể mở trang trực tiếp hoặc phục vụ bằng máy chủ tĩnh theo hướng dẫn | **Chưa kiểm thử** | README hướng dẫn mở `index.html` và chạy `python -m http.server`; chưa thực hiện chạy thử trong lần rà soát này. |
| OP-02 | CSS và ảnh nội bộ được tải đúng khi triển khai | **Chưa kiểm thử** | Cần kiểm tra tab Network/Console sau khi mở bằng máy chủ tĩnh; CSS được liên kết tại `./assets/css/styles.css`, ảnh đại diện tại `./assets/img/avatar.jpg`. |
| OP-03 | Trang vẫn dùng được khi tài nguyên ảnh bên ngoài không khả dụng | **Cần cải thiện** | Ảnh dự án phụ thuộc Internet; chưa thấy ảnh dự phòng hoặc thông điệp thay thế trong mã nguồn. |
| OP-04 | Liên kết và điều hướng không gây lỗi hoặc đưa người dùng đến vị trí ngoài dự kiến | **Cần cải thiện** | Liên kết dự án `href="#"` có thể chỉ đưa trang về đầu; cần thay bằng đích thực hoặc bỏ hành động. |
| OP-05 | Thời gian tải và hiệu năng cơ bản đạt yêu cầu bàn giao | **Chưa kiểm thử** | Chưa có phép đo Lighthouse/Web Vitals hoặc tiêu chí hiệu năng được thống nhất. |
| OP-06 | Có thông báo lỗi phù hợp khi thao tác không được hỗ trợ | **Chưa kiểm thử** | Chưa có kiểm thử tương tác thực tế; nếu form không được hỗ trợ, giao diện cần nói rõ thay vì tạo kỳ vọng rằng nút Gửi hoạt động. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| SEC-01 | Không yêu cầu cấu hình bí mật hoặc khóa API để chạy website | **Đạt** | README mô tả website không cần biến môi trường hay khóa API; dự án được mô tả là website tĩnh. |
| SEC-02 | Dữ liệu người dùng được thu thập, lưu trữ và xử lý đúng như mô tả | **Cần cải thiện** | README nói không lưu trữ dữ liệu và không gửi email. Cần xác nhận form hiển thị hiện tại không gây hiểu nhầm rằng email sẽ được gửi/lưu. |
| SEC-03 | Liên kết và nội dung bên thứ ba được xem xét trước khi công khai | **Cần cải thiện** | Có liên kết mạng xã hội và ảnh từ `i.pinimg.com`; cần chủ sản phẩm xác minh đích liên kết, quyền sử dụng và mức độ phù hợp trước bàn giao. |
| SEC-04 | Trang không để lộ thông tin nhạy cảm ngoài nội dung liên hệ được chủ sở hữu duyệt | **Chưa kiểm thử** | Chưa có xác nhận của chủ sở hữu về phạm vi thông tin cá nhân được phép công khai. |
| SEC-05 | Kiểm tra bảo mật chuyên sâu cho máy chủ/API | **Chưa kiểm thử** | Báo cáo này không thực hiện kiểm thử xâm nhập; phạm vi hiện tại là giao diện tĩnh và không xác nhận bảo mật hạ tầng lưu trữ. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| Q-01 | HTML và CSS được tổ chức thành các tệp riêng, có cấu trúc dễ theo dõi | **Đạt** | Trang chính nằm trong `index.html`, stylesheet tách tại `assets/css/styles.css`; mã nguồn dùng các section và class theo khu vực. |
| Q-02 | Không còn văn bản kiểm tra, nội dung mẫu hoặc placeholder trước bàn giao | **Chưa đạt** | Phát hiện `ff` trong menu, “321” ở tiêu đề, vai trò “Superracisc & Student”, và các liên kết dự án `href="#"`. Cần chủ sản phẩm duyệt nội dung trước khi sửa các giá trị này. |
| Q-03 | README phản ánh đúng cấu trúc repository hiện tại | **Cần cải thiện** | Cây thư mục trong `readme.md` chưa liệt kê `docs/` (bao gồm release note và báo cáo kiểm thử). |
| Q-04 | Hướng dẫn sử dụng, yêu cầu môi trường và giới hạn sản phẩm được nêu rõ | **Đạt** | README mô tả website tĩnh, yêu cầu môi trường, cách chạy Python/Docker và giới hạn không có backend/gửi email. Cần đồng bộ mô tả form với giao diện hiện tại. |
| Q-05 | Mã nguồn đã qua kiểm tra tự động về HTML/CSS và không có lỗi console | **Chưa kiểm thử** | Chưa chạy validator/linter và chưa kiểm tra Console trên trình duyệt. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| ID | Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|---|
| DEP-01 | Có quy trình triển khai phù hợp với website tĩnh | **Cần cải thiện** | README có hướng dẫn chạy Python và Docker/Nginx; chưa chạy thử để xác nhận lệnh, đường dẫn và quyền truy cập trên môi trường bàn giao. |
| DEP-02 | Có thể triển khai mà không cần bước build hoặc cài dependency dự án | **Đạt** | Tài liệu nêu rõ không dùng framework/package manager/bước biên dịch; cần xác minh lại khi thực thi trên máy bàn giao. |
| DEP-03 | Có kế hoạch kiểm thử thủ công cho luồng chính | **Cần cải thiện** | Báo cáo có checklist và ảnh kiểm tra responsive; chưa có biên bản kiểm tra thao tác/luồng chính hoặc người nghiệm thu xác nhận. |
| DEP-04 | Có kết quả kiểm thử tự động hoặc xác nhận rõ phạm vi không áp dụng | **Cần cải thiện** | Chưa thấy bộ kiểm thử tự động trong tài liệu được rà soát. Với website tĩnh, cần ghi rõ kiểm tra nào làm thủ công và lưu kết quả. |
| DEP-05 | Có ảnh chụp màn hình/log làm minh chứng cho bản bàn giao | **Đạt** | Đã lưu [ảnh mobile](screenshots/responsive-mobile.png), [ảnh tablet](screenshots/responsive-tablet.png) và [ảnh desktop](screenshots/responsive-desktop.png) tại `docs/screenshots/`; ảnh chụp ngày 05/11/2026 bằng Edge headless. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm có cấu trúc nền tảng phù hợp với một website CV/portfolio tĩnh: nội dung được chia theo khu vực, CSS tách riêng, có breakpoint responsive và README hướng dẫn chạy bằng máy chủ tĩnh. Giao diện đã được chụp trên Edge ở ba viewport mô phỏng; ảnh mobile cho thấy mô tả hero bị cắt ngang. Chưa kiểm thử trên thiết bị vật lý, trình duyệt khác hoặc môi trường triển khai.

**Trạng thái sẵn sàng bàn giao: Chưa đủ cơ sở để nghiệm thu cuối cùng.** Cần xử lý các mục chưa đạt, chủ sở hữu duyệt nội dung/liên kết, sau đó chạy kiểm thử thực tế và cập nhật minh chứng trước khi xác nhận bàn giao.

### Vấn đề cần xử lý trước khi nghiệm thu

1. Xóa chuỗi `ff` thừa khỏi điều hướng và xác nhận lại nội dung tiêu đề/vai trò trong `index.html`.
2. Sửa lỗi tràn/cắt nội dung mô tả ở viewport mobile; kiểm tra lại ở 320–375px và xác nhận ảnh sau sửa.
3. Thay các liên kết dự án `href="#"` bằng đích thật hoặc bỏ liên kết nếu dự án chưa có trang chi tiết.
4. Quyết định rõ hành vi của biểu mẫu: nếu không gửi dữ liệu, bỏ nút/form hoặc hiển thị giải thích rõ ràng; nếu cần gửi, xác định và kiểm thử giải pháp phù hợp.
5. Kiểm tra ảnh ngoài, liên kết mạng xã hội, nội dung cá nhân và quyền sử dụng tài nguyên trước khi công khai.
6. Đồng bộ cây thư mục trong README với repository hiện tại; duyệt lại màu sắc/độ tương phản và trạng thái focus bàn phím.
7. Chạy thử trên thiết bị vật lý và các trình duyệt mục tiêu, kiểm tra Console/Network và lưu kết quả hoặc ảnh minh chứng bổ sung.

### Điều kiện đề xuất để ký nghiệm thu

- Không còn lỗi chức năng mức nghiêm trọng; liên kết và hành động hiển thị có đích/hành vi đúng.
- Nội dung CV, thông tin liên hệ và tài nguyên được chủ sở hữu duyệt.
- Các mục **Chưa kiểm thử** trong sáu nhóm đã được chạy hoặc được xác nhận không áp dụng kèm lý do.
- Báo cáo được cập nhật trạng thái cuối cùng, người đánh giá, môi trường và đường dẫn minh chứng.

## 5. Xác nhận

| Vai trò | Họ tên | Ngày | Ký xác nhận |
|---|---|---|---|
| Người kiểm thử |  |  |  |
| Người đánh giá/nghiệm thu |  |  |  |
| Đại diện chủ sản phẩm |  |  |  |