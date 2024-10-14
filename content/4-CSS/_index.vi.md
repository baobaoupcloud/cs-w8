---
title : "CSS"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---
***CSS*** hay bảng định kiểu theo tầng là một ngôn ngữ đánh dấu cho phép bạn tinh chỉnh thẩm mỹ của các tệp HTML của mình.
CSS chứa các thuộc tính, bao gồm các cặp khóa-giá trị.

Trong terminal, nhập `code home.html` và viết mã như sau:
```html
<!DOCTYPE html>

<!-- Minh họa CSS nội tuyến với các thẻ P -->

<html lang="en">
    <head>
        <title>css</title>
    </head>
    <body>
        <p style="font-size: large; text-align: center;">
            John Harvard
        </p>
        <p style="font-size: medium; text-align: center;">
            Chào mừng đến trang chủ của tôi!
        </p>
        <p style="font-size: small; text-align: center;">
            Bản quyền &#169; John Harvard
        </p>
    </body>
</html>
```
Các thuộc tính `style` được cung cấp trong các thẻ `<p>`. Kích thước phông chữ được đặt là lớn, trung bình hoặc nhỏ. Sau đó, căn chỉnh văn bản được đặt ở giữa.

Tuy nhiên mã trên chưa được thiết kế tốt. Chúng ta có thể loại bỏ những phần dư thừa như sau:
```html
<!DOCTYPE html>

<!-- Loại bỏ DIV bên ngoài -->

<html lang="en">
    <head>
        <title>css</title>
    </head>
    <body style="text-align: center">
        <div style="font-size: large">
            John Harvard
        </div>
        <div style="font-size: medium">
            Chào mừng đến trang chủ của tôi!
        </div>
        <div style="font-size: small">
            Bản quyền &#169; John Harvard
        </div>
    </body>
</html>
```
Lưu ý rằng thẻ `<div>` được sử dụng để chia tệp HTML này thành các vùng cụ thể. `text-align: center` được gọi trong toàn bộ thẻ body của HTML. Bởi vì mọi thứ bên trong thẻ body là con của body, thuộc tính căn giữa sẽ được áp dụng cho các phần tử con đó.

Chúng ta có thể sửa đổi mã của mình như sau:
```html
<!DOCTYPE html>

<!-- Sử dụng thẻ ngữ nghĩa thay vì DIVs -->

<html lang="en">
    <head>
        <title>css</title>
    </head>
    <body style="text-align: center">
        <header style="font-size: large">
            John Harvard
        </header>
        <main style="font-size: medium">
            Chào mừng đến trang chủ của tôi!
        </main>
        <footer style="font-size: small">
            Bản quyền &#169; John Harvard
        </footer>
    </body>
</html>
```
Lưu ý rằng thẻ header và footer đều có các kiểu khác nhau được áp dụng.

Tuy nhiên, không nên đặt kiểu dáng và thông tin ở cùng một vị trí. Chúng ta có thể di chuyển các phần tử kiểu dáng lên đầu tệp như sau:
```html
<!-- Minh họa bộ chọn lớp (class selectors) -->

<html lang="en">
    <head>
        <style>

            .centered
            {
                text-align: center;
            }

            .large
            {
                font-size: large;
            }

            .medium
            {
                font-size: medium;
            }

            .small
            {
                font-size: small;
            }

        </style>
        <title>css</title>
    </head>
    <body class="centered">
        <header class="large">
            John Harvard
        </header>
        <main class="medium">
            Chào mừng đến trang chủ của tôi!
        </main>
        <footer class="small">
            Bản quyền &#169; John Harvard
        </footer>
    </body>
</html>
```
Chúng ta đã gán các lớp, được gọi là centered, large, medium và small cho các phần tử của mình, và chúng ta chọn những lớp đó bằng cách đặt một dấu chấm trước tên, như trong `.centered`.

Thực ra, chúng ta có thể di chuyển tất cả mã kiểu dáng của mình vào một tệp đặc biệt được gọi là tệp CSS. Chúng ta có thể tạo một tệp có tên `style.css` và dán các lớp của mình vào đó:
```css
.centered
{
    text-align: center;
}

.large
{
    font-size: large;
}

.medium
{
    font-size: medium;
}

.small
{
    font-size: small;
}
```
Đây là bản sao chính xác của những gì xuất hiện trong tệp HTML của chúng ta.

Sau đó, chúng ta có thể cho trình duyệt biết vị trí để tìm CSS cho tệp HTML này:
```html
<!DOCTYPE html>

<!-- Minh họa bảng định kiểu ngoại tuyến -->

<html lang="en">
    <head>
        <link href="style.css" rel="stylesheet">
        <title>css</title>
    </head>
    <body class="centered">
        <header class="large">
            John Harvard
        </header>
        <main class="medium">
            Chào mừng đến trang chủ của tôi!
        </main>
        <footer class="small">
            Bản quyền &#169; John Harvard
        </footer>
    </body>
</html>
```
Tệp `style.css` được liên kết với tệp HTML này dưới dạng một bảng định kiểu, cho trình duyệt biết vị trí để tìm các kiểu dáng mà chúng ta đã tạo.