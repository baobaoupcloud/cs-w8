---
title : "JavaScript"
date :  "`r Sys.Date()`" 
weight : 6 
chapter : false
pre : " <b> 6. </b> "
---
***JavaScript*** là một ngôn ngữ lập trình khác cho phép tương tác trên các trang web.

Xem xét việc triển khai tệp `hello.html` sau đây bao gồm cả JavaScript và HTML:
```html
<!DOCTYPE html>

<!-- Minh họa onsubmit -->

<html lang="en">
    <head>
        <script>

            function greet()
            {
                alert('xin chào, ' + document.querySelector('#name').value);
            }

        </script>
        <title>hello</title>
    </head>
    <body>
        <form onsubmit="greet(); return false;">
            <input autocomplete="off" autofocus id="name" placeholder="Tên" type="text">
            <input type="submit">
        </form>
    </body>
</html>
```
Script sử dụng `alert` để tạo một hộp thoại cảnh báo bật lên. `#name.value` truy cập vào hộp văn bản trên trang và lấy giá trị do người dùng nhập.

Chúng ta có thể nâng cấp mã của mình như sau:
```html
<!DOCTYPE html>

<!-- Minh họa DOMContentLoaded -->

<html lang="en">
    <head>
        <script>

            document.addEventListener('DOMContentLoaded', function() {
                document.querySelector('form').addEventListener('submit', function(e) {
                    alert('xin chào, ' + document.querySelector('#name').value);
                    e.preventDefault();
                });
            });

        </script>
        <title>hello</title>
    </head>
    <body>
        <form>
            <input autocomplete="off" autofocus id="name" placeholder="Tên" type="text">
            <input type="submit">
        </form>
    </body>
</html>
```
Phiên bản mã này tạo một `addEventListener` để lắng nghe khi biểu mẫu `submit` được kích hoạt. Lưu ý rằng `DOMContentLoaded` đảm bảo rằng toàn bộ trang được tải trước khi thực thi JavaScript.

JavaScript cho phép bạn đọc và sửa đổi động tệp HTML được tải vào bộ nhớ sao cho người dùng không cần tải lại để xem các thay đổi.
Hãy xem xét ví dụ HTML sau:
```html
<!DOCTYPE html>

<!-- Minh họa các thay đổi lập trình đối với kiểu dáng -->

<html lang="en">
    <head>
        <title>background</title>
    </head>
    <body>
        <button id="red">R</button>
        <button id="green">G</button>
        <button id="blue">B</button>
        <script>

            let body = document.querySelector('body');
            document.querySelector('#red').addEventListener('click', function() {
                body.style.backgroundColor = 'red';
            });
            document.querySelector('#green').addEventListener('click', function() {
                body.style.backgroundColor = 'green';
            });
            document.querySelector('#blue').addEventListener('click', function() {
                body.style.backgroundColor = 'blue';
            });

        </script>
    </body>
</html>
```
Lưu ý rằng JavaScript lắng nghe khi một nút cụ thể được nhấp. Sau khi nhấp, các thuộc tính kiểu dáng nhất định trên trang sẽ thay đổi. `body` được xác định là phần thân của trang. Sau đó, một sự kiện `listener` chờ đợi việc nhấp vào một trong các nút. Sau đó, thuộc tính `body.style.backgroundColor` được thay đổi.

Tương tự, hãy xem xét ví dụ sau:
```html
<!DOCTYPE html>

<html lang="en">
    <head>
        <script>

            // Bật tắt hiển thị lời chào
            function blink()
            {
                let body = document.querySelector('body');
                if (body.style.visibility == 'hidden')
                {
                    body.style.visibility = 'visible';
                }
                else
                {
                    body.style.visibility = 'hidden';
                }
            }

            // Nháy sau mỗi 500ms
            window.setInterval(blink, 500);

        </script>
        <title>blink</title>
    </head>
    <body>
        xin chào
    </body>
</html>
```
Ví dụ này nháy văn bản ở một khoảng thời gian nhất định. Lưu ý rằng `window.setInterval` nhận hai đối số: Một hàm sẽ được gọi và một khoảng thời gian chờ (tính bằng mili giây) giữa các lần gọi hàm.

Hãy xem xét ví dụ sau:
```html
<!DOCTYPE html>

<html lang="en">

    <head>
        <title>autocomplete</title>
    </head>

    <body>

        <input autocomplete="off" autofocus placeholder="Tìm kiếm" type="text">

        <ul></ul>

        <script src="large.js"></script>
        <script>
      
            let input = document.querySelector('input');
            input.addEventListener('keyup', function(event) {
                let html = '';
                if (input.value) {
                    for (word of WORDS) {
                        if (word.startsWith(input.value)) {
                            html += `<li>${word}</li>`;
                        }
                    }
                }
                document.querySelector('ul').innerHTML = html;
            });

        </script>

    </body>
</html>
```
Đây là một triển khai tự động hoàn thành của JavaScript. Điều này lấy từ một tệp có tên là `large.js`, là một danh sách các từ.

Chúng ta cũng có thể định vị địa lý bằng JavaScript:
```html
<!DOCTYPE html>

<html lang="en">
    <head>
        <title>geolocation</title>
    </head>
    <body>
        <script>
          
            navigator.geolocation.getCurrentPosition(function(position) {
                document.write(position.coords.latitude + ", " + position.coords.longitude);
            });

        </script>
    </body>
</html>
```
Điều này sẽ không hoạt động nếu máy tính hoặc trình duyệt của bạn không cho phép theo dõi vị trí.

Khả năng của JavaScript là rất nhiều. Chúng ta có thể tìm thêm trong [Tài liệu JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript).