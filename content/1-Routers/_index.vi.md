---
title : "Bộ định tuyến"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
#### Bộ định tuyến (Routers)
Để chuyển dữ liệu từ nơi này đến nơi khác, chúng ta cần phải đưa ra các quyết định định tuyến. Tức làà sẽ cần lập trình cách dữ liệu được truyền từ điểm A đến điểm B.

Bạn có thể hình dung cách dữ liệu có thể đi qua nhiều tuyến đường khác nhau từ điểm A đến điểm B, sao cho khi một bộ định tuyến bị tắc nghẽn, dữ liệu có thể đi qua tuyến đường khác. Các gói dữ liệu được chuyển từ bộ định tuyến này sang bộ định tuyến khác, từ máy tính này sang máy tính khác.

#### TCP/IP
TCP/IP là hai giao thức cho phép các máy tính truyền dữ liệu giữa chúng qua internet.

***IP*** là cách mà các máy tính có thể nhận diện lẫn nhau trên internet. Mỗi máy tính có một địa chỉ duy nhất trên thế giới. Địa chỉ có dạng như sau:
```bash
  #.#.#.#
```
Các con số dao động từ 0 đến 255. Địa chỉ IP là 32-bit, có nghĩa là các địa chỉ này có thể chứa hơn 4 tỷ địa chỉ. Phiên bản mới hơn của địa chỉ IP, sử dụng 128-bit, có thể chứa được nhiều máy tính hơn nữa!
Trong thực tế, các máy chủ làm rất nhiều công việc cho chúng ta.


***TCP*** là giao thức điều khiển truyền dẫn, được sử dụng để phân biệt các dịch vụ web với nhau. Ví dụ, số 80 được sử dụng để chỉ HTTP và số 443 được sử dụng để chỉ HTTPS. Các con số này là các số cổng.

Khi thông tin được gửi từ vị trí này đến vị trí khác, một địa chỉ IP nguồn, một địa chỉ IP đích, và số cổng TCP được gửi.

Các giao thức này cũng được sử dụng để chia nhỏ các tệp lớn thành nhiều phần hoặc gói tin. Ví dụ, một bức ảnh lớn về một con mèo có thể được gửi trong nhiều gói tin. Khi một gói tin bị mất, TCP/IP có thể yêu cầu các gói tin bị mất từ máy chủ gốc.
TCP sẽ xác nhận khi tất cả dữ liệu đã được truyền và nhận.

#### DNS
Sẽ rất khó để nhớ một địa chỉ IP để truy cập một trang web.

***DNS*** hay hệ thống tên miền là tập hợp các máy chủ trên internet được sử dụng để định tuyến địa chỉ website như harvard.edu đến một địa chỉ IP cụ thể.

DNS chỉ đơn giản là giữ một bảng hoặc cơ sở dữ liệu liên kết tên miền đầy đủ cụ thể với địa chỉ IP cụ thể.

#### HTTP
***HTTP***, giao thức truyền siêu văn bản, là một giao thức cấp ứng dụng mà các nhà phát triển sử dụng để xây dựng các công cụ mạnh mẽ và hữu ích thông qua việc truyền dữ liệu từ nơi này sang nơi khác.

Khi bạn thấy một địa chỉ như https://www.example.com, bạn thực sự đang truy cập địa chỉ đó với một dấu gạch chéo `/` ở cuối nó.

Đường dẫn là những gì tồn tại sau dấu gạch chéo đó. Ví dụ: https://www.example.com/folder/file.html truy cập vào example.com và duyệt đến thư mục folder và sau đó truy cập tệp tên là `file.html`.

`.com` được gọi là tên miền cấp cao nhất, được sử dụng để chỉ định vị trí hoặc loại tổ chức liên quan đến địa chỉ này.

`https` trong địa chỉ này là giao thức được sử dụng để kết nối với địa chỉ web đó. Bằng cách sử dụng giao thức, chúng ta có nghĩa là HTTP sử dụng các yêu cầu `GET` hoặc `POST` để yêu cầu thông tin từ một máy chủ.

