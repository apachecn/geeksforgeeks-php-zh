# PHP|Imagick getImageTotalInkDensity()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagetotalinkdensity-function/](https://www.geeksforgeeks.org/php-imagick-getimagetotalinkdensity-function/)

**Imagick：：getImageTotalInkDensity()函数**是 PHP 中的一个内置函数，用于获取图像的总墨水密度。

**语法：**

```php
*float* Imagick::getImageTotalInkDensity( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含图像总油墨密度的浮点值。

**异常：**此函数在出错时引发 ImagickException。

以下程序说明了 PHP 中的**Imagick：：getImageTotalInkDensity()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the Image total ink density
$inkDensity = $imagick->getImageTotalInkDensity();
echo $inkDensity;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20191121183021/setprofile.png');

// Get the Image total ink density
$inkDensity = $imagick->getImageTotalInkDensity();
echo $inkDensity;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagetotalinkdensity.php](https://www.php.net/manual/en/imagick.getimagetotalinkdensity.php)