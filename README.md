# TechBugs – Cổng đăng ký Chiến binh săn lỗi

## 1. Giới thiệu

Bài tập xây dựng lại biểu mẫu đăng ký tham gia chiến dịch **TechBugs – Chiến binh săn lỗi (Bug Hunters)** bằng **HTML5 thuần**, khắc phục các lỗi của mã nguồn cũ: thiếu thẻ `<form>`, thiếu nhãn `<label>`, không có thuộc tính `name` và sử dụng sai kiểu dữ liệu đầu vào.

**Mục tiêu:** Tạo biểu mẫu dễ sử dụng, có khả năng truy cập tốt, tự kiểm tra dữ liệu bằng HTML5 và minh họa cách gửi dữ liệu qua URL mà **không sử dụng JavaScript**.

## 2. Yêu cầu chức năng

| Dữ liệu cần thu thập | Thẻ/kiểu HTML gợi ý | Yêu cầu chính |
|---|---|---|
| Họ và tên | `input type="text"` | Có `id`, `name`, `required` và nhãn liên kết |
| Email liên hệ | `input type="email"` | Kiểm tra định dạng email; `required` |
| Mật khẩu | `input type="password"` | Che ký tự; `required`, `minlength="8"` |
| Trình độ | `input type="radio"` | Chọn **1 trong 3** mức; các nút cùng `name` |
| Nền tảng yêu thích | `input type="checkbox"` | Cho phép chọn **nhiều** nền tảng |
| Lý do tham gia | `textarea` | Nhập nội dung dài; có `name` và nhãn |
| Gửi đăng ký | `button type="submit"` | Kích hoạt gửi biểu mẫu |

**Quy tắc triển khai:**

- Bao bọc các trường bằng `<form action="" method="GET">` theo yêu cầu bài tập.
- Mỗi trường dữ liệu có thuộc tính `name` để tham gia vào dữ liệu gửi đi; dùng `id` duy nhất và `<label for="...">` trùng `id` để hỗ trợ thao tác và Accessibility.
- Sử dụng `required`, `type="email"`, `type="password"`, `minlength` phù hợp để trình duyệt tự kiểm tra dữ liệu.
- Có thể dùng `<fieldset>` và `<legend>` để nhóm các lựa chọn radio/checkbox rõ ràng hơn.
- Với nhóm radio bắt buộc, áp dụng `required` phù hợp; checkbox không nên bắt buộc tất cả các tùy chọn nếu đề không yêu cầu.

## 3. Quy trình thực hiện

1. **Phân tích:** Xác định lỗi của Legacy Code và các trường cần thu thập.
2. **Thiết kế:** Lập bảng ánh xạ trường dữ liệu – thẻ HTML – thuộc tính; xác định thứ tự bố cục.
3. **Triển khai:** Hoàn thiện `index.html`, liên kết nhãn và thêm HTML5 Validation.
4. **Kiểm thử:** Thử gửi biểu mẫu rỗng, email sai định dạng, mật khẩu ngắn và dữ liệu hợp lệ.

## 4. Chạy và kiểm thử

Mở `index.html` bằng trình duyệt (hoặc dùng VS Code Live Server). Không cần cài thư viện hay chạy JavaScript.

| Trường hợp thử nghiệm | Kết quả mong đợi |
|---|---|
| Bỏ trống trường bắt buộc rồi bấm **Đăng ký** | Trình duyệt yêu cầu nhập dữ liệu |
| Nhập email `abc.com` | Trình duyệt báo email không hợp lệ |
| Nhập mật khẩu dưới 8 ký tự | Trình duyệt chặn gửi và cảnh báo độ dài |
| Nhấp nhãn của một trường | Ô tương ứng được focus hoặc tùy chọn được chọn/bỏ chọn |
| Chọn một mức trình độ khác | Mức trình độ cũ tự bỏ chọn |
| Gửi dữ liệu hợp lệ | URL xuất hiện các tham số dạng `?fullname=...&email=...&level=...` |

**Lưu ý:** Các cặp `name=value` trên URL chỉ xuất hiện cho các trường được gửi thành công; checkbox không được chọn sẽ không được gửi. Tên tham số thực tế phụ thuộc vào các giá trị `name` trong `index.html`.

### Minh chứng cần chụp

- `screenshots/email-validation.png`: Thông báo lỗi khi nhập email sai định dạng.
- `screenshots/submit-url.png`: Thanh địa chỉ có các tham số sau khi gửi biểu mẫu hợp lệ.

> Chỉ thêm ảnh vào repository sau khi tự kiểm thử và chụp màn hình thật. **Không dùng mật khẩu thật** trong ảnh minh chứng.

## 5. Giải thích kiến thức trọng tâm (chuẩn bị vấn đáp)

**`id` và `name` khác nhau thế nào?** `id` định danh một phần tử trong trang, dùng để liên kết với `<label for="...">` và các mục đích khác. `name` là tên khóa được trình duyệt dùng khi gửi dữ liệu biểu mẫu cho máy chủ.

**Vì sao radio chỉ chọn được một trong ba?** Các ô radio có cùng giá trị `name` trong cùng biểu mẫu sẽ tạo thành một nhóm, nên mỗi lần chỉ chọn được một lựa chọn.

**Chuỗi tham số trên URL là gì?** Với `method="GET"`, trình duyệt mã hóa những trường hợp lệ thành các cặp `name=value`, nối bằng ký tự `&` trong phần query string sau dấu `?`.

**GET có an toàn cho mật khẩu không?** **Không.** `type="password"` chỉ che ký tự khi nhập, không mã hóa hoặc bảo vệ mật khẩu trong URL. Bài tập dùng GET để quan sát cơ chế truyền dữ liệu; trong ứng dụng thực tế phải gửi mật khẩu qua **POST trên HTTPS**, xử lý và lưu trữ an toàn ở phía máy chủ. Chỉ sử dụng mật khẩu giả khi thử nghiệm bài này.

## 6. Cấu trúc bài nộp

```text
techbugs-bug-hunter-registration/
├── index.html
├── README.md
├── ai_prompt_log.md
└── screenshots/
    ├── email-validation.png
    └── submit-url.png
```

Hai ảnh và các tệp trong cây thư mục trên là **danh sách cần hoàn thiện**, không có nghĩa chúng đã được tạo sẵn.

## 7. Checklist trước khi nộp

- [ ] Hoàn thành `index.html` đúng chuẩn HTML5, form dùng GET.
- [ ] Tất cả trường thu thập dữ liệu có `name`, nhãn có liên kết `for`–`id` phù hợp.
- [ ] Có đủ 3 mức trình độ, cho phép chọn nhiều nền tảng và nhập lý do tham gia.
- [ ] Kiểm thử các trường hợp thiếu dữ liệu, email sai, mật khẩu ngắn và submit hợp lệ.
- [ ] Chụp và đưa 2 ảnh minh chứng thật vào `screenshots/`.
- [ ] Ghi `ai_prompt_log.md` bằng **các câu hỏi thực tế đã trao đổi với AI** cùng mục đích, không dựng lịch sử giả.
- [ ] Đưa toàn bộ bài lên GitHub hoặc đóng gói file nén để nộp.

## 8. Tiêu chí chấm điểm

| Tiêu chí | Tỷ trọng |
|---|---:|
| Chất lượng form, validation và accessibility | **40%** |
| Giải thích và bảo vệ mã nguồn khi vấn đáp | **40%** |
| Tương tác AI có chiều sâu, ghi nhật ký prompt | **20%** |
