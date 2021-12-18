# PHP get_Browser()函数

> Original: [https://www.geeksforgeeks.org/php-get_browser-function/](https://www.geeksforgeeks.org/php-get_browser-function/)

在本文中，我们将了解如何使用 PHP 中的 get_Browser()函数检查用户的浏览器功能，并通过示例了解其实现。 PHP 中的 get_Browser()函数是一个内置函数，用于告诉用户浏览器的功能。 此函数查找用户的 Browscape.ini 文件，并返回用户浏览器的功能。 User_agent 和 return_array 作为参数传递给 get_Browser()函数，如果成功，它将返回一个对象或数组，其中包含有关用户浏览器的信息；如果失败，则返回 False。

**语法：**

```php
get_browser(user_agent, return_array)
```

**使用的参数：**PHP 中的 get_Browser()函数接受两个参数：

*   **user_agent** : this is an optional parameter that specifies the name of the HTTP user agent. The default value is the value of $HTTP_USER_AGENT.
*   **RETURN_ARRAY** : this is an optional parameter that, if set to True, returns an array instead of an object.

**返回值：**成功时返回包含用户浏览器信息的对象或数组，失败时返回 False。

**例外**：

*   可以使用空值绕过 USER_AGENT 参数。
*   Cookie 值仅仅表示浏览器本身能够接受 Cookie，而不意味着用户是否允许浏览器接受 Cookie。
*   要使此功能起作用，php.ini 中的 Browscap 配置设置必须指向系统上 Browscape.ini 文件的正确位置。

**方法：**为了检查相应地确认它们的用户系统的浏览器功能&，我们将使用包含两个参数的参数：user_agent，它将用于指定 HTTP 用户代理的名称；&第二个参数是 return_array，如果值设置为 true，它将返回一个数组而不是一个对象。

**示例 1：**下面的示例说明了将显示用户浏览器功能的 get_Browser()函数。

## PHP

```php
<?php
  echo $_SERVER['HTTP_USER_AGENT'];

  // Using get_browser() to display
  // capabilities of the user browser
  $mybrowser = get_browser();
  print_r($mybrowser);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**下面的示例说明了返回数组设置为 true 时的 get_Browser()函数。

## PHP

```php
<?php
    echo $_SERVER['HTTP_USER_AGENT'];

    // Using get_browser() with return_array set to TRUE
    $mybrowser = get_browser(null, true);
    print_r($mybrowser);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.get-browser.php](http://php.net/manual/en/function.get-browser.php)