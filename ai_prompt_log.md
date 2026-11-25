# AI Prompt Log -- TechBugs Bug Hunter Registration

## 1. Mục đích

Tài liệu ghi lại các câu hỏi và yêu cầu thực tế đã trao đổi với AI trong
quá trình thực hiện bài tập **Xây dựng Cổng đăng ký "Chiến binh săn lỗi"
TechBugs**.

Nhật ký được tổng hợp theo thứ tự trao đổi trong cuộc hội thoại. Phần
"Mục đích" mô tả lý do đặt câu hỏi; không bổ sung câu hỏi giả, không
dựng thêm lượt trao đổi và không ghi nhận các prompt gợi ý trong đề bài
như thể học viên đã sử dụng chúng.

## 2. Nhật ký câu hỏi và mục đích sử dụng

### Giai đoạn 1 -- Khởi tạo dự án và tổ chức Git

**01. Câu hỏi thực tế**

> Tạo file README và tóm tắt đề bài.

**Mục đích:** Xác định nội dung cần đưa vào README để giới thiệu dự án
và tóm tắt yêu cầu bài tập.

**02. Câu hỏi thực tế**

> Lệnh tiếng Anh commit git: Khởi tạo và cập nhật file thông tin dự án
> README.

**Mục đích:** Chọn commit message tiếng Anh phù hợp cho việc khởi tạo và
cập nhật README.

**03. Câu hỏi thực tế**

> Lệnh tiếng Anh commit git: Khởi tạo mã nguồn Legacy Code của dự án.

**Mục đích:** Đặt commit message cho lần đưa mã nguồn HTML cũ (Legacy
Code) vào repository.

**04. Câu hỏi thực tế**

> Cách tạo git theo Git Flow chuyên nghiệp như khi làm tại công ty thực
> tế.

**Mục đích:** Tìm hiểu cấu trúc nhánh và quy trình Git Flow để áp dụng
cho dự án.

**05. Câu hỏi thực tế**

> Từ main tạo nhánh `develop` sau đó thì làm gì?

**Mục đích:** Xác định các bước tiếp theo sau khi tạo nhánh phát triển
từ `main`.

**06. Câu hỏi thực tế**

> Sau khi `git checkout -b develop` thì làm cái gì nữa, git push lên
> luôn à?

**Mục đích:** Làm rõ thời điểm và cách đẩy nhánh `develop` lên remote
repository.

### Giai đoạn 2 -- Tách nhánh và phát triển cấu trúc HTML

**07. Câu hỏi thực tế**

> Mã nguồn Legacy Code chỉ có các thẻ input rời rạc; nhánh feature đầu
> tiên cần sửa lại cấu trúc HTML và phân lớp semantic thì đặt tên nhánh
> thế nào cho phù hợp?

**Mục đích:** Đặt tên nhánh phản ánh đúng phạm vi tái cấu trúc HTML và
tổ chức các vùng nội dung theo ngữ nghĩa.

**08. Câu hỏi thực tế**

> Msg commit cho task chỉnh sửa lại cấu trúc HTML và phân lớp semantic
> rõ ràng bằng tiếng Anh.

**Mục đích:** Viết commit message mô tả việc tái cấu trúc HTML theo
semantic.

**09. Câu hỏi thực tế**

> Msg commit cho task merge `feature/registration-form-structure` vào
> `develop`.

**Mục đích:** Đặt merge commit message cho lần tích hợp nhánh cấu trúc
đăng ký vào `develop`.

### Giai đoạn 3 -- Phát triển Header, Main và Form

**10. Câu hỏi thực tế**

> Msg commit cho task thêm tiêu đề h2 cho header và thêm hr để kẻ line
> ngăn cách với phần dưới.

**Mục đích:** Đặt commit message cho thay đổi ở phần Header.

**11. Câu hỏi thực tế**

> Msg commit cho task `feature/header` vào `develop`.

**Mục đích:** Đặt merge message khi tích hợp Header vào nhánh phát
triển.

