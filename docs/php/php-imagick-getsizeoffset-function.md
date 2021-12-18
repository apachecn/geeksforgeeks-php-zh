# PHP|Imagick getSizeOffset()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getsizeoffset-function/](https://www.geeksforgeeks.org/php-imagick-getsizeoffset-function/)

**Imagick：：getSizeOffset()函数**是 PHP 中的一个内置函数，用于获取大小偏移量。

**语法：**

```php
*int* Imagick::getSizeOffset( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含大小偏移量的整数值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：getSizeOffset()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the size offset
$sizeOffset = $imagick->getSizeOffset();
echo $sizeOffset;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the size offset
$imagick->setSizeOffset(100, 200, 25);

// Get the size offset
$sizeOffset = $imagick->getSizeOffset();
echo $sizeOffset;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getsizeoffset.php](https://www.php.net/manual/en/imagick.getsizeoffset.php)