Ví dụ: bạn có thể khởi chạy Google Chrome, nhấp chuột phải và chọn inspect. Khi bạn mở công cụ dành cho nhà phát triển và truy cập tab Network, chọn Preserve log, bạn sẽ thấy các yêu cầu như `GET`. Điều này cũng có thể thực hiện được trên các trình duyệt khác, sử dụng các phương pháp hơi khác một chút.
Ví dụ, khi gửi yêu cầu `GET`, máy tính của bạn có thể gửi những thông tin sau tới một máy chủ:
```
  GET / HTTP/2
  Host: www.harvard.edu
```
Lưu ý rằng yêu cầu này qua HTTP là yêu cầu nội dung được phục vụ trên www.harvard.edu.

Thông thường, sau khi gửi một yêu cầu đến máy chủ, bạn sẽ nhận được các giá trị sau trong Response Headers:
```
  HTTP/2 200
  Content-Type: text/html
```
Cách tiếp cận này để kiểm tra các bản ghi có thể phức tạp hơn mức cần thiết. Bạn có thể phân tích hoạt động của các giao thức HTTP tại cs50.dev. Ví dụ, nhập lệnh sau vào cửa sổ terminal của bạn:
```bash
  curl -I https://www.harvard.edu/
```
Lưu ý rằng kết quả của lệnh này trả về tất cả các giá trị header của phản hồi từ máy chủ.

Thông qua công cụ dành cho nhà phát triển trong trình duyệt web của bạn, bạn có thể thấy tất cả các yêu cầu HTTP khi duyệt đến trang web trên.
Thử thực hiện lệnh sau trong cửa sổ terminal của bạn:
```bash
  curl -I https://harvard.edu
```
Lưu ý rằng bạn sẽ thấy phản hồi 301, cung cấp một gợi ý cho trình duyệt về nơi có thể tìm thấy trang web chính xác.

Tương tự, hãy thực hiện lệnh sau trong cửa sổ terminal của bạn:
```bash
  curl -I http://www.harvard.edu/
```
Lưu ý rằng chữ `s` trong https đã bị xóa. Máy chủ sẽ cho thấy rằng phản hồi là 301, có nghĩa là trang web đã được di chuyển vĩnh viễn.

Tương tự như mã 301, mã 404 có nghĩa là URL được chỉ định không được tìm thấy. Có nhiều mã phản hồi khác như:

- **200 OK**: Thành công - Yêu cầu đã được xử lý thành công.
- **301 Moved Permanently**: Đã chuyển vĩnh viễn - Tài nguyên đã được di chuyển vĩnh viễn đến một URL khác.
- **302 Found**: Đã tìm thấy - Tài nguyên tạm thời được di chuyển đến một URL khác.
- **304 Not Modified**: Không thay đổi - Tài nguyên không có sự thay đổi kể từ lần yêu cầu cuối.
- **307 Temporary Redirect**: Chuyển hướng tạm thời - Tài nguyên tạm thời được di chuyển đến một URL khác.
- **401 Unauthorized**: Không được phép - Yêu cầu cần xác thực người dùng (thường yêu cầu đăng nhập).
- **403 Forbidden**: Bị cấm - Người dùng không có quyền truy cập tài nguyên này.
- **404 Not Found**: Không tìm thấy - Không tìm thấy tài nguyên được yêu cầu.
- **418 I'm a Teapot**: Tôi là một cái ấm trà - Mã phản hồi vui nhộn của giao thức "Hyper Text Coffee Pot Control Protocol" (HTCPCP), chỉ ra rằng máy chủ là một ấm trà và không thể pha cà phê.
- **500 Internal Server Error**: Lỗi máy chủ nội bộ - Máy chủ gặp lỗi không mong đợi.
- **503 Service Unavailable**: Dịch vụ không sẵn sàng - Máy chủ tạm thời không thể xử lý yêu cầu (thường là do quá tải hoặc bảo trì).