**12. Câu hỏi thực tế**

> Tên nhánh để chỉnh sửa phần main trong đó chứa form và các thông tin
> chính thì đặt tên ra sao?

**Mục đích:** Chọn tên nhánh cho phần nội dung chính và form đăng ký.

**13. Câu hỏi thực tế**

> Với đoạn `<fieldset>` chứa `<legend>` và
> `<input type="text" placeholder="Nhập tên">`, như này khi submit đi
> thì có gửi dữ liệu đi không, sửa thế nào?

**Mục đích:** Hiểu điều kiện để một trường input được gửi khi submit
form; làm rõ vai trò của thuộc tính `name` và cách liên kết `label`,
`for`, `id`.

**14. Câu hỏi thực tế**

> Msg commit cho nhánh `feature/main-content` sau khi sửa.

**Mục đích:** Đặt commit message cho phần Main chứa form đăng ký và các
trường dữ liệu.

**15. Câu hỏi thực tế**

> Msg merge `feature/main-content` vào `develop`.

**Mục đích:** Đặt merge message khi tích hợp Main Content vào `develop`.

### Giai đoạn 4 -- Hoàn thiện và kiểm tra nhánh phát triển

**16. Câu hỏi thực tế**

> Nhánh `develop` đã xong thì tiếp tục như nào?

**Mục đích:** Tìm hiểu các bước tiếp theo trong Git Flow sau khi hoàn
thành tích hợp các Feature.

**17. Câu hỏi thực tế**

> Trong mã hiện tại, hai radio đang trùng `id="level"` và hai checkbox
> trùng `id="platform"`. Cho mình msg commit.

**Mục đích:** Đặt commit message cho việc sửa ID trùng lặp, bảo đảm mỗi
phần tử có ID duy nhất.

**18. Câu hỏi thực tế**

> Msg merge `feature/main-content` sau khi sửa vào `develop`.

**Mục đích:** Đặt merge message cho lần cập nhật Main Content đã sửa
lỗi.

**19. Câu hỏi thực tế**

> `git push origin v1.0.0` thì sẽ có kết quả là gì?

**Mục đích:** Hiểu tác dụng của việc push Git Tag lên remote, phân biệt
Tag với Branch và biết cách kiểm tra Tag trên GitHub.

### Giai đoạn 5 -- Kiểm tra quy trình Git Flow và lịch sử thực tế

**20. Câu hỏi thực tế**

> Kiểm tra repository
> `https://github.com/dieppham999/techbugs-bug-hunter-registration`, xem
> đang sai quy trình Git Flow chỗ nào.

**Mục đích:** Đối chiếu lịch sử nhánh, commit, Pull Request, Release và
Tag thực tế với quy trình Git Flow.

**21. Câu hỏi thực tế**

> Với lỗi cho rằng `feature/registration-form-structure` không có Pull
> Request, xem có phải mình dùng lệnh `git merge` không?

**Mục đích:** Xác minh cách nhánh Feature được tích hợp vào `develop`,
phân biệt merge trực tiếp bằng Git với merge thông qua Pull Request.

**22. Câu hỏi thực tế**

> Vậy tại sao bạn lại bảo mình chưa merge?

**Mục đích:** Yêu cầu làm rõ sự khác nhau giữa trạng thái đã merge và
việc có hay không có Pull Request.

**23. Câu hỏi thực tế**

> Đưa bằng chứng thực tế cho kết luận
> `feature/registration-form-structure` đã được merge trực tiếp bằng
> `git merge`, không có PR riêng.

**Mục đích:** Kiểm tra bằng chứng từ commit SHA, parent commit, merge
commit và danh sách Pull Request; tránh kết luận chỉ dựa trên tên nhánh
hoặc nội dung file.

**24. Câu hỏi thực tế**

> Tổng hợp lại flow đúng mà tao đã làm và xem tao làm sai chỗ nào cần
> sửa gì để đúng theo Git Flow.

**Mục đích:** Tổng kết quy trình đã thực hiện, xác định các bước đúng,
thiếu hoặc chưa nhất quán và lập danh sách việc cần khắc phục.

