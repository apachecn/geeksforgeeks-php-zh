# PHP|cURL

> Original: [https://www.geeksforgeeks.org/php-curl/](https://www.geeksforgeeks.org/php-curl/)

Curl 代表“urls 的客户端”，最初的 url 拼写为大写，以表明它处理的是 urls。 它的发音是“查看 URL”。 Curl 项目有两个产品 libcurl 和 curl。

*   **libcurl：**一个免费且易于使用的客户端 URL 转移库，支持 FTP、TPS、HTTP、HTTPS、Gopher、Telnet、DICT、FILE 和 LDAP。 Libcurl 支持 TTPS 证书、HTTP POST、HTTP PUT、FTP 上传、Kerberos、基于 HTTP 的上传、代理、Cookie、用户&密码验证、文件传输恢复、HTTP 代理隧道等等。 Libcurl 免费、线程安全、兼容 IPv6、功能丰富、支持良好且速度快。
*   **curl：**使用 URL 语法获取或发送文件的命令行工具。 由于 cURL 使用 libcurl，因此它支持一系列常见的内部协议，目前包括 HTTP、HTTPS、FTP、FTPS、Gopher、Telnet、DICT 和 FILE。

**什么是 PHP/curl？**或
PHP 模块，使 PHP 程序能够访问 PHP 中的 curl 函数。 PHP 中启用了 cURL 支持，phpinfo()函数将显示在其输出中。 在用 PHP 编写您的第一个简单程序之前，请检查它。

## PHP

```
<?php

phpinfo();

?>
```

**简单用法：**使用 HTTP 进行的最简单、最常见的请求/操作是获取 URL。 URL 本身可以指向网页、图像或文件。 客户端向服务器发出 GET 请求并接收它请求的文档。
**一些基本卷曲功能：**和

*   *curl_init()*函数将初始化一个新会话并返回一个 cURL 句柄。
*   *curl_exec($ch)*函数应在初始化 cURL 会话并设置了该会话的所有选项后调用。 其目的只是执行预定义的 cURL 会话(由 ch 给出)。
*   *curl_setopt($ch，option，value)*设置由 ch 参数标识的 cURL 会话的选项。 Option 指定要设置的选项，value 指定给定选项的值。
*   *curl_setopt($ch，CURLOPT_RETURNTRANSFER，1)*返回页面内容。 如果设置为 0，则不会返回任何输出。
*   *curl_setopt($ch，CURLOPT_URL，$url)*将 URL 作为参数传递。 这是您的目标服务器网站地址。 这是您要从互联网上获取的 URL。
*   *curl_exec($ch)*抓取 URL 并将其传递给变量以显示输出。
*   *curl_close($ch)*关闭 cURL 资源，释放系统资源。

**示例：**和

## PHP

```
<?php

// From URL to get webpage contents.
$url = "https://www.geeksforgeeks.org/";

// Initialize a CURL session.
$ch = curl_init();

// Return Page contents.
curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);

//grab URL and pass it to the variable.
curl_setopt($ch, CURLOPT_URL, $url);

$result = curl_exec($ch);

echo $result;

?>
```

发帖主题：Re：Колибри0.7.8.0

![output](img/f218372a8c2d0fe84004ad420793a8da.png)

**引用：**[http://php.net/manual/en/book.curl.php](http://php.net/manual/en/book.curl.php)