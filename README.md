# TurboTV — Cydia Repo

Repo Cydia của **TurboTV** — app xem YouTube 1080p cho iPad mini 1 (iOS 6 / iOS 9, chip A5) và iPad mini 2 (iOS 12).

## Thêm source vào Cydia

Mở Cydia → Sources → Edit → Add, dán URL:

```
https://twosix11D.github.io/TurboAsi4n/
```

Rồi vào repo **TurboTV** và cài **TurboTV 1.16**.

## Tải trực tiếp file .deb

[debs/com.bun.tubepro_1.16_iphoneos-arm.deb](debs/com.bun.tubepro_1.16_iphoneos-arm.deb) (2.148.216 byte, MD5 `58e7c7095cf4f8c78f8e3eafc8f2f2e9`)

Chép file .deb sang iPad rồi mở bằng Filza → Cài đặt → Respring.

## Phiên bản hiện có

| Gói | Phiên bản | Ghi chú |
|---|---|---|
| com.bun.tubepro (TurboTV) | 1.16 | Sửa crash khi mở app (guard objectForKey ở lịch sử/WARP/SABR + breadcrumb); bỏ vạch ngang giữa các hàng; thẻ video glass bo tròn; Shorts đủ nội dung (avatar, Đăng ký, like, chia sẻ, mô tả); thanh điều khiển + drawer cố định; đăng nhập Google bằng mã kích hoạt (device flow); phát âm thanh dưới nền thật (Control Center/lock screen); mini player trong app + PiP iOS 9; icon + splash logo Long gửi (Splash C) |

## Cấu trúc repo

- `debs/` — file .deb
- `Packages`, `Packages.gz`, `Packages.bz2` — danh sách gói cho Cydia/apt
- `Release` — thông tin repo
- `CydiaIcon.png` — icon hiển thị trong Cydia
- `index.html` — trang hướng dẫn (GitHub Pages)
