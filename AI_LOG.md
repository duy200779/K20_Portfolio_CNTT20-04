# AI_LOG

## Hiện tượng và dữ kiện ban đầu

- Hiện tượng được báo cáo: website không hiển thị CSS.
- Dữ kiện người dùng cung cấp: yêu cầu trang chính trả về HTTP `304`.
- HTTP `304` chỉ cho biết tài nguyên được coi là chưa thay đổi so với bản đã cache; riêng status này không xác định nguyên nhân giao diện thiếu CSS.
- Khi kiểm tra mã ở lần phân tích ban đầu, `index.html` và `ket-qua.html` khai báo CSS bằng đường dẫn ổ đĩa Windows (`D:\CNTT20-04\portfolio\css\style.css`), trong khi stylesheet của repo nằm tại `css/style.css`.

## Nhận định trước khi hỏi AI

Ghi chú ban đầu trong repo chỉ là “không hiện css”; chưa có dữ liệu Network của riêng yêu cầu stylesheet hoặc lỗi Console để kết luận nguyên nhân. Đường dẫn tuyệt đối trên máy Windows là nghi vấn cần kiểm tra vì không phải URL tới tệp CSS trên GitHub Pages.

## AI được sử dụng và yêu cầu

Có sử dụng AI (trợ lý Copilot SDK trong VS Code). Yêu cầu tóm tắt: “Hãy nêu giả thuyết, dữ kiện cần kiểm tra và bản sửa tối thiểu. Chỉ tư vấn, không sửa tệp.”

## Gợi ý của AI

- Kiểm tra URL, status và initiator của yêu cầu stylesheet trong DevTools → Network; xem lỗi liên quan trong Console.
- Đổi `href` của stylesheet thành đường dẫn tương đối trong các trang HTML, ví dụ `css/style.css`.
- Không xem riêng status `304` của trang HTML là bằng chứng CSS tải thành công hay thất bại.

## Quyết định và lý do

Trong mã nguồn hiện tại, cả `index.html` và `ket-qua.html` đều trỏ đến `css/style.css`. Thay đổi này có trong commit `238330e` ([xem commit](https://github.com/duy200779/K20_Portfolio_CNTT20-04/commit/238330e915929d4b2f28c9ad1950236c92366bbd)). Đây là đường dẫn tương đối phù hợp với cấu trúc repo và URL triển khai dạng project site.

## Phần sửa và kết quả kiểm tra đã biết

- Commit nêu trên thay đường dẫn ổ đĩa Windows bằng đường dẫn tương đối ở hai trang.
- Khi xem mã HTML đang được website công khai trả về, cả hai trang đều khai báo `css/style.css`; URL stylesheet công khai cũng trả về nội dung CSS khi được truy cập.
- Chưa xác nhận bằng trình duyệt thực tế rằng CSS được áp dụng trực quan; chưa có kết quả kiểm tra Network/Console sau khi tải lại với cache tắt.
- Khi rà soát mã hiện tại, thấy `index.html` thiếu thẻ đóng `</head>` trước `<body>`. Đây là điểm cần sửa và kiểm tra riêng, chưa được xử lý trong thay đổi tài liệu này.

## Cách thử lại

1. Mở trang Pages hoặc chạy local theo hướng dẫn trong [README.md](README.md).
2. Trong DevTools → Network, bật **Disable cache**, tải lại trang và xác nhận yêu cầu `css/style.css` trả về nội dung CSS; xem cả Console.
3. Xác nhận kiểu dáng và bố cục đã được áp dụng; kiểm tra tương tự ở `ket-qua.html`.
4. Kiểm tra thẻ `<head>` của `index.html` đã đóng đúng trước `<body>`.
5. Thử điều hướng và biểu mẫu theo README. Ghi lại kết quả thật sau khi thực hiện; các bước này chưa được xác nhận hoàn tất tại thời điểm ghi log.