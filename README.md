# TurboTV — Cydia Repo

Repo Cydia của **TurboTV** — app xem YouTube 1080p cho iPad mini 1 (iOS 6 / iOS 9, chip A5) và iPad mini 2 (iOS 12).

## Thêm source vào Cydia

Mở Cydia → Sources → Edit → Add, dán URL:

```
https://twosix11D.github.io/TurboAsi4n/
```

Rồi vào repo **TurboTV** và cài **TurboTV 1.17**.

## Tải trực tiếp file .deb

[debs/com.bun.tubepro_1.17_iphoneos-arm.deb](debs/com.bun.tubepro_1.17_iphoneos-arm.deb) (2.261.662 byte, MD5 `a650dcb0039ff96dee0f2896006c7725`)

Chép file .deb sang iPad rồi mở bằng Filza → Cài đặt → Respring.

## Phiên bản hiện có

| Gói | Phiên bản | Ghi chú |
|---|---|---|
| com.bun.tubepro (TurboTV) | 1.17 | Sửa lỗi đăng nhập xong không phát được (gỡ Bearer khỏi /player); back không tự bật PiP; phát nền (không pause audio theo video stall); icon to hơn (tab 40pt, thanh Logo); xem live 1080p; mở được trang kênh; hẹn giờ tắt video; mục donate QR + PayPal (chờ link thật); 10 ngôn ngữ |

## Cấu trúc repo

- `debs/` — file .deb
- `Packages`, `Packages.gz`, `Packages.bz2` — danh sách gói cho Cydia/apt
- `Release` — thông tin repo
- `CydiaIcon.png` — icon hiển thị trong Cydia
- `index.html` — trang hướng dẫn (GitHub Pages)
