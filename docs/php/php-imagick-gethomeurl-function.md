# PHP|Imagick getHomeURL()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-gethomeurl-function/](https://www.geeksforgeeks.org/php-imagick-gethomeurl-function/)

**Imagick：：getHomeURL()函数**是 PHP 中的一个内置函数，用于获取 ImageMagick 主页 URL。

**语法：**

```php
*string* Imagick::getHomeURL( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数在成功时返回字符串值。

下面的程序演示了 PHP 中的**Imagick：：getHomeURL()函数**：

**程序：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Get the URL
$url = $imagick->getHomeURL();

echo $url;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.gethomeurl.php](https://www.php.net/manual/en/imagick.gethomeurl.php)