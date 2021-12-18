# PHP|Gmagick getimagewidth()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagewidth-function/](https://www.geeksforgeeks.org/php-gmagick-getimagewidth-function/)

**gmagick：：getimagewidth()函数**是 PHP 中的一个内置函数，用于获取图像宽度，即图像的水平长度。

**语法：**

```php
*int* Gmagick::getimagewidth( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含图像宽度的整数值。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimagewidth()函数**：

**程序 1：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the image width
$width = $gmagick->getimagewidth();
echo $width;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the image width
$gmagick->scaleimage(200, 200);

// Get the image width
$width = $gmagick->getimagewidth();
echo $width;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.getimagewidth.php](https://www.php.net/manual/en/gmagick.getimagewidth.php)