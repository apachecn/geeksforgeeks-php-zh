# PHP|Gmagick getimageHeight()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimageheight-function/](https://www.geeksforgeeks.org/php-gmagick-getimageheight-function/)

**Gmagick：：getimageHeight()函数**是 PHP 中的一个内置函数，用于获取图像高度，即图像的垂直长度。

**语法：**

```php
*int* Gmagick::getimageheight( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含图像高度的整数值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimageHeight()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the image height
$height = $gmagick->getimageheight();
echo $height;
?>
```

发帖主题：Re：Колибри0.7.0

```php
184
```

**程序 2：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the image height
$gmagick->scaleimage(200, 200);

// Get the image height
$height = $gmagick->getimageheight();
echo $height;
?>
```

发帖主题：Re：Колибри0.7.0

```php
200
```

**引用：**[https://www.php.net/manual/en/gmagick.getimageheight.php](https://www.php.net/manual/en/gmagick.getimageheight.php)