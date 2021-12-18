# PHP 中最好的输入消毒函数有哪些？

> 原文:[https://www . geeksforgeeks . org/什么是 php 中的最佳输入消毒功能/](https://www.geeksforgeeks.org/what-are-the-best-input-sanitizing-functions-in-php/)

**对数据进行消毒**意味着从数据中删除任何非法字符。净化用户输入是 web 应用程序中最常见的任务之一。
为了使这项任务更容易，PHP 提供了本机过滤器扩展，您可以使用它来净化数据，如电子邮件地址、网址、IP 地址等。
**PHP 过滤器扩展:** PHP 过滤器用于净化和验证外部输入。PHP 过滤器扩展具有许多检查用户输入所需的功能，旨在更容易、更快地进行数据清理。当使用示例中的标志时，该函数确保代码删除除字母、数字和以下字符之外的所有字符！#$% & '*+-=？_`{|}~@.[] .
**使用 Filters 的优势:**很多 web 应用接收外部输入。外部输入/数据可以是:

*   表单中的用户输入
*   饼干
*   Web 服务数据
*   服务器变量
*   数据库查询结果

**对字符串进行消毒:**以下示例使用 **filter_var()** 函数删除字符串中的所有 HTML 标记。
**程序**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

//Use of filter_var()
$str = "<h1>GeeksforGeeks</h1>";

$newstr = filter_var($str,
    FILTER_SANITIZE_STRING);

echo $newstr;
?>
```

**Output:** 

```
GeeksforGeeks

```

**对电子邮件地址进行消毒:**以下示例使用 **filter_var()** 函数从$email 变量中移除所有非法字符。
**程序:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

$email = "geeksforgeeks@gmail.co<m>";

// Remove all illegal characters
// from email
$nemail = filter_var($email,
        FILTER_SANITIZE_EMAIL);

echo $nemail;
?>
```

**Output:** 

```
geeksforgeeks@gmail.com

```

**对 URL 进行消毒:**以下示例使用 **filter_var()** 函数删除 URL 中的所有非法字符:
**程序:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

$url = "www.geeksforgeeks.or°g";

// Remove all illegal characters
// from a url
$nurl = filter_var($url,
        FILTER_SANITIZE_URL);

echo $nurl;
?>
```

**Output:** 

```
www.geeksforgeeks.org

```