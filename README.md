# TurboTV — Cydia Repo

Repo Cydia của **TurboTV** — app xem YouTube 1080p cho iPad mini 1 (iOS 6 / iOS 9, chip A5) và iPad mini 2 (iOS 12).

## Thêm source vào Cydia

Mở Cydia → Sources → Edit → Add, dán URL:

```
https://twosix11D.github.io/TurboAsi4n/
```

Rồi vào repo **TurboTV** và cài **TurboTV 1.15.2**.

## Tải trực tiếp file .deb

[debs/com.bun.tubepro_1.15.2_iphoneos-arm.deb](debs/com.bun.tubepro_1.15.2_iphoneos-arm.deb) (972.556 byte, MD5 `27e70e95cdfb2c4c2ce8b0ddbde2ba3c`)

Chép file .deb sang iPad rồi mở bằng Filza → Cài đặt → Respring.

## Phiên bản hiện có

| Gói | Phiên bản | Ghi chú |
|---|---|---|
| com.bun.tubepro (TurboTV) | 1.15.2 | Sửa crash khi tua (bỏ qua SIGPIPE); 4 theme glass; lịch sử xem; lấy stream bằng VISIONOS 1.02 |

## Cấu trúc repo

- `debs/` — file .deb
- `Packages`, `Packages.gz`, `Packages.bz2` — danh sách gói cho Cydia/apt
- `Release` — thông tin repo
- `CydiaIcon.png` — icon hiển thị trong Cydia
- `index.html` — trang hướng dẫn (GitHub Pages)
