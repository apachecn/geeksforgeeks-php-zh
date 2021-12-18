# PHP|gethostbyaddr()函数

> Original: [https://www.geeksforgeeks.org/php-gethostbyaddr-function/](https://www.geeksforgeeks.org/php-gethostbyaddr-function/)

**gethostbyaddr()函数**是 PHP 中的一个内置函数，它返回指定 IP 地址的域名。

**语法：**

```php
gethostbyaddr($ip_address);
```

**参数：**此函数接受一个参数，如上所述，如下所述：

*   **$IP_ADDRESS** : required parameter. It specifies the IP address whose hostname is to be found. Passed as a string.

**返回值：**

*   This function returns the hostname on success and the IP address on failure.

**注：**

*   此函数适用于 PHP 4.0.0 及更新版本。

**示例**

```php
<?php
$host = gethostbyaddr("52.25.109.230");
echo $host;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.gethostbyaddr.php](https://www.php.net/manual/en/function.gethostbyaddr.php)