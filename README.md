# VOTA Media Tool Live

VOTA Media Tool Live là ứng dụng desktop dành cho việc thiết lập và vận hành livestream video từ máy tính Windows. Ứng dụng kết hợp giao diện quản lý luồng với worker chạy cục bộ, giúp người vận hành cấu hình nguồn video và điểm phát, khởi chạy livestream, theo dõi trạng thái và xử lý sự cố tại một nơi.

## Tính năng chính

- Tạo, chỉnh sửa, lên lịch, bắt đầu, dừng và quản lý nhiều luồng livestream.
- Phát tới YouTube hoặc các đích RTMP/RTMPS/HLS tùy chỉnh.
- Dùng video từ máy tính, liên kết Google Drive hoặc Transfer.it, URL video trực tiếp và playlist; có thể tải trước nguồn từ xa để chuẩn bị trước giờ phát.
- Thay video trong lúc livestream mà không phải kết nối lại đầu ra.
- Theo dõi trạng thái worker, tiến trình FFmpeg và thông tin chẩn đoán.
- Lưu cấu hình luồng và lịch phát theo người dùng; khi mở ứng dụng lại, các luồng ở trạng thái dừng để người dùng chủ động khởi chạy.

Ứng dụng ưu tiên vận hành cục bộ. Worker cung cấp API HTTP và cập nhật trạng thái qua WebSocket; giao diện desktop và API cùng quản lý các luồng trên một worker.

## Tải xuống

Tải installer Windows x64 từ [bản phát hành mới nhất](https://github.com/vat2003/vati-media-tool-live-releases/releases/latest). Mở trang phát hành để xem ghi chú và các tệp đi kèm.

### Bản mới nhất: v5.22.60.33

Bản này cải thiện hiển thị các Worker độc lập đã kết nối khi yêu cầu đọc trạng thái tạm thời thất bại. Worker được đánh dấu chưa xác minh và thao tác trên luồng bị khóa cho đến khi đọc lại được trạng thái; ứng dụng không dừng hoặc khởi động lại Worker hay FFmpeg.

- [Ghi chú và tệp phát hành v5.22.60.33](https://github.com/vat2003/vati-media-tool-live-releases/releases/tag/v5.22.60.33)
- [Tải installer Windows x64](https://github.com/vat2003/vati-media-tool-live-releases/releases/download/v5.22.60.33/vota-media-tool-live-amd64-installer-v5.22.60.33.exe)
- SHA-256: `f6409c93e4925d81b9c9d63b3298e8ea2bb7a96406ae8d289687a73d370c6265`

## Mã nguồn

Ứng dụng được xây dựng bằng Go, Wails và Svelte, sử dụng FFmpeg để xử lý luồng video. Xem mã nguồn và tài liệu kỹ thuật tại
