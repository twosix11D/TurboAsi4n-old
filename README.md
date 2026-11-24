# TurboTV — Repo (Cydia / Sileo / Zebra)

Repo của **TurboTV** — app xem YouTube 1080p cho iPad mini 1 (iOS 6 / iOS 9, chip A5) và iPad mini 2 (iOS 12). Dùng được với **Cydia, Sileo và Zebra** (cùng 1 URL source).

## Thêm source

**Nhập đúng URL này** (có dấu `/` cuối, KHÔNG phải link github.com):

```
https://twosix11D.github.io/TurboAsi4n/
```

- **Cydia:** Sources → Edit → Add, dán URL → Add Source.
- **Sileo:** Sources → dấu `+`, dán URL → Add Source, rồi Refresh.
- **Zebra:** Sources → Add, dán URL → Add.

Rồi vào repo **TurboTV** và cài **TurboTV 1.17.3**.

## Tải trực tiếp file .deb

[debs/com.bun.tubepro_1.17.3_iphoneos-arm.deb](debs/com.bun.tubepro_1.17.3_iphoneos-arm.deb) (2.374.070 byte, MD5 `a0911c5e027802e928571ccd8b72f263`)

Chép file .deb sang iPad rồi mở bằng Filza → Cài đặt → Respring.

## Phiên bản hiện có

| Gói | Phiên bản | Ghi chú |
|---|---|---|
| com.bun.tubepro (TurboTV) | 1.17.3 | Sửa lỗi LOGIN_REQUIRED ngẫu nhiên (tự seed lại visitorData mới rồi thử lại, tối đa 5 lần; áp dụng cả SABR); log chẩn đoán đăng nhập từng bước (lấy mã / chờ kích hoạt / lỗi Google); thử lại bằng client TV kèm token khi đã đăng nhập; sửa phát nền im ngay khi bấm Home (luôn kích hoạt âm thanh nền song song với PiP + ghi log trạng thái phát 1s/3s/10s sau khi vào nền). Giữ nguyên 1.17.2 (Back thu nhỏ mini player; lặp lại video; bấm Home tự vào PiP; sửa kẹt phát nền; sửa log ghi version; depiction cho Cydia/Sileo/Zebra; bố cục dists/ chuẩn Debian + Packages.xz) + donate PayPal thật (paypal.me/turboasi4n) + mã VietQR của 1.17.1 và mọi tính năng 1.17 |

## Cấu trúc repo

- `debs/` — file .deb
- `Packages`, `Packages.gz`, `Packages.bz2`, `Packages.xz` — danh sách gói (flat, cho Cydia; Sileo thử `.xz` trước nên phải có đủ)
- `Release` — thông tin repo (flat, cho Cydia)
- `dists/stable/Release` + `dists/stable/main/binary-iphoneos-arm/Packages*` — bố cục Debian chuẩn (Sileo tìm Release ở đây; không có là Sileo báo "Could not find release file")
- `depiction.html` — trang mô tả gói (Cydia/Zebra)
- `depiction.json` — mô tả native cho Sileo (theo schema developer.getsileo.app/native-depictions)
- `CydiaIcon.png` — icon hiển thị trong trình quản lý gói
- `index.html` — trang hướng dẫn (GitHub Pages)

## Sinh lại repo khi lên bản mới

```sh
./regen_repo.sh ../tubepro/packages/com.bun.tubepro_<ban-moi>_iphoneos-arm.deb
```

Script ở `~/workspace/ios6-toolchain/v1172-patches/regen_repo.sh` (không upload lên GitHub): copy .deb mới, sinh Packages bằng `apt-ftparchive` (giữ nguyên viết hoa `SileoDepiction` — `dpkg-scanpackages` sẽ đổi thành `Sileodepiction`), nén đủ 4 dạng, copy sang `dists/`, sinh 2 file Release (có `Date`, hash md5/sha1/sha256 khớp file thật) rồi tự kiểm chứng.
