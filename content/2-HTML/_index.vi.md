---
title : "HTML"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
***HTML*** là ngôn ngữ đánh dấu siêu văn bản bao gồm các thẻ, mỗi thẻ có thể có một số thuộc tính để mô tả nó.
Trong terminal của bạn, nhập `code hello.html` và viết mã như sau:

```html
<!DOCTYPE html>

<!-- Minh họa HTML -->

<html lang="en">
    <head>
        <title>hello, title</title>
    </head>
    <body>
        hello, body
    </body>
</html>
```
Thẻ `html` mở và đóng tệp này. Thuộc tính `lang` sửa đổi hành vi của thẻ `html`. Cũng chú ý rằng có các thẻ `head` và các thẻ `body`. Không bắt buộc thụt lề nhưng nên sử dụng giúp thể hiện rõ hệ thống phân cấp.

Hệ thống phân cấp của các thẻ có thể được biểu diễn như sau:

![Hệ thống phân cấp](https://raw.githubusercontent.com/baobaoupcloud/cs-w8/main/static/images/2.html/html1.png)

Kiến thức về hệ thống phân cấp này sẽ hữu ích sau này khi chúng ta học JavaScript.

Trình duyệt sẽ đọc tệp HTML của bạn từ trên xuống dưới và từ trái sang phải.
Do khoảng trắng và thụt lề bị bỏ qua trong HTML, bạn sẽ cần sử dụng thẻ đoạn văn `<p>` để mở và đóng một đoạn văn. Hãy xem ví dụ sau:

```html
<!DOCTYPE html>

<!-- Minh họa đoạn văn -->

<html lang="en">

    <head>
        <title>Headings</title>
    </head>

    <body>
        <p>
            Đây là văn bản mẫu minh họa việc sử dụng tiêu đề. 
        </p>
        <p>
            Phần này tiếp tục minh họa việc sử dụng tiêu đề.
        </p>
        <p>
            Phần này đi sâu hơn vào nội dung.
        </p>
        <p>
            Phần này nhấn mạnh các điểm chính và giới thiệu những thông tin liên quan bổ sung cho các phần trước.
        </p>
        <p>
            Phần phụ này chứa các ghi chú và lưu ý quan trọng mà người đọc nên ghi nhớ khi khám phá chủ đề.
        </p>
        <p>
            Cuối cùng, phần này kết thúc và tóm tắt những điểm cần lưu ý về chủ đề.
        </p>

    </body>
</html>
```
Các đoạn văn bắt đầu bằng thẻ `<p>` và kết thúc bằng thẻ `</p>`.

HTML cho phép biểu diễn các tiêu đề:
```html
<!DOCTYPE html>

<!-- Minh họa tiêu đề (cho các chương, phần, tiểu mục, v.v.) -->

<html lang="en">

    <head>
        <title>Headings</title>
    </head>

    <body>

        <h1>Một</h1>
        <p>
            Đây là văn bản mẫu minh họa việc sử dụng tiêu đề. 
        </p>

        <h2>Hai</h2>
        <p>
            Phần này tiếp tục minh họa việc sử dụng tiêu đề.
        </p>

        <h3>Ba</h3>
        <p>
            Phần này đi sâu hơn vào nội dung.
        </p>

        <h4>Bốn</h4>
        <p>
            Phần này nhấn mạnh các điểm chính và giới thiệu những thông tin liên quan bổ sung cho các phần trước.
        </p>

        <h5>Năm</h5>
        <p>
            Phần phụ này chứa các ghi chú và lưu ý quan trọng mà người đọc nên ghi nhớ khi khám phá chủ đề.
        </p>

        <h6>Sáu</h6>
        <p>
            Cuối cùng, phần này kết thúc và tóm tắt những điểm cần lưu ý về chủ đề.
        </p>

    </body>
</html>
```
Lưu ý rằng `<h1>`, `<h2>`, và `<h3>` chỉ ra các mức độ tiêu đề khác nhau.

Chúng ta cũng có thể tạo danh sách không có thứ tự trong HTML:
```html

<!DOCTYPE html>

<!-- Minh họa danh sách không có thứ tự -->

<html lang="en">
    <head>
        <title>list</title>
    </head>
    <body>
        <ul>
            <li>một</li>
            <li>hai</li>
            <li>ba</li>
        </ul>
    </body>
</html>
```
Lưu ý rằng thẻ `<ul>` tạo ra danh sách không có thứ tự chứa ba mục.

Chúng ta cũng có thể tạo danh sách có thứ tự trong HTML:
```html
<!DOCTYPE html>

<!-- Minh họa danh sách có thứ tự -->

<html lang="en">
    <head>
        <title>list</title>
    </head>
    <body>
        <ol>
            <li>một</li>
            <li>hai</li>
            <li>ba</li>
        </ol>
    </body>
</html>
```
Lưu ý rằng thẻ `<ol>` tạo ra danh sách có thứ tự chứa ba mục.

Chúng ta cũng có thể tạo bảng trong HTML:
```html
<!DOCTYPE html>

<!-- Minh họa bảng -->

<html lang="en">
    <head>
        <title>table</title>
    </head>
    <body>
        <table>
            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
            </tr>
            <tr>
                <td>4</td>
                <td>5</td>
                <td>6</td>
            </tr>
            <tr>
                <td>7</td>
                <td>8</td>
                <td>9</td>
            </tr>
            <tr>
                <td>*</td>
                <td>0</td>
                <td>#</td>
            </tr>
        </table>
    </body>
</html>
```

Hình ảnh cũng có thể được sử dụng trong HTML:
```html
<!DOCTYPE html>

<!-- Minh họa hình ảnh -->

<html lang="en">
    <head>
        <title>image</title>
    </head>
    <body>
        <img alt="photo of bridge" src="bridge.png">
    </body>
</html>
```
`src="bridge.png"` chỉ ra đường dẫn nơi tệp hình ảnh có thể được tìm thấy.

Video cũng có thể được thêm trong HTML:
```html
<!DOCTYPE html>

<!-- Minh họa video -->

<html lang="en">
    <head>
        <title>video</title>
    </head>
    <body>
        <video controls muted>
            <source src="video.mp4" type="video/mp4">
        </video>
    </body>
</html>
```
Thuộc tính type chỉ định rằng đây là một video thuộc loại mp4.

Bạn cũng có thể liên kết giữa các trang web khác nhau:
```html
<!DOCTYPE html>

<!-- Minh họa liên kết -->

<html lang="en">
    <head>
        <title>link</title>
    </head>
    <body>
       Truy cập <a href="https://www.harvard.edu">Harvard</a>.
    </body>
</html>
```
Lưu ý rằng thẻ `<a>` hay thẻ liên kết được sử dụng để làm cho từ Harvard trở thành văn bản có thể nhấp vào.

Các thẻ meta được sử dụng để giữ thông tin về dữ liệu bên trong tệp HTML. Xem xét ví dụ sau:
```html
<!DOCTYPE html>

<!-- Minh họa thiết kế đáp ứng -->

<html lang="en">
    <head>
        <meta name="viewport" content="initial-scale=1, width=device-width">
        <title>meta</title>
    </head>
    <body>
        Đây là văn bản giữ chỗ được sử dụng trong thiết kế và xuất bản để điền vào các khu vực nội dung.
    </body>
</html>
```
Lưu ý rằng tập hợp các thuộc tính meta này làm cho trang này thân thiện với thiết bị di động.

Có rất nhiều cặp khóa-giá trị meta mà bạn có thể sử dụng:
```html
<!DOCTYPE html>

<!-- Minh họa thẻ Open Graph -->

<html lang="en">
    <head>
        <meta property="og:title" content="CS50">
        <meta property="og:description" content="Giới thiệu về các doanh nghiệp trí tuệ của khoa học máy tính và nghệ thuật lập trình.">
        <meta property="og:image" content="cat.jpg">
        <title>meta</title>
    </head>
    <body>
        ...
    </body>
</html>
```
Lưu ý rằng các cặp khóa-giá trị này liên quan đến tiêu đề và mô tả của trang web.

Bạn cũng có thể tạo các biểu mẫu tương tự như Google Tìm kiếm:
```html
<!DOCTYPE html>

<!-- Minh họa biểu mẫu -->

<html lang="en">
    <head>
        <title>search</title>
    </head>
    <body>
        <form action="https://www.google.com/search" method="get">
            <input name="q" type="search">
            <input type="submit" value="Google Search">
        </form>
    </body>
</html>
```
Lưu ý rằng một thẻ `form` mở ra và cung cấp thuộc tính của hành động mà nó sẽ thực hiện. Trường nhập được bao gồm truyền tên q và loại là tìm kiếm.

Chúng ta có thể làm cho tìm kiếm này tốt hơn như sau:
```html
<!DOCTYPE html>

<!-- Minh họa các thuộc tính biểu mẫu bổ sung -->

<html lang="en">
    <head>
        <title>search</title>
    </head>
    <body>
        <form action="https://www.google.com/search" method="get">
            <input autocomplete="off" autofocus name="q" placeholder="Query" type="search">
            <button>Google Search</button>
        </form>
    </body>
</html>
```
Lưu ý rằng tính năng autocomplete đã được tắt. Tính năng autofocus đã được bật.

Trên đây chỉ là một vài trong số rất nhiều phần tử HTML mà bạn có thể thêm vào trang web của mình. Nếu bạn có ý tưởng muốn thêm điều gì đó vào trang web mà chưa đề cập (như nút bấm, tệp âm thanh,...), hãy thử tìm kiếm trên Google cụm từ “X trong HTML” để tìm cú pháp chính xác! Tương tự, bạn có thể sử dụng cs50.ai để khám phá thêm các tính năng khác của HTML!