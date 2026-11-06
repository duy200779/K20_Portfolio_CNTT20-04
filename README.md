# Portfolio CV - K20 CNTT 20-04

## Sản phẩm này là gì?

Website CV cá nhân của Mai Lâm Duy, sinh viên Công nghệ Thông tin, giới thiệu kỹ năng, dự án học tập, quá trình học tập và thông tin liên hệ.

## Demo

https://duy200779.github.io/K20_Portfolio_CNTT20-04/

## Tính năng

- Xem thông tin giới thiệu, kỹ năng, ba dự án học tập, học tập và liên hệ.
- Dùng menu hoặc nút **Xem dự án** để chuyển tới từng mục trên trang.
- Gửi lời nhắn qua biểu mẫu HTML có kiểm tra các trường bắt buộc, định dạng email và độ dài nội dung; biểu mẫu chuyển tới trang kết quả thực hành.
- Bố cục thích ứng với kích thước màn hình.

## Cách mở

1. Mở URL ở mục Demo.
2. Chọn các mục trên thanh điều hướng hoặc cuộn trang để xem nội dung.
3. Ở mục **Liên hệ**, có thể thử biểu mẫu với dữ liệu mẫu hợp lệ để mở trang kết quả. Đây chỉ là biểu mẫu thực hành: không gửi email và không lưu dữ liệu.

Để chạy bản trong máy, mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Sau đó mở <http://localhost:8000/>. Nếu máy không có lệnh `py`, dùng `python -m http.server 8000`. Nhấn `Ctrl+C` trong PowerShell để dừng máy chủ.

## Cấu trúc thư mục

```text
index.html       Trang CV chính
ket-qua.html     Trang kết quả biểu mẫu
css/             Kiểu dáng và bố cục responsive
assets/          Ảnh đại diện và hình minh họa dự án
docs/            Nhật ký AI và chỉ mục minh chứng
```

## Đã kiểm tra

Xem [docs/evidence-index.md](docs/evidence-index.md); hiện chưa có minh chứng kiểm thử được liệt kê tại đây. [docs/AI_LOG.md](docs/AI_LOG.md) ghi nhận đường dẫn stylesheet tương đối trong hai trang và stylesheet công khai trả về nội dung CSS, nhưng chưa xác nhận CSS được áp dụng trực quan sau khi tắt cache.

## Hạn chế / Chưa kiểm tra

- Chưa xác nhận CSS được áp dụng trực quan trên trình duyệt hoặc thử nghiệm trên thiết bị di động.
- Chưa xác nhận cấu hình nguồn xuất bản trong GitHub Pages (**Settings → Pages**).
- Biểu mẫu dùng `GET`, nên dữ liệu thử có thể xuất hiện trên URL; không nhập thông tin nhạy cảm.
- Trang `ket-qua.html` còn tên “Việt Anh”, chưa thống nhất với trang chính.
- `index.html` đang thiếu thẻ đóng `</head>` trước `<body>`; cần sửa và kiểm tra HTML.
- Các liên kết dự án hiện là nội dung hiển thị, chưa phải liên kết bấm được tới mã nguồn.

## Khai báo AI

Xem [docs/AI_LOG.md](docs/AI_LOG.md) để biết yêu cầu, gợi ý, quyết định và trạng thái kiểm tra liên quan đến việc sử dụng AI.
