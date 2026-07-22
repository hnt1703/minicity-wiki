# MINICITY SS2 — Wiki & Hướng Dẫn Toàn Tập

> Server FiveM dựa trên nền tảng **Qbox Framework** — Phiên bản SS2
> Đường dẫn resource: `resources/`

---

## Mục Lục

1. [Tổng Quan Server](#1-tổng-quan-server)
2. [Cấu Trúc Thư Mục](#2-cấu-trúc-thư-mục)
3. [Nghề Hợp Pháp (NGHE_SACH)](#3-nghề-hợp-pháp-nghe_sach)
4. [Nghề Bất Hợp Pháp (NGHE_BAN)](#4-nghề-bất-hợp-pháp-nghe_ban)
5. [Hệ Thống Xe Cộ & Garage](#5-hệ-thống-xe-cộ--garage)
6. [Hệ Thống Bán Hàng & Thương Mại](#6-hệ-thống-bán-hàng--thương-mại)
7. [Hệ Thống Nghề Chuyên Môn (BAN_NGANH)](#7-hệ-thống-nghề-chuyên-môn-ban_nganh)
8. [Trò Chơi & Mini Game](#8-trò-chơi--mini-game)
9. [Tính Năng Tổng Hợp](#9-tính-năng-tổng-hợp)
10. [Hệ Thống HUD & Giao Diện](#10-hệ-thống-hud--giao-diện)
11. [Framework & Core Resources](#11-framework--core-resources)
12. [Hướng Dẫn Cấu Hình & Chỉnh Sửa](#12-hướng-dẫn-cấu-hình--chỉnh-sửa)
13. [Các Resource ox (Ox Library)](#13-các-resource-ox-ox-library)
14. [Xe & Đồ Họa (CAR / CLOTHING / MLO)](#14-xe--đồ-họa-car--clothing--mlo)
15. [Bảo Mật & Quản Trị](#15-bảo-mật--quản-trị)
16. [Bản Đồ & Vị Trí Quan Trọng](#16-bản-đồ--vị-trí-quan-trọng)

---

## 1. Tổng Quan Server

**MINICITY SS2** là server roleplay Việt Nam xây dựng trên nền tảng **Qbox Framework** (phiên bản nâng cấp từ QBCore), sử dụng hệ sinh thái **ox_lib / ox_inventory / ox_target / ox_doorlock** cho quản lý items, UI, và tương tác.

### Các tính năng chính:
- **15+ nghề nghiệp** hợp pháp và bất hợp pháp
- **Hệ thống garage nâng cao** (Advanced Garages) với job garage, impound, dashboard
- **Hệ thống bang hội** với cơ chế chiếm giữ
- **Mini game đa dạng**: loto, poker, tài xỉu, vòng quay may mắn
- **Cửa hàng, quán ăn, workshop** bán hàng hóa
- **Hệ thống trang phục** với hàng nghìn mẫu quần áo
- **Điện thoại LBPhone** đầy đủ tính năng
- **HUD tùy chỉnh** (JG Scripts)
- **Hệ thống voice chat** (PMA-Voice)
- **Hệ thống-properties** (QShousingE) với nhà ở

---

## 2. Cấu Trúc Thư Mục

```
resources/
├── [JOB]/              ← Tài nguyên nghề nghiệp
│   ├── [NGHE_BAN]/     ← Nghề bất hợp pháp
│   └── [NGHE_SACH]/    ← Nghề hợp pháp
├── [TINH_NANG]/        ← Tính năng tổng hợp
├── [BAN_NGANH]/        ← Nghề chuyên môn (Cảnh sát, Y tế, v.v.)
├── [MINI_GAME]/        ← Mini game
├── [GAME]/             ← Trò chơi giải trí
├── [ox]/               ← Hệ sinh thái Ox (lib, inventory, target, doorlock)
├── [qbx]/              ← Qbox Framework Core + Plugins
├── [CAR]/              ← Xeehicles (Job, Police, Medical, Sell)
├── [CLOTHING]/         ← Đồ họa quần áo
├── [MLO]/              ← Map Interior / MLO
├── [standalone]/       ← Resource độc lập
├── [STREAM]/           ← Streaming assets
└── [voice]/            ← Voice Chat (PMA-Voice)
```

---

## 3. Nghề Hợp Pháp (NGHE_SACH)

Đường dẫn: `[JOB]/[NGHE_SACH]/`

### 3.1 🌾 Nông Trại — mini-farming
- **Mô tả:** Chăn bò, trồng bắp cải, bí ngô, nuôi gà, thỏ, thu muối biển
- **Cấu hình:** `config.lua` trong resource
- **Hệ thống:** ox_target để tương tác cây trồng/động vật, progressbar khi thu hoạch

### 3.2 🚛 Lái Xe Tải — mini_laixetai
- **Mô tả:** Nghề Trucker — vận chuyển hàng hóa từ kho đến các địa điểm
- **Cơ chế:** Lấy hàng tại điểm bắt đầu, lái xe đến điểm giao, nhận tiền

### 3.3 🚌 Lái Xe Buýt — mini_busjob
- **Mô tả:** Nghề lái xe buýt — chở hành khách theo tuyến đường cố định
- **Cấu hình:** 17 file lua, 1 file JSON

### 3.4 🪨 Khai Thác Đá — stone-mining
- **Mô tả:** Đào đá, thu thập khoáng sản, chế biến thành vật liệu
- **Đặc điểm:** 15 file lua, có progressbar, ox_target

### 3.5 🌿 Thu Hoạch Cao Su — rubber-farming
- **Mô tả:** Thu hoạch mủ cao su từ cây cao su và chế biến
- **Đặc điểm:** Đơn giản, chỉ có lua

### 3.6 🏊 Lặn Biển — minicity_diving
- **Mô tả:** Lặn xuống biển tìm kiếm vật phẩm quý hiếm
- **Đặc điểm:** HTML UI + Lua, có thể tìm thấy đồ vật đặc biệt dưới nước

### 3.7 🎣 Câu Cá — i_fishing (bộ [cauca])
- **Mô tả:** Hệ thống câu cá đầy đủ với_props (bệ câu, cần câu, mồi)
- **Components:**
  - `i_fishing` — Script chính
  - `i_fishingProps` — Props đồ vật câu cá (stream)
  - `Propscauca` — Props bệ câu cá (stream)
  - `object_gizmo` — Công cụ Gizmo cho đối tượng

### 3.8 🌳 Nghề Gỗ — don_go
- **Mô tả:** Khai thác và chế biến gỗ
- **Đặc điểm:** 5 lua, 3 ydr (model 3D), 3 ytyp, 2 ycd (animation)

### 3.9 🗑️ Lục Rác — luc_rac
- **Mô tả:** Tìm kiếm trong thùng rác để nhặt vật phẩm
- **Cơ chế:** Tương tác thùng rác, có xác suất nhận item

### 3.10 💧 Nhà Máy Nước — water-plant
- **Mô tả:** Nhà máy xử lý nước sạch
- **Đặc điểm:** Đơn giản, chỉ có lua

---

## 4. Nghề Bất Hợp Pháp (NGHE_BAN)

Đường dẫn: `[JOB]/[NGHE_BAN]/`

> ⚠️ **Lưu ý:** Tất cả các nghề bất hợp pháp đều yêu cầu có **event_guard** để bảo vệ chống lạm dụng.

### 4.1 ⏰ Cậy Đồng Hồ — CayDongHo
- **Mô tả:** Cậy máy đỗ xe (parking meter) để lấy tiền và đồng hồ
- **Config:** `[JOB]/[NGHE_BAN]/CayDongHo/config.lua`
- **Cấu hình quan trọng:**
  ```lua
  Config.ThoiGianThanh = 9000      -- Thời gian thanh chạy (9s)
  Config.Cops = 0                   -- Số cảnh sát yêu cầu (0 = không cần)
  Config.CooldownSuccess = 120      -- Cooldown khi thành công (2 phút)
  Config.CooldownFailed = 10        -- Cooldown khi thất bại (10 giây)
  Config.Lockpick = { item = 'lockpick', amount = 1, breakChance = 100 }
  Config.Rewards = { { chance = 100, items = {{name = 'dongho', amount = 1}} } }
  Config.RareItems = { { item = 'bangkeo', chance = 10, amount = 1 } }
  ```
- **Khu vực:** `vec3(196.5, -933.25, 30.0)` — Bán kính `112.5 x 171.5`
- **Model xe đỗ:** `prop_parknmeter_02`, `prop_parknmeter_01`
- **Hệ thống cooldown:** Server-side_GlobalState + Config-driven

### 4.2 🪧 Trộm Biển Báo — trombienbao
- **Mô tả:** Ăn cắp các biển hiệu/bảng quảng cáo đường phố
- **Config:** `[JOB]/[NGHE_BAN]/trombienbao/config.lua`
- **Cấu hình quan trọng:**
  ```lua
  Config.ProgressbarTime = 120000    -- 2 phút thanh tiến trình
  Config.Lockpick = { item = 'xa_beng', amount = 1, consume = true, breakChance = 50 }
  Config.CopsRequired = 3            -- Cần 3 cảnh sát onduty
  Config.ServerCooldown = 300        -- Cooldown server 5 phút
  Config.PlayerCooldown = 0          -- Cooldown cá nhân (tắt)
  Config.CooldownFailed = 10         -- Cooldown khi minigame thất bại (10 giây)
  Config.StealMaxDistance = 15.0     -- Khoảng cách tối đa player ↔ biển
  ```
- **Loại biển báo có thể trộm:**
  | Prop | Item | Mô tả |
  |------|------|-------|
  | prop_sign_road_01a | stopsign | Biển STOP |
  | prop_sign_road_05a | walkingmansign | Biển người đi bộ |
  | prop_sign_road_03e | dontblockintersectionsign | Biển giao lộ |
  | prop_sign_road_03m | uturnsign | Biển quay đầu |
  | prop_sign_road_04a | noparkingsign | Biển cấm đỗ xe |
  | prop_sign_road_05e | leftturnsign | Biển rẽ trái |
  | prop_sign_road_05f | rightturnsign | Biển rẽ phải |
  | prop_sign_road_restriction_10 | notrespassingsign | Biển cấm vào |
  | prop_sign_road_02a | yieldsign | Biển nhường đường |
- **Khu vực:** Sa mạc (`2088.06, 3027.11, 45.42`) và Thành phố (`-198.6, -518.38, 34.77`), bán kính 1000m
- **Item hiếm:** `bulong` (10% xác suất)

### 4.3 🌱 Trồng Cần Sa — growing-weed
- **Mô tả:** Trồng và thu hoạch cần sa
- **Đặc điểm:** HTML UI + Lua, 6 lua, 6 png (hình ảnh)

### 4.4 🕳️ Trộm Nắp Cống — TromNapCong
- **Mô tả:** Ăn cắp nắp cống trên đường phố
- **Đặc điểm:** Stream props nắp cống

### 4.5 🐟 Câu Cá Bất Hợp Pháp
- **Lưu ý:** Bộ câu cá [cauca] nằm trong [NGHE_BAN] — có thể câu bất hợp pháp

---

## 5. Hệ Thống Xe Cộ & Garage

### 5.1 🏢 Advanced Garages — advancedgarages
- **Đường dẫn:** `[TINH_NANG]/advancedgarages/`
- **Mô tả:** Hệ thống garage nâng cao — bãi đỗ xe, impound, dashboard, private garage
- **Các loại garage:**
  - **Public Garage:** Bãi đỗ xe công cộng
  - **Job Garage:** Bãi đỗ xe cho nhân viên (theo nghề)
  - **Private Garage:** Bãi đỗ xe riêng (cá nhân)
  - **Impound:** Bãi giữ xe tạm
- **Config jobs:** `[TINH_NANG]/advancedgarages/config/config-jobs.lua`
- **Framework:** `[TINH_NANG]/advancedgarages/framework/cl-functions.lua`
  - Hỗ trợ: `cdn-fuel`, `ox_fuel`, vanilla fuel
- **Client spawn:** `[TINH_NANG]/advancedgarages/client/cl-spawn.lua`
  - Hỗ trợ livery: `SetVehicleMod(vehicle, 48, livery, false)` + `SetVehicleLivery(vehicle, livery)`
- **Cấu hình fuel system:**
  ```lua
  Config.FuelSystem = "cdn-fuel"  -- hoặc "ox_fuel" hoặc "vanilla"
  ```

### 5.2 🔧 Độ Xe — do_xe
- **Đường dẫn:** `[TINH_NANG]/do_xe/`
- **Mô tả:** Hệ thống độ xe tùy chỉnh
- **Đặc điểm:** 7 lua, 100 png (hình ảnh mod), 4 ttf (font), 3 svg

### 5.3 🛠️ Công Cụ Sửa Xe — mechanic_tools
- **Đường dẫn:** `[TINH_NANG]/mechanic_tools/`
- **Mô tả:** Bộ công cụ sửa chữa xe cho thợ sửa xe

### 5.4 🎮 Trình Chỉnh Sửa Handling — mini-handling
- **Đường dẫn:** `[TINH_NANG]/mini-handling/`
- **Mô tả:** Công cụ chỉnh sửa handling xe real-time

### 5.5 🛞 Bánh Xe Hư Hỏng — kq-wheeldamage
- **Đường dẫn:** `[TINH_NANG]/kq-wheeldamage/`
- **Mô tả:** Hệ thống bánh xe hư hỏng thực tế

### 5.6 🚗 Bán Xe Cũ — ban_xe_cu
- **Đường dẫn:** `[TINH_NANG]/ban_xe_cu/`
- **Mô tả:** Ký gửi bán xe cũ tại garage

### 5.7 🚘 Bán Xe — Cardealer
- **Đường dẫn:** `[BAN_NGANH]/Cardealer/`
- **Mô tả:** Showroom bán xe mới
- **Database:** Có SQL để tạo bảng

### 5.8 🚕 Mua Bán Xe
- **Resource:** Qbox vehicles (`[qbx]/qbx_vehicles`)
- **Framework:** Qbox vehicle system

---

## 6. Hệ Thống Bán Hàng & Thương Mại

### 6.1 🏪 Mini Shop — mini-shop
- **Đường dẫn:** `[TINH_NANG]/mini-shop/`
- **Mô tả:** Cửa hàng mini với catalog, tồn kho, checkout
- **Đặc điểm:** 15 lua (rất nhiều config), có font tùy chỉnh

### 6.2 🏷️ Bán Vật Phẩm — ban_item
- **Đường dẫn:** `[TINH_NANG]/ban_item/`
- **Mô tả:** Script bán hàng (chỉnh sửa bởi D-TEAM)
- **Có thể:** Bán items lấy tiền

### 6.3 📦 Bưu Cục — buu-cuc
- **Đường dẫn:** `[TINH_NANG]/buu-cuc/`
- **Mô tả:** Bưu cục cá nhân — kho chứa đồ (P2P tùy chọn)
- **Đặc điểm:** 8 lua, 1 SQL, 1 JSON

### 6.4 🎁 Mini Case — mini-case
- **Đường dẫn:** `[TINH_NANG]/mini-case/`
- **Mô tả:** Hệ thống mở Case (Case Opening) — gacha, thẻ bài, crayon, shop
- **Đặc điểm:** Rất lớn — 3511 JS, 2438 TS

### 6.5 👜 Đồ Phụ Kiện — mini_dapphukien
- **Đường dẫn:** `[TINH_NANG]/mini_dapphukien/`
- **Mô tả:** Hệ thống stash đồ vật Generic

### 6.6 🍳 Nấu Ăn — cooking
- **Đường dẫn:** `[TINH_NANG]/cooking/`
- **Mô tả:** Hệ thống nấu ăn
- **Đặc điểm:** 4 lua, 18 png (hình ảnh nguyên liệu)

### 6.7 ⚒️ Chế Tạo — che_tao
- **Đường dẫn:** `[TINH_NANG]/che_tao/`
- **Mô tả:** Hệ thống chế tạo (Crafting) — Qbox + ox_inventory + ox_target
- **Đặc điểm:** 228 TS, rất nhiều thành phần

### 6.8 💰 Hệ Thống Ngân Hàng — Renewed-Banking
- **Đường dẫn:** `[standalone]/Renewed-Banking/`
- **Mô tả:** Ngân hàng cá nhân, chuyển tiền, tài khoản chung

---

## 7. Hệ Thống Nghề Chuyên Môn (BAN_NGANH)

Đường dẫn: `[BAN_NGANH]/`

### 7.1 👮 Cảnh Sát — qbx_police
- **Đường dẫn:** `[BAN_NGANH]/qbx_police/`
- **Mô tả:** Hệ thống cảnh sát — cuff, drag, search, seize, ticket, warrant
- **Đặc điểm:** 18 lua, 15 JSON (items/locales)

### 7.2 🚑 Y Tế — qbx_ambulancejob
- **Đường dẫn:** `[BAN_NGANH]/qbx_ambulancejob/`
- **Mô tả:** Nghề bác sĩ — hồi sinh, chữa lành, chở bệnh nhân
- **Đặc điểm:** 17 JSON, 14 lua

### 7.3 🏥 Hệ Thống Y Tế — qbx_medical
- **Đường dẫn:** `[BAN_NGANH]/qbx_medical/`
- **Mô tả:** Hệ thống y tế nâng cao — chấn thương, thuốc men, phẫu thuật
- **Đặc điểm:** 17 JSON, 16 lua, 3 MD

### 7.4 📋 MDT — MDT (Mobile Data Terminal)
- **Đường dẫn:** `[BAN_NGANH]/MDT/`
- **Mô tả:** Terminal dữ liệu di động cho cảnh sát — tra cứu người, xe, tội phạm
- **Đặc điểm:** Rất lớn — 1400 JS

### 7.5 🚔 Dispatch — ping_dispatch
- **Đường dẫn:** `[BAN_NGANH]/ping_dispatch/`
- **Mô tả:** Hệ thống dispatch — nhận thông báo sự cố, gửi cảnh sát/y tế

### 7.6 🔫 Công Cụ Cảnh Sát — pdtools
- **Đường dẫn:** `[BAN_NGANH]/pdtools/`
- **Mô tả:** Công cụ cảnh sát — radar, speed gun, breathalyzer
- **Đặc điểm:** 19 lua (rất nhiều tool)

### 7.7 📋 Quản Lý Kho — quanlykho
- **Đường dẫn:** `[BAN_NGANH]/quanlykho/`
- **Mô tả:** Quản lý kho hàng cho các nghề

### 7.8 🏥 Nạng — crutches-main
- **Đường dẫn:** `[BAN_NGANH]/crutches-main/`
- **Mô tả:** Hệ thống nạng khi bị thương

### 7.9 📸 Chụp Ảnh Tội Phạm — kael-mugshot-main
- **Đường dẫn:** `[BAN_NGANH]/kael-mugshot-main/`
- **Mô tả:** Chụp ảnh mugshot khi bắt giữ

### 7.10 🪪 Thẻ Cảnh Sát — stevo_policebadge
- **Đường dẫn:** `[BAN_NGANH]/stevo_policebadge/`
- **Mô tả:** Thẻ cảnh sát để xác nhận danh tính

### 7.11 💇 Cắt Tóc — nl_hotcut
- **Đường dẫn:** `[BAN_NGANH]/nl_hotcut/`
- **Mô tả:** Tiệm cắt tóc
- **Đặc điểm:** 7 lua, SQL, HTML

### 7.12 🎙️ Radio — 0r-radio
- **Đường dẫn:** `[BAN_NGANH]/0r-radio/`
- **Mô tả:** Hệ thống radio cho các nghề
- **Đặc điểm:** 47 lua, 9 ogg (âm thanh), 4 ycd (animation)

### 7.13 🪪 CMND — bl_idcard-main
- **Đường dẫn:** `[BAN_NGANH]/bl_idcard-main/`
- **Mô tả:** Hệ thống chứng minh nhân dân / giấy tờ tùy thân

### 7.14 📝 Hóa Đơn — HOA_DON
- **Đường dẫn:** `[BAN_NGANH]/HOA_DON/`
- **Mô tả:** Hệ thống hóa đơn cho giao dịch

### 7.15 🚨 CRM — Phạt Đâm Xe
- **Đường dẫn:** `[TINH_NANG]/CRM/`
- **Mô tả:** Collision Response Management — phạt khi đâm xe
- **Đặc điểm:** 5 lua, SQL, HTML

### 7.16 🚨 Sirens — Renewed-Sirensync
- **Đường dẫn:** `[BAN_NGANH]/Renewed-Sirensync/`
- **Mô tả:** Đồng bộ sirens cho xe cảnh sát

---

## 8. Trò Chơi & Mini Game

### 8.1 Mini Game — [MINI_GAME]
Đường dẫn: `[MINI_GAME]/`

| Resource | Mô tả |
|----------|-------|
| **minigameui** | Hệ thống UI cho mini game (rất lớn: 7866 JS) |
| **1307_NhayAu** | Trò nhảy au (dance game) |
| **safecracker-main** | Trò crack két sắt |
| **skillchecks** | Kiểm tra kỹ năng (throttle, hack, v.v.) |

### 8.2 Trò Chơi Giải Trí — [GAME]
Đường dẫn: `[GAME]/`

| Resource | Mô tả |
|----------|-------|
| **loto** | Trò chơi loto / xổ số (11 lua, 91 âm thanh) |
| **tienlen** | Trò chơi tiến lên (card game) |
| **veso** | Trò chơi tài xỉu / xí ngầu |
| **vongquay** | Vòng quay may mắn |
| **jh / jh_gfx** | Trò chơi khác (graphic effects) |
| **tivi_loto_gfx** | TV hiển thị kết quả loto |

---

## 9. Tính Năng Tổng Hợp

Đường dẫn: `[TINH_NANG]/`

### 9.1 🏠 Nhà Ở — QShousingE
- **Đường dẫn:** `[TINH_NANG]/[QShousingE]/`
- **Mô tả:** Hệ thống nhà ở — mua bán, trang trí, storage
- **Đặc điểm:** Rất lớn — 893 webp, 408 png, 178 lua

### 9.2 📱 Điện Thoại — LBPHONE
- **Đường dẫn:** `[TINH_NANG]/[LBPHONE]/`
- **Mô tả:** Hệ thống điện thoại thông minh — gọi, tin nhắn, camera, apps
- **Đặc điểm:** 165 lua, 230 jpg

### 9.3 💬 Chat — [chat]
- **Đường dẫn:** `[TINH_NANG]/[chat]/`
- **Mô tả:** Hệ thống chat tùy chỉnh
- **Đặc điểm:** 14 lua, 6 JS

### 9.4 👔 Quần Áo — Clothes
- **Đường dẫn:** `[TINH_NANG]/Clothes/`
- **Mô tả:** Cửa hàng quần áo (Clothesshop) — quản lý trang phục, balo
- **Đặc điểm:** Rất lớn — 1436 JS, 260 TS

### 9.5 🎒 Đập Balo — dapbalo
- **Đường dẫn:** `[TINH_NANG]/dapbalo/`
- **Mô tả:** Hệ thống đập balo (loot box)
- **Đặc điểm:** 74 mp3 (âm thanh), 42 png, 7 lua

### 9.6 🎁 Gift Code — giftcode
- **Đường dẫn:** `[TINH_NANG]/giftcode/`
- **Mô tả:** Hệ thống gift code — nhập code nhận quà
- **Đặc điểm:** 6 lua, 2 MD, 1 SQL

### 9.7 📊 Điểm Danh & Referral — diemdanh_newbie
- **Đường dẫn:** `[TINH_NANG]/diemdanh_newbie/`
- **Mô tả:** Điểm danh hàng ngày + hệ thống referral (tuyển người chơi mới)
- **Đặc điểm:** 13 lua, SQL, CSS

### 9.8 🏍️ Vật Mang Vũ Khí — CarryWeapons
- **Đường dẫn:** `[TINH_NANG]/CarryWeapons/`
- **Mô tả:** Vật mang vũ khí (client-side)

### 9.9 🪑 Ngồi — dc-sit
- **Đường dẫn:** `[TINH_NANG]/dc-sit/`
- **Mô tả:** Cho phép người chơi ngồi ở nhiều vị trí

### 9.10 🌙 Hệ Thống Ngủ — sleep_system
- **Đường dẫn:** `[TINH_NANG]/sleep_system/`
- **Mô tả:** Hệ thống ngủ — cần ngủ để phục hồi energy
- **Đặc điểm:** 10 lua, video MP4 hướng dẫn

### 9.11 🗺️ Sat Map — oulsen_satmap_mini
- **Đường dẫn:** `[TINH_NANG]/oulsen_satmap_mini/`
- **Mô tả:** Bản đồ vệ tinh (satellite map)

### 9.12 📖 Guidebook — rcore_guidebook
- **Đường dẫn:** `[TINH_NANG]/rcore_guidebook/`
- **Mô tả:** Sách hướng dẫn trong game

### 9.13 🔧 Prop Tool — prop_tool
- **Đường dẫn:** `[TINH_NANG]/prop_tool/`
- **Mô tả:** Công cụ đặt prop

### 9.14 📊 XP UI — xp_ui
- **Đường dẫn:** `[TINH_NANG]/xp_ui/`
- **Mô tả:** Hiển thị cấp độ kinh nghiệm nghề nghiệp + bảng xếp hạng giàu có

### 9.15 🏢 Bang Hội — bang_dang
- **Đường dẫn:** `[TINH_NANG]/bang_dang/`
- **Mô tả:** Hệ thống bang hội — lập bang, chiếm nhà, quản lý thành viên, sự kiện
- **Đặc điểm:** 14 lua, SQL

### 9.16 🪣 Bucket Manager — bucket_manager
- **Đường dẫn:** `[TINH_NANG]/bucket_manager/`
- **Mô tả:** Kiểm tra và reset bucket cho QBCore

### 9.17 🔒 Client Detect — client_detect
- **Đường dẫn:** `[TINH_NANG]/client_detect/`
- **Mô tả:** Phát hiện client — anti-cheat cơ bản
- **Đặc điểm:** 15 lua

### 9.18 📋 Log — log
- **Đường dẫn:** `[TINH_NANG]/log/`
- **Mô tả:** Hệ thống log quản trị items

### 9.19 📡 Event — Event
- **Đường dẫn:** `[TINH_NANG]/Event/`
- **Mô tả:** Quản lý sự kiện (event handler)

---

## 10. Hệ Thống HUD & Giao Diện

### 10.1 📊 HUD Chính — jg-hud
- **Đường dẫn:** `[TINH_NANG]/jg-hud/`
- **Mô tả:** HUD chính của server — bản đồ, speedometer, trạng thái
- **Đặc điểm:** 111 webp, 31 py, 22 lua

### 10.2 📊 Progress Bar — progressbar
- **Đường dẫn:** `[TINH_NANG]/progressbar/`
- **Mô tả:** Thanh tiến trình cho các hoạt động

### 10.3 🔔 Thông Báo — thongbaosv
- **Đường dẫn:** `[TINH_NANG]/thongbaosv/`
- **Mô tả:** Hệ thống thông báo server

### 10.4 🎮 Menu Tùy Chỉnh — pausemenu
- **Đường dẫn:** `[TINH_NANG]/pausemenu/`
- **Mô tả:** Pause menu tùy chỉnh (NC Menu)
- **Đặc điểm:** 1552 JS

### 10.5 ☸️ Menu Radial — qb-radialmenu
- **Đường dẫn:** `[TINH_NANG]/qb-radialmenu/`
- **Mô tả:** Menu radial (bánh xe) cho thao tác nhanh

### 10.6 🖥️ Loading Screen — loadingscreen
- **Đường dẫn:** `[TINH_NANG]/loadingscreen/`
- **Mô tả:** Màn hình loading khi vào server

### 10.7 🎭 Rich Presence — dt-richpresence
- **Đường dẫn:** `[TINH_NANG]/dt-richpresence/`
- **Mô tả:** Discord Rich Presence — hiển thị thông tin server trên Discord

### 10.8 💊 Thuốc Dapbalo
- **Lưu ý:** `dapbalo` cũng là một hệ thống loot box với hiệu ứng âm thanh

---

## 11. Framework & Core Resources

### 11.1 Qbox Core — qbx_core
- **Đường dẫn:** `[qbx]/qbx_core/`
- **Mô tả:** Nền tảng chính của server
- **Đặc điểm:** 55 lua, 37 JSON

### 11.2 Qbox Management — qbx_management
- **Đường dẫn:** `[qbx]/qbx_management/`
- **Mô tả:** Quản lý boss, society, gang

### 11.3 Qbox City Hall — qbx_cityhall
- **Đường dẫn:** `[qbx]/qbx_cityhall/`
- **Mô tả:** Tòa thị chính — nhận việc, nộp hồ sơ

### 11.4 Qbox Properties — qbx_properties
- **Đường dẫn:** `[qbx]/qbx_properties/`
- **Mô tả:** Hệ thống bất động sản

### 11.5 Qbox Admin Menu — qbx_adminmenu
- **Đường dẫn:** `[qbx]/qbx_adminmenu/`
- **Mô tả:** Menu quản trị viên

### 11.6 Qbox Multi Character — qb-multicharacter-main
- **Đường dẫn:** `[qbx]/qb-multicharacter-main/`
- **Mô tả:** Hệ thống multi character

### 11.7 Animations — bablo-animations
- **Đường dẫn:** `[qbx]/bablo-animations/`
- **Mô tả:** Library animations
- **Đặc điểm:** 313 ycd, 92 lua

### 11.8 Seatbelt — qbx_seatbelt
- **Đường dẫn:** `[qbx]/qbx_seatbelt/`
- **Mô tả:** Hệ thống thắt dây an toàn

### 11.9 Density — qbx_density
- **Đường dẫn:** `[qbx]/qbx_density/`
- **Mô tả:** Quản lý density NPC/xe trên đường
- **Đặc điểm:** 23 ymap, 3 lua

### 11.10 Fireworks — qbx_fireworks
- **Đường dẫn:** `[qbx]/qbx_fireworks/`
- **Mô tả:** Pháo hoa

### 11.11 Interior — qbx_interior
- **Đường dẫn:** `[qbx]/qbx_interior/`
- **Mô tả:** Interior loading system

### 11.12 Binoculars — qbx_binoculars
- **Đường dẫn:** `[qbx]/qbx_binoculars/`
- **Mô tả:** Ống nhòm

### 11.13 Small Resources — qbx_smallresources
- **Đường dẫn:** `[qbx]/qbx_smallresources/`
- **Mô tả:** Các resource nhỏ (29 lua)

### 11.14 Vehicle Keys — Renewed-Vehiclekeys
- **Đường dẫn:** `[qbx]/Renewed-Vehiclekeys/`
- **Mô tả:** Hệ thống chìa khóa xe

### 11.15 Media — mini-media
- **Đường dẫn:** `[qbx]/mini-media/`
- **Mô tả:** Phát media

### 11.16 Orbit UI — orbit-ui
- **Đường dẫn:** `[qbx]/orbit-ui/`
- **Mô tả:** UI framework

### 11.17 Renewed Lib — Renewed-Lib
- **Đường dẫn:** `[qbx]/Renewed-Lib/`
- **Mô tả:** Thư viện chung (38 lua)

### 11.18 Core Guard — core_guard
- **Đường dẫn:** `[qbx]/core_guard/`
- **Mô tả:** Bảo vệ server — rate limiting, exploit detection
- **Đặc điểm:** 9 lua, 8 SQL

### 11.19 Event Guard — event_guard
- **Đường dẫn:** `[qbx]/event_guard/`
- **Mô tả:** Bảo vệ event — chống lạm dụng event

### 11.20 Backdoor Anti — backdoor_anti
- **Đường dẫn:** `[qbx]/backdoor_anti/`
- **Mô tả:** Anti-backdoor

---

## 12. Hướng Dẫn Cấu Hình & Chỉnh Sửa

### 12.1 Thêm Item Mới
**File:** `[ox]/ox_inventory/data/items.lua`

```lua
["ten_item"] = {
    label       = 'Tên hiển thị',
    weight      = 500,
    stack       = true,
    maxStack    = 5,           -- (tùy chọn) tối đa 5 cái/ô
    close       = true,
    durability  = 100,
    degrade     = 720,         -- phút để item hao mòn hết
    consume     = 1,           -- 1 = dùng hết
    description = 'Mô tả item...',
    level       = 1,           -- cấp độ hiếm (1-5)
    client = {
        export  = 'resource.exportName',
        image   = 'path/to/image.png',
    },
    server = {
        export  = 'resource.exportName',
    },
},
```

**Cấp độ hiếm (level):**
| Level | Tên | Màu |
|-------|-----|-----|
| 1 | Basic (★) | Bạc xám |
| 2 | Plus (★★) | Xanh ngọc lục |
| 3 | Pro (★★★) | Xanh coban |
| 4 | Pro Max (★★★★) | Tím hoàng gia |
| 5 | Ultra (★★★★★) | Đỏ |

### 12.2 Cấu Hình Nghề CayDongHo
**File:** `[JOB]/[NGHE_BAN]/CayDongHo/config.lua`
```lua
Config.ThoiGianThanh = 9000        -- ms
Config.Cops = 0                     -- số cảnh sát yêu cầu
Config.CooldownSuccess = 120        -- giây
Config.CooldownFailed = 10          -- giây
Config.Lockpick.item = 'lockpick'
Config.Lockpick.breakChance = 100   -- % lockpick hỏng
```

### 12.3 Cấu Hình Nghề Trombienbao
**File:** `[JOB]/[NGHE_BAN]/trombienbao/config.lua`
```lua
Config.ProgressbarTime = 120000     -- 2 phút
Config.CopsRequired = 3             -- cần 3 cảnh sát
Config.ServerCooldown = 300         -- 5 phút cooldown server
Config.CooldownFailed = 10          -- 10 giây khi thất bại
Config.Lockpick.item = 'xa_beng'
Config.Lockpick.breakChance = 50
```

### 12.4 Cấu Hình Advanced Garages
**File:** `[TINH_NANG]/advancedgarages/config/config.lua`
- `Config.FuelSystem` = `"cdn-fuel"` | `"ox_fuel"` | `"vanilla"`

**File:** `[TINH_NANG]/advancedgarages/config/config-jobs.lua`
```lua
-- Thêm xe job garage
Config.JobGarageVehicles['police'] = {
    { model = 'polvstr', nickname = 'Vapid', price = 0, minJobGrade = 0, plate = 'POLICE', maxMods = true, color1 = 0, color2 = 0 },
}
```

### 12.5 Cấu Hình Cooldown Chung
Tất cả cooldown được cấu hình trong `config.lua` của từng resource:

| Resource | Cooldown | Config Key |
|----------|----------|------------|
| CayDongHo | 120s thành công, 10s thất bại | `Config.CooldownSuccess`, `Config.CooldownFailed` |
| trombienbao | 300s server, 10s thất bại | `Config.ServerCooldown`, `Config.CooldownFailed` |

### 12.6 Cấu Hình Fuel System
**File:** `[TINH_NANG]/advancedgarages/framework/cl-functions.lua`
```lua
Config.FuelSystem = "cdn-fuel"  -- Sửa thành "ox_fuel" hoặc "vanilla" nếu cần
```

### 12.7 Cấu Hình Vehicle Livery
**File:** `[TINH_NANG]/advancedgarages/config/config-jobs.lua`
```lua
-- Để xe có livery:
{ model = 'polvstr', livery = 0, ... }  -- 0, 1, 2, ...

-- Để xe KHÔNG có livery:
{ model = 'polvstr', ... }  -- Không khai báo livery
```

---

## 13. Các Resource Ox (Ox Library)

Đường dẫn: `[ox]/`

| Resource | Mô tả | Chi tiết |
|----------|-------|----------|
| **ox_lib** | Thư viện UI & utility | 78 lua, 32 font, 31 JSON |
| **ox_inventory** | Quản lý vật phẩm | 43 lua, 21 png |
| **ox_target** | Hệ thống tương tác (nhắm) | 21 JSON, 13 lua |
| **ox_doorlock** | Khóa cửa tự động | 20 JSON, 12 lua, 4 wav/ogg |
| **oxmysql** | MySQL connector | 3 lua, 3 JS |

---

## 14. Xe & Đồ Họa (CAR / CLOTHING / MLO)

### 14.1 Xe — [CAR]

| Thư mục | Mô tả |
|---------|-------|
| `[JOB_CAR]` | Xe cho các nghề (17 meta, 8 yft, 4 lua) |
| `[MED_CAR]` | Xe cấp cứu (19 meta, 8 yft, 6 lua) |
| `[POLICE_CAR]` | Xe cảnh sát (307 yft — rất nhiều mẫu!) |
| `[SELL]` | Xe bán tại showroom |
| `[xe_cuuho]` | Xe cứu hộ |
| `policebikerb/policebvn` | Xe cảnh sát mô tô |
| `r1custom` | Xe tùy chỉnh |

### 14.2 Quần Áo — [CLOTHING]

| Resource | Mô tả |
|----------|-------|
| **1miniclothing** | Bộ quần áo chính (3748 ytd, 1353 ydd — rất lớn!) |
| **2miniclothing** | Bộ quần áo bổ sung (286 ytd, 150 ydd) |

### 14.3 MLO (Map Interior) — [MLO]
- **Đường dẫn:** `[MLO]/`
- **Mô tả:** Các bản đồ interior (879 ydr, 225 ymap, 113 ybn, 65 ytyp, 43 ytd)

### 14.4 Streaming — [STREAM]
- **Đường dẫn:** `[STREAM]/`
- **Mô tả:** Streaming assets (8 ydr, 2 lua, 2 ytyp, 2 ycd, 1 ytd)

---

## 15. Bảo Mật & Quản Trị

### 15.1 Core Guard
- **Path:** `[qbx]/core_guard/`
- **Mô tả:** Bảo vệ server cơ bản — rate limiting, exploit detection
- **Database:** 8 SQL scripts

### 15.2 Event Guard
- **Path:** `[qbx]/event_guard/`
- **Mô tả:** Bảo vệ event — tất cả các resource bất hợp pháp đều dùng `dependency 'event_guard'`

### 15.3 Client Detect
- **Path:** `[TINH_NANG]/client_detect/`
- **Mô tả:** Phát hiện client-side cheat
- **Đặc điểm:** 15 lua scripts

### 15.4 Backdoor Anti
- **Path:** `[qbx]/backdoor_anti/`
- **Mô tả:** Phát hiện và ngăn chặn backdoor

### 15.5 Admin Menu
- **Path:** `[qbx]/qbx_adminmenu/`
- **Mô tả:** Menu quản trị — teleport, spawn xe, kick, ban
- **Đặc điểm:** 12 lua, 11 JSON (permissions/configs)

### 15.6 Log System
- **Path:** `[TINH_NANG]/log/`
- **Mô tả:** Hệ thống log giao dịch items

### 15.7 Bucket Manager
- **Path:** `[TINH_NANG]/bucket_manager/`
- **Mô tả:** Quản lý routing bucket — chống trùng lặp instance

---

## 16. Bản Đồ & Vị Trí Quan Trọng

### Vị Trí Nghề Bất Hợp Pháp

| Nghề | Tọa Độ | Bán Kính |
|------|--------|----------|
| Cậy Đồng Hồ | `196.5, -933.25, 30.0` | `112.5 x 171.5` |
| Trộm Biển Báo (Sa mạc) | `2088.06, 3027.11, 45.42` | 1000m |
| Trộm Biển Báo (Thành phố) | `-198.6, -518.38, 34.77` | 1000m |

### Yêu Cầu Cảnh Sát

| Nghề | Số cảnh sát onduty |
|------|-------------------|
| Cậy Đồng Hồ | 0 (không cần) |
| Trộm Biển Báo | 3 |

---

## Bảng Từ Khóa Nhanh

| Từ Khóa | Ý Nghĩa |
|----------|---------|
| `ox_lib` | Thư viện UI & utility |
| `ox_inventory` | Quản lý vật phẩm |
| `ox_target` | Tương tác đối tượng |
| `ox_doorlock` | Khóa cửa |
| `qbx_core` | Nền tảng Qbox |
| `event_guard` | Bảo vệ event |
| `cdn-fuel` | Hệ thống nhiên liệu |
| `lbphone` | Điện thoại |
| `advancedgarages` | Garage xe |
| `jg-hud` | HUD chính |

---

> **Phiên bản:** SS2
> **Framework:** Qbox (QBCore fork)
> **Lua Version:** 5.4
> **Last Updated:** 2026-07-22