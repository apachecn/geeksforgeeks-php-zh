# 用 PHP 去掉一个饼干

> 原文:[https://www.geeksforgeeks.org/remove-a-cookie-using-php/](https://www.geeksforgeeks.org/remove-a-cookie-using-php/)

**Cookie:**Cookie 是服务器为了给用户保存状态信息而发送的小文件。它存储在客户端计算机上，并在用户每次请求同一页面时发送到服务器。

要创建 cookie，您可以使用 PHP 的 **setcookie()** 功能来设置 cookie。

**语法:**

```php
setcookie(name, value, expire, path, domain, secure, httponly)
```

**参数:**该功能接受 7 个参数，如上所述，描述如下:

*   **名称:**饼干的名称。
*   **值:**要存储在 cookie 中的值。
*   **expire-time:** 是浏览器将 cookie 保存在用户机器上之前的秒数。之后会自动删除。如果未设置，浏览器将保留该 cookie，直到它被打开。
*   **路径:**它确定 cookie 对哪些目录有效。如果你想在所有目录中访问它，那么把它放在"/"上，也就是说，cookie 在整个域中都是可访问的。否则，cookie 将被限制在子目录中。
*   **域:**用于定义 cookie 的访问层次。例如，如果您将此设置为“yourdomain.com”，它也可以通过所有子域访问。但是如果设置为“sub.yourdomain.com”，它将可以被“sub.yourdomain.com”及其子域访问。
*   **安全:**它决定如何通过 HTTP 或 HTTPS 发送 cookie。如果设置为真，那么 cookie 将只通过 HTTPS 发送，否则，它将通过 HTTP 发送。其默认值为**假**。
*   **httponly:** 如果设置为 true，则只能通过 HTTP 或 HTTPS 访问 cookie。这意味着客户端代码(比如 Javascript)不能访问 cookie。

在以上参数中，只有**前两个**参数是强制的。其他是可选参数。如果你想保存饼干，那么提供*过期时间*参数。

**注意:**存储在名为 **$_COOKIE** 的全局数组中。

**创建 Cookie:** 如前所述，我们可以使用 **setcookie()** 功能设置 Cookie。

*   **示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<!DOCTYPE html>

<?php
$cookie_name = "gfg";
$cookie_value = "GeeksforGeeks";

// 86400 = 1 day
setcookie($cookie_name, $cookie_value, time() + (86400 * 15), "/"); 
?>

<html>
<body>
    <?php
    if(!isset($_COOKIE[$cookie_name])) {
          echo "Cookie named '" . $cookie_name . "' is not set!";
    } 
    else {
          echo "Cookie '" . $cookie_name . "' is set!<br>";
          echo "Value is: " . $_COOKIE[$cookie_name];
    }
    ?>

</body>

</html>
```

*   **输出:**

```php
Cookie 'gfg' is set!
Value is: GeeksforGeeks
```

**删除 Cookie:**PHP 中没有专门提供删除 Cookie 的功能。我们所要做的就是通过使用 **setcookie()** 功能将其设置为过去的时间来更新 cookie 的**过期时间**值。一个非常简单的方法是从当前时间中扣除几秒钟。

*   **语法:**

```php
setcookie(name, time() - 3600);
```

*   **示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<!DOCTYPE html>
<?php

// Set the expiration date to one hour ago
setcookie("gfg", "", time() - 3600);
?>

<html>

<body>

    <?php
    echo "Cookie 'gfg' is deleted.";
    ?>

</body>

</html>
```

*   **输出:**

```php
Cookie 'gfg' is deleted.
```

**注意:**setcookie()函数必须出现在< html >标签之前。

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。