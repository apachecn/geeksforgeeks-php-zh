# PHP|Imagick getFormat()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getformat-function/](https://www.geeksforgeeks.org/php-imagick-getformat-function/)

**Imagick：：getFormat()函数**是 PHP 中的一个内置函数，用于获取 Imagick 对象的格式。

**语法：**

```php
*string* Imagick::getFormat( *void* )
```

**参数：**此函数不接受任何参数。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**此函数在成功时返回字符串值。

下面的程序演示了 PHP 中的**Imagick：：getFormat()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Get the Format
$format = $imagick->getFormat();

echo $format;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Format
$imagick->setFormat('png');

// Get the Format
$format = $imagick->getFormat();

echo $format;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getformat.php](https://www.php.net/manual/en/imagick.getformat.php)