# 使用 PHP 刷新页面

> 原文:[https://www.geeksforgeeks.org/refresh-a-page-using-php/](https://www.geeksforgeeks.org/refresh-a-page-using-php/)

使用 [header()函数](https://www.geeksforgeeks.org/php-header-function/)在 PHP 中刷新一个网页。HTTP 函数是那些在发送任何其他输出之前操纵由网络服务器发送到客户机或浏览器的信息的函数。函数的作用是:以原始形式向客户端或浏览器发送一个 HTTP 头。在将 HTML、XML、JSON 或其他输出发送到浏览器或客户端之前，原始数据会与服务器发出的请求(尤其是 HTTP Request)一起作为标头信息发送。HTTP 头提供了关于消息正文中发送的对象的必要信息，更准确地说是关于请求和响应的信息。

**语法:**

```php
void header( $header, $replace = TRUE, $http_response_code )
Or
header(string, replace, http_response_code)

```

**参数:**

*   **$header:** 它保存头字符串。有两种类型的标题调用。第一个报头以字符串“HTTP/”开头，该字符串用于计算要发送的 HTTP 状态代码。标题的第二种情况是“位置”:它是强制参数。
*   **$replace:** 为可选参数。它表示标头应该替换先前的标头或添加第二个标头。默认值为真(将替换)。如果$replace 值为 False，则强制多个相同类型的头。
*   **$http_response_code:** 为可选参数。它将 HTTP 响应代码强制为指定的值(PHP 4.3 及更高版本)。

**注意:**此功能防止一次发送多个报头。这是针对 PHP 4.4 发布后的头注入攻击的保护。

下面的例子说明了在 PHP 中如何使用 header()来刷新当前页面:

**示例:**本示例使用 header()函数每 3 秒刷新一次网页。

```php
<?php

// Demonstrate the use of header() function
// to refresh the current page

echo "Welcome to index page</br>";
echo "Page will refresh in every 3 seconds</br></br>";

// The function will refresh the page 
// in every 3 second
header("refresh: 3");

echo date('H:i:s Y-m-d');

exit;
?>
```

**输出:**

<video class="wp-video-shortcode" id="video-290369-1" width="665" height="373" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20190404004757/Untitled-Project.mp4?_=1">[https://media.geeksforgeeks.org/wp-content/uploads/20190404004757/Untitled-Project.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20190404004757/Untitled-Project.mp4)</video>

**示例 2:** 本示例使用 header()函数将网页重定向到另一个页面。

```php
<?php

// Demonstrate the use of header() function
// to refresh the current page

echo "Welcome to index page</br>";
echo "we will redirect to GeeksForGeeks Official website in 3 second";

// The function will redirect to geeksforgeeks official website
header("refresh: 3; url = https://www.geeksforgeeks.org/");

exit;
?>
```

**输出:**

<video class="wp-video-shortcode" id="video-290369-2" width="665" height="373" preload="metadata" controls=""><source type="video/mp4" src="https://media.geeksforgeeks.org/wp-content/uploads/20190404005742/Untitled.mp4?_=2">[https://media.geeksforgeeks.org/wp-content/uploads/20190404005742/Untitled.mp4](https://media.geeksforgeeks.org/wp-content/uploads/20190404005742/Untitled.mp4)</video>

**参考文献:**T2】https://www.php.net/manual/en/function.header.php

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。