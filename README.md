# Portfolio CV - K20 CNTT 20-04

**Tác giả:** Mai Lâm Duy

**Mô tả:** CV cá nhân dạng website tĩnh, giới thiệu thông tin, kỹ năng, dự án, học tập và liên hệ. Trang có biểu mẫu HTML thực hành; biểu mẫu không gửi email và không lưu dữ liệu lên máy chủ.

## Liên kết

- **Mã nguồn:** [GitHub repository](https://github.com/duy200779/K20_Portfolio_CNTT20-04)
- **Website:** [GitHub Pages](https://duy200779.github.io/K20_Portfolio_CNTT20-04/)
- **Hồ sơ tác giả:** [github.com/duy200779](https://github.com/duy200779)
- **Minh chứng:** website đã xuất bản và mã nguồn tại repository. Repo hiện không có ảnh chụp màn hình hoặc video minh chứng riêng.

## Cấu trúc thư mục

```text
.
├── index.html       # Trang CV chính
├── ket-qua.html     # Trang kết quả của biểu mẫu
├── README.md        # Hướng dẫn mở và kiểm tra sản phẩm
├── AI_LOG.md        # Ghi nhận hỗ trợ AI và quyết định
├── RELEASE_NOTES.md # Ghi chú bàn giao v7
├── css/
│   └── style.css    # Kiểu dáng và bố cục responsive
└── assets/
    ├── avatar.jpg
    ├── avatar.svg
    ├── du-an-1.svg
    ├── du-an-2.svg
    └── du-an-3.svg
```

## Chạy local

Không cần cài thư viện. Mở PowerShell tại thư mục gốc của repo và chạy:

```powershell
py -m http.server 8000
```

Nếu máy không có lệnh `py`, thử `python -m http.server 8000`. Mở <http://localhost:8000/> trong trình duyệt; nhấn `Ctrl+C` trong PowerShell để dừng máy chủ.

## Nguồn xuất bản

Website được cung cấp qua GitHub Pages tại liên kết ở trên; mã nguồn nằm trong repository. Cấu hình nhánh và thư mục nguồn xuất bản cần được xác nhận trong **Settings → Pages** của repository, vì cấu hình này không được mô tả trong các tệp dự án.

## Cách kiểm tra

1. Mở trang chính và xem các mục Giới thiệu, Kỹ năng, Dự án, Học tập, Liên hệ; thử các liên kết điều hướng.
2. Trong DevTools → **Network**, tải lại trang và xác nhận `css/style.css` cùng các ảnh trong `assets/` được tải. Đường dẫn CSS được khai báo tương đối là `css/style.css`.
3. Thu nhỏ cửa sổ trình duyệt để kiểm tra bố cục responsive.
4. Trong phần Liên hệ, thử gửi biểu mẫu khi để trống trường bắt buộc hoặc nhập email không hợp lệ để xem kiểm tra HTML5. Sau đó nhập dữ liệu mẫu hợp lệ để mở `ket-qua.html`.
5. Biểu mẫu dùng `GET`: dữ liệu có thể xuất hiện trên URL. Chỉ dùng dữ liệu thử, không nhập thông tin nhạy cảm. Trang kết quả không gửi email và không lưu dữ liệu.
6. Kiểm tra riêng trang `ket-qua.html`, nút quay lại, CSS và điều hướng về trang chính.

Khi ghi nhận kết quả kiểm thử, phân biệt trạng thái phản hồi HTTP `304` (tài nguyên không đổi và có thể dùng bản cache) với việc stylesheet đã tải và được trình duyệt áp dụng đúng.
