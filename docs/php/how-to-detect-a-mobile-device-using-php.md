# 如何使用 PHP 检测移动设备？

> 原文:[https://www . geesforgeks . org/如何使用 php 检测移动设备/](https://www.geeksforgeeks.org/how-to-detect-a-mobile-device-using-php/)

我们经常发现检测用户的浏览器以提供更好的显示体验很重要。很少有网站是必须从电脑而不是手机访问的。此外，对于粗心的用户来说，这也是一种预防措施，他们可以从手机这样的小显示器上填写重要的表格。

**使用 HTTP_USER_AGENT:** 我们将检查访问者使用的是哪种浏览器。为此，我们检查浏览器作为 HTTP 请求的一部分发送的用户代理字符串。这些信息存储在一个变量中。在 PHP 中，变量总是以一个美元符号开始。

**语法:**

```php
$_SERVER['HTTP_USER_AGENT']
```

。

这里的 **$_SERVER** 是一个特殊的保留 PHP 变量，包含所有的 web 服务器信息。它被称为**超级全球**。这些特殊变量是在 PHP 4.1.0 中引入的。接下来，我们需要读取 HTTP_USER_AGENT 返回的消息，以将控制传递给下一组指令。出于演示目的，我们将使用 **echo""** 语句来确认检测到移动设备。我们将用 [**preg_match()函数**](https://www.geeksforgeeks.org/php-preg_match-function/) 读取 HTTP_USER_AGENT 返回的消息。它执行正则表达式匹配。

**示例:**很容易迷失在这一大块 regex 中，但就是这样从市场上可用的每个移动操作系统中检测各种浏览器(也可以检测 Kindle 设备)。比如**(安卓|bb\d+|meego)。+mobile|avantgo|bada** 将检查用户设备的操作系统是否为 **Android** 。如果将此片段插入网站的 index.php，并且从移动设备访问该网站，浏览器将显示消息为**检测到移动浏览器**。

```php
<?php
function isMobileDevice() {
    return preg_match("/(android|avantgo|blackberry|bolt|boost|cricket|docomo
|fone|hiptop|mini|mobi|palm|phone|pie|tablet|up\.browser|up\.link|webos|wos)/i"
, $_SERVER["HTTP_USER_AGENT"]);
}
if(isMobileDevice()){
    echo "Mobile Browser Detected";
}
else {
    echo "Mobile Browser Not Detected";
}
?>
```

**输出:**我们正在从笔记本电脑访问它。

```php
Mobile Browser Not Detected
```