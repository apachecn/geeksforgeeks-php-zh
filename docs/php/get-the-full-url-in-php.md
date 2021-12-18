# 获取 PHP 中的完整网址

> 原文:[https://www.geeksforgeeks.org/get-the-full-url-in-php/](https://www.geeksforgeeks.org/get-the-full-url-in-php/)

在本文中，我们将看到如何使用 PHP 获取当前运行页面的完整 URL，以及通过示例了解它们的实现。$_SERVER 是 PHP 中的一个[超级全局](https://www.geeksforgeeks.org/php-superglobals/)变量，它包含与头、路径和脚本位置相关的细节。HTTPS 的状态将保存在全局变量$_SERVER['HTTPS']中。因此，使用 isset()函数中的$_SERVER['HTTPS']来检查它是否存在。这也将告诉我们 HTTPS 是否启用。检查$_SERVER['HTTPS']的值，如果它是“开”，那么 HTTPS 是启用的，我们必须在网址上附加“HTTPS”。

**方法:**获取当前运行页面的完整网址有以下几个步骤:

*   创建一个 PHP 变量，以字符串格式存储网址。
*   检查服务器是否启用了 HTTPS。如果是，请在网址字符串中添加“https”。如果未启用 HTTPS，请将“http”附加到 URL 字符串中。
*   将常规符号，即“://”附加到网址上。
*   附加服务器的名称。
*   将 REQUEST_URI(我们已经请求的资源，例如/index.php 等)附加到 URL 字符串中。

**注意:**使用 isset()功能检查 HTTPS 是否启用。isset()函数用于检查变量是否存在。
**示例 1:** 此示例说明获取当前页面的 url。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
    // Program to display URL of current page.
    if (isset($_SERVER['HTTPS']) && $_SERVER['HTTPS'] === 'on')
        $link = "https";
    else $link = "http";

    // Here append the common URL characters.
    $link .= "://";

    // Append the host(domain name, ip) to the URL.
    $link .= $_SERVER['HTTP_HOST'];

    // Append the requested resource location to the URL
    $link .= $_SERVER['REQUEST_URI'];

    // Print the link
    echo $link;
?>
```

**输出:**

```php
https://ide.geeksforgeeks.org/
```

**示例 2:** 使用$_SERVER['HTTP_HOST']获取网页的 url，该 URL 将从当前请求返回主机头。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
    // Program to display current page URL.
    $link = (isset($_SERVER['HTTPS']) && $_SERVER['HTTPS'] 
                === 'on' ? "https" : "http") . 
                "://" . $_SERVER['HTTP_HOST'] . 
                $_SERVER['REQUEST_URI'];
    echo $link;
?>
```

**输出:**

```php
https://ide.geeksforgeeks.org/
```

上面代码的输出是 https://ide.geeksforgeeks.org/而不是 https://ide.geeksforgeeks.org/index.php.为了修复这个问题，需要将，$_SERVER['REQUEST_URI']替换为$_SERVER['PHP_SELF']。

**程序 3:** 这个例子显示的是当前正在执行的 PHP 文件的 URL。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

  // Program to display complete URL
  if (isset($_SERVER['HTTPS']) && $_SERVER['HTTPS'] === 'on') 
      $link = "https";
  else $link = "http";

  // Here append the common URL
  // characters.
  $link .= "://";

  // Append the host(domain name,
  // ip) to the URL.
  $link .= $_SERVER['HTTP_HOST'];

  // Append the requested resource
  // location to the URL
  $link .= $_SERVER['PHP_SELF'];

  // Display the link
  echo $link;
?>
```

**输出:**

```php
https://ide.geeksforgeeks.org/index.php
```

**程序 4:** 这个例子描述了获取网页的完整 url。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

  // Program to display complete URL
  $link = (isset($_SERVER['HTTPS']) && $_SERVER['HTTPS']
              === 'on' ? "https" : "http") . "://" . 
              $_SERVER['HTTP_HOST'] . $_SERVER['PHP_SELF'];

  // Display the complete URL
  echo $link;
?>
```

**输出:**

```php
https://ide.geeksforgeeks.org/index.php
```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。