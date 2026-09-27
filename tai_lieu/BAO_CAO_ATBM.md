# BÁO CÁO BẢO MẬT VÀ MÃ HÓA TÀI LIỆU THƯ VIỆN SỐ

- **Họ và tên:** Vũ Thế Anh
- **Mã số sinh viên:** K235480106004

---

## 1. Thuật toán Mã hóa Khối DES & AES-256
- **DES:** Cấu trúc mạng Feistel 64-bit, kích thước khóa 56-bit, thực hiện 16 vòng hoán vị/thế.
- **AES-256:** Cấu trúc SPN 128-bit block, khóa 256-bit (14 vòng biến đổi `SubBytes`, `ShiftRows`, `MixColumns`, `AddRoundKey`). Ứng dụng để bảo vệ nội dung tài liệu bản quyền.

---

## 2. Mã hóa Bất đối xứng RSA & Chữ ký số Bằng cấp
- **Khóa Public/Private:** $PU = (e, n)$, $PR = (d, n)$.
- **Mã hóa:** $C = M^e \pmod n$.
- **Giải mã:** $M = C^d \pmod n$.
- **Ứng dụng:** Ký số xác minh tính toàn vẹn của bằng cấp và thẻ thư viện điện tử.
