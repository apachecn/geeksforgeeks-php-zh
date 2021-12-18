# PHP|Imagick getCompression()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getcompression-function/](https://www.geeksforgeeks.org/php-imagick-getcompression-function/)

**Imagick：：getCompression()函数**是 PHP 中的一个内置函数，用于获取对象压缩类型。

**语法：**

```php
*int* Imagick::getCompression( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时此函数返回整数值。

下面的程序演示了 PHP 中的**Imagick：：getCompression()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Compression
$compression = $imagick->getCompression();
echo $compression;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Compression
$imagick->setCompression(5);

// Get the Compression
$compression = $imagick->getCompression();
echo $compression;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getcompression.php](https://www.php.net/manual/en/imagick.getcompression.php)