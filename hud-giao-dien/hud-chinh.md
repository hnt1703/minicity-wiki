# HUD Chính

HUD chính hiển thị tất cả thông tin quan trọng về nhân vật và môi trường.

## Các Thanh Trạng Thái

### 1. Thanh Máu (Health)

- **Hiển thị:** Thanh màu đỏ ở góc dưới bên trái
- **Ý nghĩa:** Sức khỏe hiện tại
- **Khi thấp:** Nhân vật sẽ yếu đi, có thể gục khi về 0
- **Phục hồi:** Sử dụng băng gạc, morphine, đến bệnh viện hồi phục

### 2. Thanh Đói (Hunger)

- **Hiển thị:** Thanh màu cam ở góc dưới bên trái
- **Ý nghĩa:** Mức độ no của nhân vật
- **Khi thấp:** Nhân vật mệt mỏi, giảm máu dần khi về 0
- **Phục hồi:** Ăn đồ ăn

### 3. Thanh Khát (Thirst)

- **Hiển thị:** Thanh màu xanh dương ở góc dưới bên trái
- **Ý nghĩa:** Mức độ nước trong cơ thể
- **Khi thấp:** Nhân vật khô khát, giảm máu dần khi về 0
- **Phục hồi:** Uống nước

### 4. Thanh Ngủ (Sleep)

- **Hiển thị:** Thanh màu tím ở góc dưới bên trái
- **Ý nghĩa:** Mức độ buồn ngủ của nhân vật
- **Khi cao:** Nhân vật mệt mỏi, trạng thái xấu khi về 0
- **Phục hồi:** Ngủ bằng chiếu ngủ mua tại tạp hoá hoặc các chỗ ngủ khác

### 5. Thanh Stress (Stress)

- **Hiển thị:** Thanh màu hồng ở góc dưới bên trái
- **Ý nghĩa:** Mức độ căng thẳng của nhân vật khi bạn lái xe tốc độ cao, làm các nghề bẩn
- **Khi cao:** Nhân vật căng thẳng, trạng thái xấu khi về 0
- **Phục hồi:** Sử dụng thuốc lá, các chất làm giảm căng thẳng

## Thông Tin Nhân Vật

### Trên Màn Hình

- **Avatar:** Ảnh đại diện nhân vật
- **Server ID:** Số ID duy nhất được tạo khi bạn đăng ký
- **Nghề nghiệp:** Ban ngành hoặc tổ chức bạn đang tham gia
- **Số dư ngân hàng:** Tiền trong tài khoản
- **Tiền mặt:** Tiền mặt mang theo
- **Vũ khí:** Vũ khí đang cầm

### Thanh Trạng Thái Xe

- **Tốc độ:** Đơn vị km/h
- **Nhiên liệu:** Phần trăm xăng
- **Đèn:** Đèn xe đang bật/tắt
- **Cửa:** Mở/khóa cửa xe
- **Dây an toàn:** Đang thắt hoặc tháo ra

## Bản Đồ Nhỏ (Minimap)

### Vị Trí

- **Góc trái dưới màn hình**

### Tính Năng

- **Hiển thị vị trí:** Bạn đang ở đâu
- **Đánh dấu địa điểm:** Cửa hàng, ngân hàng, việc làm
- **Đường đi:** Khi có nhiệm vụ
- **Đồng hồ:** La bàn hướng

### Khi Đi Bộ

- **Hiển thị:** Minimap + la bàn
- **Ẩn:** Khi ngồi trong xe

## Hệ Thống Xe

### Cruise Control

- **Phím:** `Z`
- **Tính năng:** Giữ tốc độ hiện tại
- **Sử dụng:** Đi đường dài

### Bảng Điều Khiển Xe

- **Phím:** `Y`
- **Tính năng:** Điều khiển đèn, còi, cửa
- **Hiển thị:** Tất cả controls

### Xi Nhan

- **Phím:** `LEFT/RIGHT/UP`
- **Tính năng:** Bật xi nhan trái/phải, hazard
- **Lưu ý:** Phải có đèn xe

### Còi

- **Phím:** `E`
- **Tính năng:** Còi xe

### Dây An Toàn

- **Phím:** `B`
- **Tính năng:** Bật/tắt dây an toàn

## Lưu Ý Quan Trọng

- **Stress khi chạy nhanh:** Tự động tăng stress khi chạy > 160 km/h (mỗi 10 giây +2 stress)
- **Ngưỡng văng:** 32 km/h không thắt, 160 km/h có thắt
- **Ẩn/hiện:** Sử dụng `/togglehud`

## Mẹo Sử Dụng

1. **Theo dõi thường xuyên:** Luôn chú ý các thanh trạng thái
2. **Ăn uống đúng lúc:** Đừng để đói/khát quá
3. **Sử dụng cruise control:** Đi đường dài giữ tốc độ
4. **Tùy chỉnh layout:** Dùng `/hud` để chỉnh giao diện
5. **Ẩn HUD khi cần:** Dùng `/togglehud` khi chụp ảnh

---

> Quay lại: [HUD & Giao Diện](README.md) | Tiếp theo: [Menu Radial](menu-radial.md) →
