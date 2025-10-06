# TẤT CẢ CÁC KIỂU DỮ LIỆU SỬ DỤNG TRONG SQL SERVER

## DANH SÁCH NHÓM KIỂU DỮ LIỆU CHÍNH
| Nhóm | Mô tả |
|-------|-------|
|Kiểu số nguyên|lưu trữ số nguyên|
|kiểu số thực|lưu số có phần thập phân|
|Kiểu chuỗi|lưu chữ, ký tự|
|kiểu ngày, giờ|lưu ngày, giờ|
|Kiểu logic|lưu giá trị true/false|
|Kiểu nhị phân|lưu dữ liệu dạng file, hình ảnh|
|Kiểu đặc biệt|dữ liệu lớn, duy nhất, JSON, XML,...|

### NHÓM SỐ NGUYÊN ( INTERGER TYPES )
|Kiểu|Dung lượng|Phạm vi|
|-------|-------|-------|
|TINYINT|1 BYTE|0 → 255|
|SMALLINT|2 BYTES|-32,768 → 32,767|
|INT|4 BYTES|-2,147,483,648 → 2,147,483,647|
|BIGINT|8 BYTES|rất lớn (~±9 tỷ tỷ)|

### KIỂU SỐ THỰC/ THẬP PHÂN (FLOAT/DECIMAL)
|Kiểu|Dung lượng|Mô tả|
|-------|-------|-------|
|DECIMAL(p, s) / NUMERIC(p, s)|Tùy|Số có độ chính xác cao (p: tổng chữ số, s: chữ số sau dấu phẩy)|
|FLOAT|8 bytes|Số thực (xấp xỉ)|
|REAL|4 bytes|Giống FLOAT nhưng nhỏ hơn|


### KIỂU CHUỖI
|Kiểu|Dung lượng|Mô tả|
|-------|-------|-------|
|CHAR(n)|Cố định (1–8000)|Chuỗi độ dài cố định|
|VARCHAR(n)|Linh hoạt (1–8000)|Chuỗi độ dài thay đổi|
|TEXT|Lên đến 2GB|Chuỗi dài (đã lỗi thời, nên dùng VARCHAR(MAX))|
|NCHAR(n)|2 bytes/ký tự|Hỗ trợ Unicode (tiếng Việt, tiếng Trung, …)|
|NVARCHAR(n)|2 bytes/ký tự|Unicode, độ dài thay đổ|
|NTEXT|2GB|Unicode dài (cũ, thay bằng NVARCHAR(MAX))|



### KIỂU NGÀY GIỜ
|Kiểu|Dung lượng|Mô tả|
|-------|-------|-------|
|DATE|3 bytes|Ngày (yyyy-mm-dd)|
|TIME|5 bytes|Giờ (hh:mm:ss.nnnnnnn)|
|DATETIME|8 bytes|Ngày + giờ (1753–9999)|
|SMALLDATETIME|4 bytes|Ngày + giờ (1900–2079)|
|DATETIME2|6–8 bytes|Độ chính xác cao hơn DATETIME|
|DATETIMEOFFSET|8–10 bytes|Có thêm thông tin múi giờ|


### KIỂU LOGIC
|Kiểu|Mô tả|
|-------|-------|
|BIT|Lưu giá trị 0, 1 hoặc NULL||


### KIỂU NHỊ PHÂN
|Kiểu|Mô tả|
|-------|-------|
|BINARY(n)|Dữ liệu nhị phân cố định||
|VARBINARY(n)|Nhị phân thay đổi||
|VARBINARY(MAX)|Dữ liệu lớn như hình ảnh, file, âm thanh||