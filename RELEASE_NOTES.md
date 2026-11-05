# Release Notes — v7

## Thông tin bàn giao

- **Sản phẩm:** Portfolio CV - K20 CNTT 20-04
- **Phiên bản:** v7
- **Ngày cập nhật:** 2026-11-05
- **Tác giả:** Mai Lâm Duy
- **Website:** [GitHub Pages](https://duy200779.github.io/K20_Portfolio_CNTT20-04/)
- **Repository:** [duy200779/K20_Portfolio_CNTT20-04](https://github.com/duy200779/K20_Portfolio_CNTT20-04)

## Thay đổi chính

- Bàn giao CV website tĩnh gồm trang chính, trang kết quả biểu mẫu, CSS và tài nguyên hình ảnh.
- Bổ sung hướng dẫn chạy, kiểm tra và giới hạn của sản phẩm trong [README.md](README.md).
- Ghi lại dữ kiện, hỗ trợ AI, quyết định và trạng thái kiểm tra trong [AI_LOG.md](AI_LOG.md).

## Lỗi đã sửa

- Thay đường dẫn CSS tuyệt đối theo ổ đĩa Windows bằng `css/style.css` trong `index.html` và `ket-qua.html`, để liên kết tới stylesheet theo cấu trúc website. Thay đổi mã nguồn có trong [commit 238330e](https://github.com/duy200779/K20_Portfolio_CNTT20-04/commit/238330e915929d4b2f28c9ad1950236c92366bbd).

## Bản mã và commit liên quan

Commit mã nguồn liên quan: [`238330e915929d4b2f28c9ad1950236c92366bbd`](https://github.com/duy200779/K20_Portfolio_CNTT20-04/commit/238330e915929d4b2f28c9ad1950236c92366bbd). Tài liệu v7 đang được bổ sung trong working tree; chưa có commit phát hành riêng chứa các tài liệu này. Trước khi nộp, cần commit và push các tệp tài liệu để URL commit phát hành trỏ đúng bản bàn giao đầy đủ.

## Hạn chế còn lại

- Chưa kiểm tra trực quan trên trình duyệt rằng stylesheet đã được áp dụng sau khi tắt cache.
- `index.html` hiện thiếu thẻ đóng `</head>` trước `<body>`; cần sửa và kiểm tra HTML trước khi bàn giao.
- `ket-qua.html` vẫn hiển thị tên “Việt Anh/Trần Việt Anh”, không thống nhất với tên tác giả và trang chính.
- Biểu mẫu chỉ là thực hành HTML, dùng `GET`; dữ liệu nhập có thể hiện trên URL. Không gửi email, không lưu dữ liệu trên máy chủ.
- Cần xác nhận cấu hình nhánh/thư mục nguồn GitHub Pages trong **Settings → Pages**.
- Repo chưa có ảnh chụp hoặc video minh chứng riêng.

## Tiếp tục kiểm tra và bàn giao

Chạy local và làm theo danh sách trong [README.md](README.md). Kiểm tra CSS, Console, điều hướng và biểu mẫu ở cả hai trang; xử lý lỗi thẻ `</head>`; sau đó kiểm tra lại URL Pages. Cập nhật ghi chú này bằng kết quả thực tế, commit/push đầy đủ và dẫn link commit phát hành cuối cùng.
