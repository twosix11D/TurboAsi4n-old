# TurboTV — Repo (Cydia / Sileo / Zebra)

Repo của **TurboTV** — app xem YouTube 1080p cho iPad mini 1 (iOS 6 / iOS 9, chip A5), iPad mini 2 (iOS 12), iPhone và iPod touch. Dùng được với **Cydia, Sileo và Zebra** (cùng 1 URL source).

## Thêm source

**Nhập đúng URL này** (có dấu `/` cuối, KHÔNG phải link github.com):

```
https://twosix11D.github.io/TurboAsi4n/
```

- **Cydia:** Sources → Edit → Add, dán URL → Add Source.
- **Sileo:** Sources → dấu `+`, dán URL → Add Source, rồi Refresh.
- **Zebra:** Sources → Add, dán URL → Add.

Rồi vào repo **TurboTV** và cài **TurboTV 1.17.5**.

## Tải trực tiếp file .deb

[debs/com.bun.tubepro_1.17.5_iphoneos-arm.deb](debs/com.bun.tubepro_1.17.5_iphoneos-arm.deb) (2.974.592 byte, MD5 `c0dc76718cc4a80ec0ec4b17059eb73b`)

Chép file .deb sang iPad rồi mở bằng Filza → Cài đặt → Respring.

## Phiên bản hiện có

| Gói | Phiên bản | Ghi chú |
|---|---|---|
| com.bun.tubepro (TurboTV) | 1.17.5 | Sửa lỗi "lúc xem được lúc báo lỗi" (LOGIN_REQUIRED ngẫu nhiên): retry giãn cách 6 lượt VISIONOS → ANDROID (2s) → WEB (5s) → VISIONOS với visitorData mới (10s) → ANDROID với visitorData mới → TV kèm token khi đã đăng nhập; log từng lượt (client, visitorData 12 ký tự, trạng thái YouTube); sửa 2 lỗi khiến đăng nhập Google im lặng (poll token bị hủy khi mở Safari; lỗi mạng thoáng qua làm poll dừng hẳn); màn lỗi hiện đủ câu + nút "Thử lại". Menu phát kiểu Troubadour (Fill the screen, Reload video, Stats for nerds); màn phát thêm Chapters, Comments, số dislike; màn Cài đặt riêng kiểu Troubadour (tài khoản, ngôn ngữ, giao diện, video, chặn WARP, giới thiệu) + kiểm tra cập nhật trong Cài đặt (không popup tự động); vuốt xuống thu nhỏ video về mini player; nhấn giữ phát nhanh 2x; chụm 2 ngón phóng to; Shorts prefetch Short kế tiếp (chỉ link + thumbnail, không tải video về máy); mini player thành thẻ nổi góc dưới-phải. PO token/SABR vẫn chưa giải được (Google khóa key), WEB ẩn danh vẫn không lấy được stream. Giữ nguyên 1.17.4 (iPhone/iPod touch; bố cục màn hình hẹp) + 1.17.3 (sửa LOGIN_REQUIRED ngẫu nhiên; log chẩn đoán đăng nhập; sửa phát nền im khi bấm Home) + 1.17.2 (Back thu nhỏ mini player; lặp lại video; bấm Home tự vào PiP; sửa kẹt phát nền; sửa log ghi version; depiction cho Cydia/Sileo/Zebra; bố cục dists/ chuẩn Debian + Packages.xz) + donate PayPal thật (paypal.me/turboasi4n) + mã VietQR của 1.17.1 và mọi tính năng 1.17 |

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
