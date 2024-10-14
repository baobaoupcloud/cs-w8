---
title : "Biểu thức chính quy"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---
***Biểu thức chính quy*** hay regexes là một phương tiện để đảm bảo rằng dữ liệu do người dùng cung cấp tuân theo một định dạng cụ thể.

Chúng ta có thể triển khai trang đăng ký của riêng mình sử dụng biểu thức chính quy như sau:
```html
<!DOCTYPE html>

<!-- Minh họa type="email" -->

<html lang="en">
    <head>
        <title>register</title>
    </head>
    <body>
        <form>
            <input autocomplete="off" autofocus name="email" placeholder="Email" type="email">
            <button>Register</button>
        </form>
    </body>
</html>
```
Thẻ nhập `form` bao gồm các thuộc tính chỉ định rằng đây là kiểu email. Trình duyệt biết cách kiểm tra lại rằng dữ liệu nhập là một địa chỉ email.

Mặc dù trình duyệt sử dụng các thuộc tính tích hợp này để kiểm tra địa chỉ email, chúng ta có thể thêm thuộc tính mẫu (pattern) để đảm bảo rằng chỉ dữ liệu cụ thể mới được nhập vào địa chỉ email:
```html
<!DOCTYPE html>

<!-- Minh họa thuộc tính pattern -->

<html lang="en">
    <head>
        <title>register</title>
    </head>
    <body>
        <form>
            <input autocomplete="off" autofocus name="email" pattern=".+@.+\.edu" placeholder="Email" type="email">
            <button>Register</button>
        </form>
    </body>
</html>
```
Thuộc tính `pattern` được cung cấp một biểu thức chính quy để chỉ định rằng địa chỉ email phải bao gồm ký tự `@` và `.edu`.