### Giai đoạn 6 -- Release, Tag và đồng bộ nhánh

**25. Câu hỏi thực tế**

> Msg để merge `Release/1.0.0` vào `main`.

**Mục đích:** Đặt merge message cho bước đưa phiên bản Release vào nhánh
Production.

**26. Câu hỏi thực tế**

> Đã tạo PR Release vào `main` rồi thì tiếp theo làm gì?

**Mục đích:** Xác định các bước sau khi tạo và merge Release Pull
Request, đặc biệt là tạo Git Tag và hoàn tất phát hành.

**27. Nội dung thực tế đã gửi cho AI**

> Người dùng gửi kết quả chạy các lệnh `git pull origin main`,
> `git fetch --tags`, xóa Tag cũ, tạo và push lại `v1.0.0`, sau đó chạy
> `git show` và `git rev-parse`; kết quả `git rev-parse` phát sinh lỗi
> PowerShell.

**Mục đích:** Nhờ kiểm tra kết quả thao tác phát hành, xác minh Tag mới
trỏ đúng commit và xử lý lỗi cú pháp khi chạy lệnh trong PowerShell.

**28. Câu hỏi thực tế**

> Tại sao phải làm thao tác xóa Release Branch trên remote và local?

**Mục đích:** Hiểu lý do dọn dẹp nhánh tạm sau khi Release đã hoàn tất,
đồng thời phân biệt việc xóa nhánh với xóa commit hoặc Tag.

**29. Câu hỏi thực tế**

> Đồng bộ thay đổi Release về `develop` -- chỗ này mày hướng dẫn tao làm
> chưa?

**Mục đích:** Kiểm tra bước đồng bộ thay đổi từ Release về nhánh phát
triển có được thực hiện hay chưa.

**30. Câu hỏi thực tế**

> Vẽ lại toàn bộ quy trình Git Flow của dự án này và chỉ ra chỗ nào còn
> thiếu sót và cần sửa ra sao một cách trực quan.

**Mục đích:** Yêu cầu sơ đồ hóa toàn bộ lịch sử thực tế, chỉ ra các điểm
chưa đúng và hướng dẫn cách hoàn thiện.

## 3. Kết quả học tập rút ra từ quá trình trao đổi

Qua các câu hỏi thực tế trên, các nội dung đã được tìm hiểu gồm:

1.  Tổ chức nhánh `main`, `develop`, `feature/*`, `release/*` theo Git
    Flow.
2.  Đặt tên branch và commit message theo mục đích công việc.
3.  Phân biệt `git merge` trực tiếp với Pull Request trên GitHub.
4.  Đọc Git graph, commit SHA và parent commit để xác minh lịch sử tích
    hợp.
5.  Hiểu vai trò của Release Branch và Git Tag.
6.  Kiểm tra Tag đang trỏ đến commit nào.
7.  Phân biệt xóa branch với xóa commit và Tag.
8.  Hiểu việc đồng bộ thay đổi Release trở lại `develop`.
9.  Nhận diện các điểm cần cải thiện như tách PR theo Feature, Code
    Review, bảo vệ nhánh và dọn dẹp branch.

## 4. Ghi chú về tính trung thực của nhật ký

-   Nhật ký chỉ tổng hợp các câu hỏi, yêu cầu và nội dung thực tế xuất
    hiện trong cuộc hội thoại về dự án TechBugs.
-   Các câu hỏi gợi ý được in sẵn trong đề bài không được ghi nhận là
    prompt đã sử dụng, trừ khi người học thực sự gửi câu hỏi đó trong
    cuộc trò chuyện.
-   Không tự tạo thêm câu hỏi, câu trả lời, kết quả kiểm thử hoặc lịch
    sử Git.
-   Các mục mô tả lại nội dung người dùng gửi (ví dụ mục 27) được ghi rõ
    là nội dung thực tế đã gửi, không trình bày như một câu hỏi nguyên
    văn.
