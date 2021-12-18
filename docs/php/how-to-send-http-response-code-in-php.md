# 如何用 PHP 发送 HTTP 响应代码？

> 原文:[https://www . geesforgeks . org/how-send-http-response-code-in-PHP/](https://www.geeksforgeeks.org/how-to-send-http-response-code-in-php/)

**HTTP 响应代码:**根据版本的不同，有三种方法可以达到上述要求。

**对于 PHP 4.0 版本:**为了发送 HTTP 响应代码，我们需要组装响应代码。为此，请使用 header()函数。header()函数包含一个特殊的用例，它可以检测到一个 HTTP 响应行，并用一个定制的响应行替换它。

```php
header("HTTP/1.1 200 OK");
```

**示例:**

```php
$sapitype = php_sapi_name();
if (substr($sapitype, 0, 3) == 'cgi')
    header("Status: 404 Not Found");
else
    header("HTTP/1.1 404 Not Found");
```

**对于 PHP 4.3 版本:**使用第一种方法时明显有几个问题。最大的一个问题是，它部分由 PHP 解析，文档记录不佳。从 4.3 版本开始，header()函数有一个额外的第三个参数，通过它我们可以设置响应代码。但是要使用第一个参数，应该是一个非空字符串。

```php
header(':', true, 400);
header(‘X_PHP_Response_Code: 400', true, 400);

```

推荐第二种。此变体中的标题字段名称不规范，可以修改。

**对于 PHP 5.4 版本:**这个版本使用 http_response_code()函数让事情变得更简单。

```php
http_response_code(400);
```

**示例:**本示例使用 http_response_code()函数发送 http 响应代码。

```php
<?php

error_reporting(E_ERROR | E_PARSE);

// Initialize a variable into domain name
$domain1 = 'https://contribute.geeksforgeeks.org';

// Function to get HTTP response code 
function get_http_response_code($domain1) {
    $headers = get_headers($domain1);
    return substr($headers[0], 9, 3);
}

// Function call 
$get_http_response_code = get_http_response_code($domain1);

// Display the HTTP response code
echo $get_http_response_code;

// Check HTTP response code is 200 or not
if ( $get_http_response_code == 200 )
    echo "<br>HTTP request successfully";
else
    echo "<br>HTTP request not successfully!";

?>
```

**输出:**

```php
200
HTTP request successfully
```