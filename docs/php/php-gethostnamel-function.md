# PHP|gethostnamel()函数

> Original: [https://www.geeksforgeeks.org/php-gethostnamel-function/](https://www.geeksforgeeks.org/php-gethostnamel-function/)

函数**gethostbynamel()**是 PHP 中内置函数，它返回指定 Internet 主机/域名的 IPv4 地址列表。

**语法：**

```
gethostbynamel( *string* $hostname )
```

**参数：**此函数接受必需的单个参数**$hostname**。 它指定要查找其 IPv4 地址列表的主机名。

**返回值：**此函数成功时返回指定主机/域名的 IPv4 地址列表，失败时返回 False。

**注意：**此函数适用于 PHP 4.0.0 及更新版本。

下面的程序演示了 PHP 中的 gethostbynamel()函数：

**程序：**

```
<?php
$hostlist = gethostbynamel("geeksforgeeks.org");
print_r($hostlist);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.gethostbynamel.php](https://www.php.net/manual/en/function.gethostbynamel.php)