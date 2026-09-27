# ĐỒ ÁN CỔNG ĐĂNG KÝ HỌC PHẦN VÀ BẢO MẬT BẰNG CẤP

- **Sinh viên thực hiện:** Vũ Thế Anh
- **Mã số sinh viên:** K235480106004
- **Tên miền dịch vụ:** `portal.vutheanh.id.vn` & `sec.vutheanh.id.vn`
- **Hạ tầng:** Ubuntu 24.04 (WSL2), Docker Compose, Nginx Reverse Proxy, Node-RED, MariaDB

---

## 🌐 DEMO HỆ THỐNG TRỰC TUYẾN

* **Website 1 (Cổng Đăng ký Học phần):** [http://portal.vutheanh.id.vn](http://portal.vutheanh.id.vn)
* **API Endpoint Học phần (JSON):** [http://portal.vutheanh.id.vn/api/benh-nhan](http://portal.vutheanh.id.vn/api/benh-nhan)
* **Website 2 (Cổng Mã hóa & Chữ ký số AES/RSA):** [http://sec.vutheanh.id.vn](http://sec.vutheanh.id.vn)

---

## 📊 SƠ ĐỒ KIẾN TRÚC CHUYỂN TIẾP (MERMAID DIAGRAM)

```mermaid
graph TD
    Client[Client / Browser] -->|HTTP| Nginx[Nginx Reverse Proxy - Port 80]
    
    Nginx -->|portal.vutheanh.id.vn| Site1[Website 1: Cổng Đăng ký Học phần]
    Site1 -->|/api/benh-nhan| NodeRED[Node-RED Backend API - Port 1880]
    
    Nginx -->|sec.vutheanh.id.vn| Site2[Website 2: Cổng Bảo mật Đồ án & RSA]
