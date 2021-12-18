# PHP|Imagick getImageInterlaceScheme()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageinterlacescheme-function/](https://www.geeksforgeeks.org/php-imagick-getimageinterlacescheme-function/)

**Imagick：：getImageInterlaceScheme()函数**是 PHP 中的一个内置函数，用于获取图像隔行扫描方案。

**语法：**

```php
*int* Imagick::getImageInterlaceScheme( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个整数值，其中包含与[隔行扫描常数](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.interlace-undefined)之一相对应的隔行扫描方案。

隔行扫描常量列表如下：

*   Imagick：：Interlace_ 未定义(0)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   Imagick：：Interlace_Plane(3)
*   Imagick：：Interlace_Partition(4)
*   Imagick：：Interlace_GIF(5)
*   Imagick：：Interlace_JPEG(6)
*   Imagick：：interlace_png(7)

**异常：**此函数在出错时引发 ImagickException。

下面给定的程序说明了 PHP：
**程序 1：**中的**Imagick：：getImageInterlaceScheme()函数**

```php
<?php
// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Interlace Scheme
$interlaceScheme = $imagick->getImageInterlaceScheme();
echo $interlaceScheme;
?>
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**程序 2：**

```php
<?php
// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Interlace Scheme
$imagick->setImageInterlaceScheme(imagick::INTERLACE_PNG);

// Get the Interlace Scheme
$interlaceScheme = $imagick->getImageInterlaceScheme();
echo $interlaceScheme;
?>
```

发帖主题：Re：Колибри0.7.0

```php
7
```

**引用：**[https://www.php.net/manual/en/imagick.getimageinterlacescheme.php](https://www.php.net/manual/en/imagick.getimageinterlacescheme.php)