# MailTQR · QR Pocket Delivery Studio

Ứng dụng HTML cho điện thoại và máy tính, xử lý danh sách ngay trên thiết bị.

## Sử dụng

1. Mở `index.html` bằng trình duyệt, hoặc mở địa chỉ GitHub Pages sau khi bật hosting.
2. Dán danh sách dạng `email|mật khẩu|`, tiếp theo là dòng email phụ. App chỉ nhận các dòng có dấu `|`, bỏ qua dòng email phụ không có dấu `|`.
3. Nhập tên shop và lời nhắn cho khách.
4. Tạo gói bàn giao. Mỗi tài khoản có trang nhận với Copy email / Copy mật khẩu, xuất HTML riêng; có thể xuất HTML tổng để giao cả lô.
5. Muốn tạo QR mở trang, nhập URL HTTPS trỏ đến chính app đang chạy. Khi mở app trên HTTPS, ô URL tự điền.

## GitHub Pages

Vào Settings → Pages. Nếu tài khoản/gói GitHub cho phép Pages với repository Private, chọn Deploy from a branch → main → /(root) → Save. Nếu không, cần gói hỗ trợ hoặc chủ repository tự quyết định đổi visibility. Không tự đổi repository thành Public.

Địa chỉ dự kiến khi dùng Pages mặc định: https://vn8690-create.github.io/MailTQR/ (chỉ hoạt động sau khi Pages được bật và triển khai thành công).

## Dữ liệu và giới hạn

- Source không chứa danh sách khách thật. Không commit HTML bàn giao đã chứa tài khoản hoặc ảnh QR của khách.
- Dữ liệu nhận nằm trong phần `#delivery=` của URL. Base64url chỉ đóng gói dữ liệu, không mã hóa bảo mật. Ai có link hoặc QR đều có thể đọc tài khoản.
- Không có máy chủ lưu tài khoản, đăng nhập quản trị, hết hạn, thu hồi link hoặc thống kê lượt xem. Copy không tự đăng nhập dịch vụ.
- Dùng tối đa 100 tài khoản mỗi lần. Dấu `|` tiếp theo kết thúc mật khẩu; không hỗ trợ mật khẩu chứa dấu `|`.
- HTML riêng chạy offline trong trình duyệt hỗ trợ JavaScript. Chức năng clipboard có dự phòng sao chép thủ công.

Bộ tạo QR nhúng sử dụng mã nguồn của Kazuhiko Arase; thông báo bản quyền và giấy phép MIT được giữ trong index.html.
