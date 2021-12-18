# PHP|gethostname()函数

> Original: [https://www.geeksforgeeks.org/php-gethostname-function/](https://www.geeksforgeeks.org/php-gethostname-function/)

**gethostname()函数**是 PHP 中的一个内置函数，它返回本地计算机的主机或域名。 此函数适用于 PHP 5.3.0 之后的版本，此前还有另一个函数名为**php_uname**函数。

**语法：**

```php
*string* gethostname( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回主机或域名，失败时返回 False。

**注意：**此函数适用于 PHP 5.3.0 及更高版本。

下面的程序演示了 PHP 中的**gethostname()函数**：

**程序：**

```php
<?php

// Use gethostname() function to
// get the host name
echo gethostname();

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.gethostname.php](https://www.php.net/manual/en/function.gethostname.php)