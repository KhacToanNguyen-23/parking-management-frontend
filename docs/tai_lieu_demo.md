# HƯỚNG DẪN DEMO NHANH (QUICK RUN SHEET)
*(Tối giản - Dùng để copy-paste nhanh khi báo cáo)*

---

## 📌 BẢNG DỮ LIỆU NHẬP MẪU

| Luồng Demo | Biển số xe | Mã đặt chỗ / Thẻ | Cổng vào / Zone | Phí thanh toán |
| :--- | :--- | :--- | :--- | :--- |
| **1. Khách vãng lai** | `51F-999.99` | *(Tự sinh QR)* | Gate Main-In 1 -> Zone B1-B | Tính theo giờ thực tế |
| **2. Khách đặt trước**| `59X-777.77` | `RES-2026-001` | Gate Main-In 1 -> Zone B1-A | Tính theo giờ thực tế |
| **3. Vé tháng/quý/năm**| `51A-123.45` | Gói tháng ACTIVE | Gate Main-In 1 -> Zone B1-B | **0 VNĐ** |
| **4. Admin cấu hình**| *(Tạo mới)* | N/A | Tòa nhà: `Grand Center` | Đơn giá: `10.000đ/h` (Free 15m) |
| **5. Security sự cố**| `51F-999.99` | Ghi log `LOST_CARD` | Đen: `30A-111.11` (Báo động) | Nút SOS (Nhấn giữ 3s) |

---

## 🔄 BƯỚC THỰC HIỆN CHI TIẾT TỪNG LUỒNG

### 1. Khách vãng lai (Walk-in)
1. **Vào cổng:** Check-In Cổng Chính -> Nhập biển `51F-999.99` -> Chọn `CAR` -> Bấm **Tạo phiên**.
   * *Ảnh xe vào:* `[ ... ]`
2. **Vào Zone:** Check-In Cổng Zone -> Nhập mã phiên / quét QR vừa tạo -> Chọn `Gate Zone-B1-B-In` -> Bấm **Xác nhận**.
   * *Ảnh QR Code:* `[ ... ]`
3. **Ra cổng:** Check-Out Cổng Ra -> Nhập biển `51F-999.99` -> Chọn `MOMO`/`CASH` -> Xem phí -> Bấm **Xác nhận**.

### 2. Khách đặt chỗ trước (Pre-booked)
1. **Vào cổng:** Check-In Cổng Chính -> Nhập mã đặt chỗ `RES-2026-001` + biển `59X-777.77` -> Bấm **Tạo phiên** (Hệ thống tự nhận diện đúng `Zone B1-A`).
   * *Ảnh xe đặt trước:* `[ ... ]`
2. **Vào Zone:** Check-In Cổng Zone -> Nhập mã phiên -> Chọn `Gate Zone-B1-A-In` -> Bấm **Xác nhận**.
3. **Ra cổng:** Check-Out Cổng Ra -> Nhập biển `59X-777.77` -> Tính phí theo giờ -> Bấm **Xác nhận**.

### 3. Xe đăng ký theo gói (Subscriber)
1. **Vào cổng:** Check-In Cổng Chính -> Nhập biển `51A-123.45` -> Bấm **Tạo phiên** (Hệ thống tự động hiển thị loại `SUBSCRIBER`).
   * *Ảnh xe đăng ký:* `[ ... ]`
2. **Vào Zone:** Check-In Cổng Zone -> Chọn `Gate Zone-B1-B-In` -> Bấm **Xác nhận**.
3. **Ra cổng:** Check-Out Cổng Ra -> Nhập biển `51A-123.45` -> Hệ thống báo phí **0 VNĐ** -> Bấm **Xác nhận**.

### 4. Admin cấu hình tòa nhà & biểu phí
1. **Hạ tầng:** Vào **Infrastructure** -> Thêm Building `Grand Center` -> Thêm Floor `Tầng Hầm G1` -> Thêm Zone `ZONE-G1` -> Thêm Cổng `Gate GC-In`.
2. **Biểu phí:** Vào **Pricing Rules** -> Tạo biểu phí cho `Grand Center` (Xe `CAR`, Phí `10.000đ/giờ`, Miễn phí `15` phút đầu).

### 5. Security & Sự cố an ninh
1. **Tra cứu:** Vào **Search** -> Nhập biển `51F-999.99` -> Xem trạng thái xe đang đỗ & lịch sử.
2. **Báo sự cố:** Vào **Exception Logs** -> Chọn loại `LOST_CARD` -> Nhập biển `51F-999.99` -> Bấm **Lưu**.
   * *Ảnh biên bản sự cố:* `[ ... ]`
3. **Danh sách đen:** Vào **Blacklist** -> Thêm biển `30A-111.11` -> Khi xe này qua cổng chính, màn hình báo động đỏ nháy liên tục -> Bấm **Đã tiếp nhận**.
4. **Báo động khẩn cấp:** Vào **Emergency** -> Nhấn giữ nút **SOS đỏ** trong **3 giây** (Barrier toàn bộ cổng sẽ tự động mở).
