# BÁO CÁO LÝ THUYẾT VÀ KIẾN TRÚC HỆ THỐNG THƯ VIỆN SỐ

- **Họ và tên:** Vũ Thế Anh
- **Mã số sinh viên:** K235480106004
- **Tên miền dịch vụ:** `vutheanh.id.vn`

---

## 1. Hạ tầng Đóng gói Container với Docker Compose
Dự án vận hành 3 dịch vụ nền tảng kết nối qua mạng nội bộ `app_net`:
1. **Nginx Reverse Proxy (`nginx_vutheanh`):** Điều hướng truy cập từ tên miền `s1.vutheanh.id.vn` và `s2.vutheanh.id.vn` vào các thư mục web tương ứng.
2. **Node-RED Backend (`nodered_vutheanh`):** Xử lý luồng dữ liệu API trả về danh mục sách và tình trạng mượn/trả.
3. **MariaDB Database (`mariadb_vutheanh`):** Lưu trữ thông tin tài liệu và thẻ thư viện độc giả.

---

## 2. API Node-RED Tra cứu Sách Thư viện (`/api/benh-nhan`)
API tiếp nhận yêu cầu từ client, trả về danh sách sách kèm trạng thái mượn và mức phí đặt cọc:
- **Độc giả VIP:** Miễn phí đặt cọc mượn sách ($0 \text{ VNĐ}$).
- **Độc giả Thường:** Phụ thu đặt cọc từ $50.000 \text{ VNĐ} - 100.000 \text{ VNĐ}$.
