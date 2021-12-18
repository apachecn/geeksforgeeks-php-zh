# PHP 中 file_get_contents 和 cURL 的区别

> 原文:[https://www . geesforgeks . org/difference-file _ get _ contents-and-curl-in-PHP/](https://www.geeksforgeeks.org/difference-between-file_get_contents-and-curl-in-php/)

[**file _ get _ contents()****函数:**](https://www.geeksforgeeks.org/php-file_get_contents-function/) 这个 PHP 函数用来检索一个文件的内容。内容可以存储为字符串变量。或者，它也模拟 HTTP 事务，分别涉及通过 GET 方法的请求和使用 POST 方法的响应。首先，它最适合简单的 HTTP 操作和获取单行的 JSON 响应。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Reading contents from the
// GeeksforGeeks homepage
$homepage = file_get_contents(
  "https://www.geeksforgeeks.org/");

echo $homepage;

?>
```

**输出:**将重定向至[极客论坛](https://www.geeksforgeeks.org/)主页。

[**【cURL:**](https://www.geeksforgeeks.org/php-curl/)**它是一个第三方库，以一种高效得多的方式模拟 HTTP 请求和响应。它可以处理异步 HTTP 请求和复杂的通信，如回调函数或断点续传。它也适用于执行基于跨域的 FTP 请求。此外，它可以用于不同的应用，如代理设置和网站抓取等。**

****示例:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php

// From URL to get webpage contents
$url = "https://www.geeksforgeeks.org/";

// Initialize a CURL session.
$ch = curl_init();

// Return Page contents.
curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);

// Grab URL and pass it to the variable
curl_setopt($ch, CURLOPT_URL, $url);

$result = curl_exec($ch);

echo $result;

?>
```

****输出:**将重定向至[极客论坛](https://www.geeksforgeeks.org/)主页。**

<figure class="table">

| 文件 _ 获取 _ 内容()方法 | 卷曲 |
| --- | --- |
| Handle simple HTTP communication. | Handle complex HTTP communication. |
| Simple HTTP GET and HTTP POST operations are supported. | In addition to GET and POST requests, HTTP PUT and certificate are also supported. |
| Caching, cookies and so on are not supported. | Support caching, cookies progress report, etc. |
| It uses HTTP and HTTPS protocols to communicate. | 是阿云 http、https、ftp、ftps 哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟哟。 |
| It can be used to read file contents. | It can be used to read, edit, update and delete files on the server. |
| Running slowly. | Safe and fast operation. |
| Easy to understand. | Complicated and difficult to understand. |

</figure>