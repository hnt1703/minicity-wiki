# HUD Chính

HUD chính hiển thị tất cả thông tin quan trọng về nhân vật và môi trường. Hệ thống được thiết kế直观, dễ theo dõi.

## Các Thanh Trạng Thái

### 1. Thanh Máu (Health)
- **Hiển thị:** Màu đỏ trên màn hình
- **Ý nghĩa:** Sức khỏe hiện tại
- **Khi thấp:** Nhân vật sẽ yếu đi, có thể chết
- **Phục hồi:** Sử dụng bông băng, thuốc men

### 2. Thanh Đói (Hunger)
- **Hiển thị:** Màu cam trên màn hình
- **Ý nghĩa:** Mức độ no của nhân vật
- **Khi thấp:** Nhân vật mệt mỏi, giảm hiệu suất
- **Phục hồi:** Ăn đồ ăn

### 3. Thanh Khát (Thirst)
- **Hiển thị:** Màu xanh dương trên màn hình
- **Ý nghĩa:** Mức độ nước trong cơ thể
- **Khi thấp:** Nhân vật khô khát, giảm hiệu suất
- **Phục hồi:** Uống nước

### 4. Thanh Stress
- **Hiển thị:** Màu tím trên màn hình
- **Ý nghĩa:** Mức độ căng thẳng
- **Khi cao:** Ảnh hưởng đến gameplay
- **Giảm stress:** Sử dụng thuốc lá, nghỉ ngơi

### 5. Thanh Nhiên Liệu (Xe)
- **Hiển thị:** Khi lái xe
- **Ý nghĩa:** Mức xăng còn lại
- **Khi thấp:** Xe có thể dừng hoạt động
- **Phục hồi:** Đổ xăng tại trạm

## Thông Tin Nhân Vật

### Trên Màn Hình
- **Avatar:** Ảnh đại diện nhân vật
- **Server ID:** Số ID trên server
- **Nghề nghiệp:** Nghề hiện tại
- **Số dư ngân hàng:** Tiền trong tài khoản
- **Tiền mặt:** Tiền mặt mang theo
- **Vũ khí:** Vũ khí đang cầm

### Thanh Trạng Thái Xe
- **Tốc độ:** Đơn vị km/h
- **Nhiên liệu:** Phần trăm xăng
- **Đèn:** Đèn xe đang bật/tắt
- **Cửa:** Mở/khóa cửa xe

## Bản Đồ Nhỏ (Minimap)

### Vị Trí
- **Góc trái dưới màn hình**

### Tính Năng
- **Hiển thị vị trí:** Bạn đang ở đâu
- **Đánh dấu địa điểm:** Cửa hàng, ngân hàng, việc làm
- **Đường đi:** Khi có nhiệm vụ
- **Đồng hồ:** La bàn方向

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

## Lưu Ý Quan Trọng

- **Stress khi chạy nhanh:** Tự động tăng stress khi chạy > 160 km/h (mỗi 10 giây +2 stress)
- **Dây an toàn:** Tắt (đã xử lý sẵn)
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
