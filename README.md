# maintenance
Bảo trì nâng cấp

# Trang Bảo Trì / Nâng Cấp Hệ Thống

## Mục đích
File `maintenance.html` này được dùng để thay thế tạm thời trang chủ khi hệ thống đang:
- Bảo trì định kỳ
- Nâng cấp phiên bản mới
- Xử lý sự cố nghiêm trọng
- Migrate dữ liệu, chuyển server, v.v.

Hiện tại **chưa ấn định thời gian hoàn thành chính xác**, vì vậy trang sẽ hiển thị thông báo chung chung thay vì đồng hồ đếm ngược cố định.

## Cách sử dụng

1. Đổi tên file thành `index.html` (hoặc đặt làm trang mặc định của server)
2. Upload lên hosting / server (có thể để ở thư mục gốc)
3. Hoặc cấu hình web server redirect tất cả request về file này:

   **Nginx example:**
   ```nginx
   server {
       listen 80;
       server_name yourdomain.com;

       location / {
           return 307 /maintenance.html;
       }
   }
