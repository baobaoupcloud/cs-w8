---
title : "Framework"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---
Tương tự như các thư viện của bên thứ ba mà chúng ta có thể tận dụng trong Python, có các thư viện của bên thứ ba được gọi là ***framework*** mà chúng ta có thể sử dụng với các tệp HTML của mình.

Bootstrap là một trong những framework mà chúng ta có thể sử dụng để làm đẹp HTML của mình và dễ dàng hoàn thiện các phần tử thiết kế để trang của chúng ta trở nên dễ đọc hơn.

Bootstrap có thể được sử dụng bằng cách thêm thẻ liên kết sau vào phần đầu của tệp HTML của bạn:
```html
<head>
      <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
    <title>favorites</title>
</head>
```
Xem xét HTML sau:
```html
<!DOCTYPE html>

<!-- Minh họa bảng -->

<html lang="en">
    <head>
        <title>phonebook</title>
    </head>
    <body>
        <table>
            <thead>
                <tr>
                    <th>Tên</th>
                    <th>Số điện thoại</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Carter</td>
                    <td>+1-617-495-1000</td>
                </tr>
                <tr>
                    <td>David</td>
                    <td>+1-617-495-1000</td>
                </tr>
                <tr>
                    <td>John</td>
                    <td>+1-949-468-2750</td>
                </tr>
            </tbody>
        </table>
    </body>
</html>
```

Bây giờ hãy xem xét HTML sau đây triển khai việc sử dụng Bootstrap:
```html
<!DOCTYPE html>

<!-- Minh họa bảng với Bootstrap -->

<html lang="en">
    <head>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
        <title>phonebook</title>
    </head>
    <body>
        <table class="table">
            <thead>
                <tr>
                    <th scope="col">Tên</th>
                    <th scope="col">Số điện thoại</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Carter</td>
                    <td>+1-617-495-1000</td>
                </tr>
                <tr>
                    <td>David</td>
                    <td>+1-949-468-2750</td>
                </tr>
            </tbody>
        </table>
    </body>
</html>
```
Trang web lúc này trông đẹp hơn nhiều nhờ vào Bootstrap.

Tương tự, chúng ta có thể trang trí web như đoạn code sau:
```html
<!DOCTYPE html>

<!-- Minh họa bố cục với Bootstrap -->

<html lang="en">
    <head>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
        <title>search</title>
    </head>
    <body>

        <div class="container-fluid">

            <ul class="m-3 nav">
                <li class="nav-item">
                    <a class="nav-link text-dark" href="https://about.google/">About</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link text-dark" href="https://store.google.com/">Store</a>
                </li>
                <li class="nav-item ms-auto">
                    <a class="nav-link text-dark" href="https://www.google.com/gmail/">Gmail</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link text-dark" href="https://www.google.com/imghp">Images</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link text-dark" href="https://www.google.com/intl/en/about/products">
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-grid-3x3-gap-fill" viewBox="0 0 16 16">
                            <path d="M1 2a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1V2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1V2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1V2zM1 7a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1V7zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1V7zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1V7zM1 12a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1v-2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1v-2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1v-2z"/>
                        </svg>
                    </a>
                </li>
                <li class="nav-item">
                    <a class="btn btn-primary" href="https://accounts.google.com/ServiceLogin" role="button">Đăng nhập</a>
                </li>
            </ul>

            <div class="text-center">

                <!-- https://knowyourmeme.com/memes/happy-cat -->
                <img alt="Happy Cat" class="img-fluid w-25" src="cat.gif">

                <form action="https://www.google.com/search" class="mt-4" method="get">
                    <input autocomplete="off" autofocus class="form-control form-control-lg mb-4 mx-auto w-50" name="q" placeholder="Query" type="search">
                    <button class="btn btn-light">Google Search</button>
                    <button class="btn btn-light" name="btnI">Tôi cảm thấy may mắn</button>
                </form>

            </div>

        </div>

    </body>
</html>
```
Phiên bản của trang này đã được thiết kế đẹp hơn nhiều nhờ vào Bootstrap.