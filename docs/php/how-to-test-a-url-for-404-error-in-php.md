# 如何在 PHP 中测试一个 URL 是否有 404 错误？

> 原文:[https://www . geesforgeks . org/how-test-a-URL-for-404-error-in-PHP/](https://www.geeksforgeeks.org/how-to-test-a-url-for-404-error-in-php/)

在 PHP 中，检查网页网址是否存在相对容易。如果所需的网址不存在，那么它将返回 404 错误。使用和不使用 cURL 库都可以进行检查。

**[cURL](https://www.geeksforgeeks.org/php-curl/):**cURL 的意思是‘URL 的客户端’，最初是用大写字母拼写 URL，以表明它处理 URL。它的发音是“看网址”。CUlR 项目有两个产品 libcurl 和 CUlR。

*   **libcurl:** 一个免费易用的客户端 url 传输库，支持 FTP、TPS、HTTP、HTTPS、GOPHER、TELNET、DICT、FILE、LDAP。libcurl 支持 TTPS 证书、HTTP POST、HTTP PUT、FTP 上传、kerberos、基于 HTTP 的上传、代理、cookies、用户&密码认证、文件传输恢复、HTTP 代理隧道等等。libcurl 免费、线程安全、兼容 IPv6、功能丰富、支持良好且速度快。
*   **curl:** 使用 url 语法获取或发送文件的命令行工具。由于 curl 使用 libcurl，它支持一系列常见的内部协议，目前包括 HTTP、HTTPS、FTP、FTPS、GOPHER、TELNET、DICT 和 FILE。

**示例 1:** 本示例在不使用 cURL 方法的情况下测试 URL 是否有 404 错误。

```php
<?php

// Creating a variable with an URL
// to be checked
$url = 'https://www.geeksforgeeks.org';

// Getting page header data
$array = @get_headers($url);

// Storing value at 1st position because
// that is only what we need to check
$string = $array[0];

// 404 for error, 200 for no error
if(strpos($string, "200")) {
    echo 'Specified URL Exists';
} 
else {
    echo 'Specified URL does not exist';
}

?>
```

**输出:**

```php
Specified URL exists
```

**示例 2:** 本示例使用 cURL 方法测试一个 URL 的 404 错误。

```php
<?php

// Initializing new session
$ch = curl_init("https://www.geeksforgeeks.org");

// Request method is set
curl_setopt($ch, CURLOPT_NOBODY, true);

// Executing cURL session
curl_exec($ch);

// Getting information about HTTP Code
$retcode = curl_getinfo($ch, CURLINFO_HTTP_CODE);

// Testing for 404 Error
if($retcode != 200) {
    echo "Specified URL does not exist";
}
else {
    echo "Specified URL exists";
}

curl_close($ch);

?>
```

**输出:**

```php
Specified URL exists
```