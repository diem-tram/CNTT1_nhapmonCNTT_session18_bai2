# Bài 2 : Sự cố phiên làm việc trên hệ thống vận tải
Phần 1
Cache : Lưu trữ tài nguyên tĩnh (hình ảnh, CSS, JS) trên trình duyệt để tăng tốc độ tải trang.
Cookies: Lưu trữ token định danh ngắn gọn và tự động gửi kèm trong mọi HTTP Request.
Phần 2
HTTP
Set-Cookie: shipper_token=eyJhbGci...; Max-Age=2592000; Path=/; Domain=vantaics.vn; Secure; HttpOnly; SameSite=Strict
Token định danh: Là "thẻ tên" mã hóa của shipper. Máy chủ nhìn vào đây để biết bạn là ai mà không cần bắt đăng nhập lại khi load lại trang hay tắt trình duyệt.
Thời gian sống:Quy định cookie này sống trong 30 ngày. Nhờ vậy, giỏ hàng và phiên đăng nhập được giữ lại lâu dài  chứ không bị mất ngay khi đóng web.
HttpOnly:Khóa cửa không cho mã JavaScript của hacker (lỗ hổng XSS) trộm mất token.
Phần 3
Khi giao diện mới cập nhật nhưng trình duyệt vẫn hiển thị màu sắc/bố cục cũ, tiến hành Hard Reload bằng một trong hai cách:
Thao tác chuột: Mở F12 →Nhấn giữ chuột trái vào nút Refresh (Tải lại) trên trình duyệt →Chọn "Empty Cache and Hard Reload".
