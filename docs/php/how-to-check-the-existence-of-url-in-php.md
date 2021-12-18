# PHP 中如何检查 URL 的存在？

> 原文:[https://www . geesforgeks . org/如何检查 php 中 url 的存在/](https://www.geeksforgeeks.org/how-to-check-the-existence-of-url-in-php/)

可以通过检查响应头中的状态代码来检查网址的存在。状态码 200 是成功的 HTTP 请求的标准响应，状态码 404 表示网址不存在。

**使用的功能:**

*   **get_headers()函数:**它获取服务器响应 HTTP 请求发送的所有头。
*   [strpos()函数:](https://www.geeksforgeeks.org/php-strpos-stripos-functions/)此函数用于将一个字符串的第一个匹配项查找到另一个字符串中。

**示例 1:** 本示例检查响应标题中的状态代码 200。如果状态代码为 200，则表示网址存在，否则不存在。

```
<?php

// Initialize an URL to the variable
$url = "https://www.geeksforgeeks.org";

// Use get_headers() function
$headers = @get_headers($url);

// Use condition to check the existence of URL
if($headers && strpos( $headers[0], '200')) {
    $status = "URL Exist";
}
else {
    $status = "URL Doesn't Exist";
}

// Display result
echo($status);

?>
```

**输出:**

```
URL Exist

```

**示例 2:** 该示例检查响应报头中的状态代码 404。如果状态代码为 404，则表明网址不存在，否则网址存在。

```
<?php

// Initialize an URL to the variable
$url = "https://www.geeksforgeeks.org";

// Use get_headers() function
$headers = @get_headers($url);

// Use condition to check the existence of URL
if($headers || strpos( $headers[0], '404')) {
    $status = "URL Doesn't Exist";
}
else {
    $status = "URL Exist";
}

// Display result
echo($status);

?>
```

**输出:**

```
URL Doesn't Exist

```

**示例 3:** 本示例使用 curl_init()方法检查 url 的存在。

```
<?php

// Initialize an URL to the variable
$url = "https://www.geeksfgeeks.org";

// Use curl_init() function to initialize a cURL session
$curl = curl_init($url);

// Use curl_setopt() to set an option for cURL transfer
curl_setopt($curl, CURLOPT_NOBODY, true);

// Use curl_exec() to perform cURL session
$result = curl_exec($curl);

if ($result !== false) {

    // Use curl_getinfo() to get information
    // regarding a specific transfer
    $statusCode = curl_getinfo($curl, CURLINFO_HTTP_CODE); 

    if ($statusCode == 404) {
        echo "URL Doesn't Exist";
    }
    else {
        echo "URL Exist";
    }
}
else {
    echo "URL Doesn't Exist";
}

?>
```

**输出:**

```
URL Doesn't Exist

```