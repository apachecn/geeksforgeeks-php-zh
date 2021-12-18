# PHP|Header()函数

> Original: [https://www.geeksforgeeks.org/php-header-function/](https://www.geeksforgeeks.org/php-header-function/)

Header()函数是 PHP 中的一个内置函数，用于发送原始 HTTP 标头。 HTTP 函数是那些在发送任何其他输出之前处理由 Web 服务器发送到客户端或浏览器的信息的函数。 函数作用是：以原始形式向客户端或浏览器发送 HTTP 标头。 在将 HTML、XML、JSON 或其他输出发送到浏览器或客户端之前，原始数据与服务器发出的请求(尤其是 HTTP 请求)一起作为头信息发送。 HTTP 标头提供了有关在消息正文中发送的对象的所需信息，更准确地提供了有关请求和响应的信息。

**语法：**

```php
void header( $header, $replace = TRUE, $http_response_code )
```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **$Header:** this parameter saves the title string. There are two types of header calls. The first header begins with the string "HTTP/" and is used to determine the HTTP status code to be sent. The second case of Header is "Location:". Required parameters.
*   **$REPLACE:** optional parameters. It indicates that the title should replace the previous title or add a second title. The default value is True (will be replaced). If the $replace value is FALSE, multiple headers of the same type are forced.
*   **$HTTP_RESPONSE_CODE:** optional parameters. It forces the HTTP response code to the specified value (PHP 4.3 and later).

**返回值：**此函数不返回任何值。

**示例 1：**

```php
<?php
// PHP program to describes header function

// Redirect the browser
header("Location: https://www.geeksforgeeks.org");

// The below code does not get executed 
// while redirecting
exit;

?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**

```php
<?php
// PHP program to describes header function

// Set a past date
header("Expires: Sun, 25 Jul 1997 06:02:34 GMT");
header("Cache-Control: no-cache");
header("Pragma: no-cache");
?>

<html>
    <body>
        <p>Hello World!</p>

        <!-- PHP program to display
        header list -->
        <?php
            print_r(headers_list());
        ?>
    </body>
</html>
```

发帖主题：Re：Колибри0.7.8.0

上述示例通过将覆盖浏览器设置的标头信息发送到非缓存来帮助防止缓存。

**注意：**示例中多次使用 Header()函数，因为一次只允许发送一个报头(从 PHP 4.4 开始)，以防止报头注入攻击。

**用法：**

*   Change the page location
*   Set time zone
*   Set cache control
*   Start forced download
*   Send HTTP status

**引用：**[http://php.net/manual/en/function.header.php](http://php.net/manual/en/function.header.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。