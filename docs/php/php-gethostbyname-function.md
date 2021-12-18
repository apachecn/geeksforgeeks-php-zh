# PHP|gethostbyname()函数

> Original: [https://www.geeksforgeeks.org/php-gethostbyname-function/](https://www.geeksforgeeks.org/php-gethostbyname-function/)

**gethostbyname()函数**是 PHP 中的一个内置函数，它返回指定主机/域名的 IPv4 地址。

**语法：**

```
*string* gethostbyname( *$hostname* )
```

**参数：**此函数接受必需的单个参数**$hostname**。 它指定要查找其 IPv4 地址的主机名。

**返回值：**此函数成功时返回 IPv4 地址，失败时返回包含未修改主机名的字符串。

**注意：**此函数适用于 PHP 4.0.0 及更新版本。

下面的程序演示了 PHP 中的 gethostbyname()函数：

**程序：**

```
<?php

$ip = gethostbyname("geeksforgeeks.org");

echo $ip;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.gethostbyname.php](https://www.php.net/manual/en/function.gethostbyname.php)