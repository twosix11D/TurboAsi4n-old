# TurboTV — Cydia Repo

Repo Cydia của **TurboTV** — app xem YouTube 1080p cho iPad mini 1 (iOS 6 / iOS 9, chip A5) và iPad mini 2 (iOS 12).

## Thêm source vào Cydia

Mở Cydia → Sources → Edit → Add, dán URL:

```
https://twosix11D.github.io/TurboAsi4n/
```

Rồi vào repo **TurboTV** và cài **TurboTV 1.17.1**.

## Tải trực tiếp file .deb

[debs/com.bun.tubepro_1.17.1_iphoneos-arm.deb](debs/com.bun.tubepro_1.17.1_iphoneos-arm.deb) (2.357.240 byte, MD5 `be480682949770aadd77636a75bbdd6e`)

Chép file .deb sang iPad rồi mở bằng Filza → Cài đặt → Respring.

## Phiên bản hiện có

| Gói | Phiên bản | Ghi chú |
|---|---|---|
| com.bun.tubepro (TurboTV) | 1.17.1 | Mục donate dùng link PayPal thật (paypal.me/turboasi4n) + mã VietQR nhận tiền của Long, lời kêu gọi ủng hộ đổi theo ngôn ngữ app. Giữ nguyên mọi tính năng 1.17 |

## Cấu trúc repo

- `debs/` — file .deb
- `Packages`, `Packages.gz`, `Packages.bz2` — danh sách gói cho Cydia/apt
- `Release` — thông tin repo
- `CydiaIcon.png` — icon hiển thị trong Cydia
- `index.html` — trang hướng dẫn (GitHub Pages)
