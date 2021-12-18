# PHP|get_headers()函数

> Original: [https://www.geeksforgeeks.org/php-get_headers-function/](https://www.geeksforgeeks.org/php-get_headers-function/)

PHP 中的**get_headers()函数**用于获取服务器在响应 HTTP 请求时发送的所有标头。

**语法：**

```
get_headers( $url, $format, $context )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$url：**它是字符串类型的强制参数。 它定义了目标 URL。
*   **$format：**它是 int 类型的可选参数。 如果它的值设置为非零，它将返回一个关联数组，否则将返回索引数组。
*   **$CONTEXT：**它保存 STREAM_CONTEXT_CREATE()函数创建的有效资源上下文。

**示例 1：**在此示例中，未分配可选参数**$format**的值。

```
<?php

// Target URL
$url = "https://www.geeksforgeeks.org";

// Fetching headers
$headers = get_headers($url);

// Printing headers
print_r($headers);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array (
     [0] => HTTP/1.1 200 OK 
     [1] => Content-Type: text/html; charset=UTF-8 
     [2] => Connection: close 
     [3] => Date: Sun, 19 May 2019 08:31:29 GMT 
     [4] => Server: Apache 
     [5] => Strict-Transport-Security: max-age=3600; includeSubDomains 
     [6] => Cache-Control: s-maxage=21600, max-age=3, must-revalidate 
     [7] => Access-Control-Allow-Credentials: true 
     [8] => X-Frame-Options: DENY 
     [9] => X-Content-Type-Options: nosniff 
     [10] => Vary: Accept-Encoding, Cookie 
     [11] => X-Cache: Miss from cloudfront 
     [12] => Via: 1.1 aa0bb866c09b4e243eb9a97bcdb7fe32.cloudfront.net (CloudFront) 
     [13] => X-Amz-Cf-Id: QAOIIj4eBsrX0hyZ-UHjOtqA2dQePcLbEUZJ3KRohjsSPfcrcAFaiQ== 
) 

```

**示例 2：**在本例中，可选参数**$format**的值设置为非零。

```
<?php

// Target URL
$url = "https://www.geeksforgeeks.org";

// Fetching headers
$headers = get_headers($url, 1);

// Printing headers
print_r($headers);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( 
        [0] => HTTP/1.1 200 OK 
        [Content-Type] => text/html; charset=UTF-8 
        [Connection] => close 
        [Date] => Sun, 19 May 2019 08:35:47 GMT 
        [Server] => Apache 
        [Strict-Transport-Security] => max-age=3600; includeSubDomains 
        [Cache-Control] => s-maxage=21600, max-age=3, must-revalidate 
        [Access-Control-Allow-Credentials] => true 
        [X-Frame-Options] => DENY 
        [X-Content-Type-Options] => nosniff 
        [Vary] => Accept-Encoding, Cookie 
        [X-Cache] => Miss from cloudfront 
        [Via] => 1.1 95d17b4d563934eb90636ad03f8f524e.cloudfront.net (CloudFront) 
        [X-Amz-Cf-Id] => se3QRyaWDeuHI3GrisMzAr4FJBamqMtbUNzhTPqAJhBoQZbWvy3UPw== 
) 

```