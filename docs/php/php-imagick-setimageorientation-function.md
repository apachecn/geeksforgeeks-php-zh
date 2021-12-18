# PHP|Imagick setImageOrientation()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageorientation-function/](https://www.geeksforgeeks.org/php-imagick-setimageorientation-function/)

**Imagick：：setImageOrientation()函数**是 PHP 中的内置函数，用于设置图像方向。 此函数实际上并不旋转图像，它只是更改 EXIF 旋转信息。

**语法：**

```php
*bool* Imagick::setImageOrientation( *int* $orientation )
```

**参数：**此函数接受单个参数**$Orientation**，该参数保存一个整数值，其中包含[方向常量](https://www.php.net/manual/en/imagick.constants.php#imagick.constants.orientation-undefined)之一。 我们还可以直接传递一个常量，如*setImageOrientation(imagick：：ORIENTATION_BOTTOMRIGHT)；*。

方向常数列表如下：

*   Imagick：：Orientation_Unfined(0)
*   Imagick：：Orientation_topleft(1)
*   Imagick：：Orientation_TOPRIGHT(2)
*   Imagick：：Orientation_Bottomright(3)
*   Imagick：：Orientation_BOTTOMLEFT(4)
*   Imagick：：Orientation_BOTTOMLEFT(4)
*   Imagick：：Orientation_RIGHTTOP(6)
*   Imagick：：Orientation_RIGHTBOTOM(7)
*   Imagick：：Orientation_LEFTBOTOM(8)

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**Imagick：：setImageOrientation()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Orientation
$imagick->setImageOrientation(imagick::ORIENTATION_LEFTTOP);

// Get the Orientation
$orientation = $imagick->getImageOrientation();
echo $orientation;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the Orientation
$imagick->setImageOrientation(imagick::ORIENTATION_RIGHTBOTTOM);

// Get the Orientation
$orientation = $imagick->getImageOrientation();
echo $orientation;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setimageorientation.php](https://www.php.net/manual/en/imagick.setimageorientation.php)