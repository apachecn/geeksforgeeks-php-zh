# PHP|Imagick PolaroidImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-polaroidimage-function/](https://www.geeksforgeeks.org/php-imagick-polaroidimage-function/)

**Imagick：：polaroidImage()**函数是 PHP 中的内置函数，用于模拟宝丽来照片。 此函数用于将带有宝丽来镜框的图像旋转给定的角度。

**注意：**仅当 Imagick 已针对版本 6.3.2 或更高版本编译时，此方法才可用。

**语法：**

```php
*bool* Imagick::polaroidImage( $properties, $angle )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$properties：**此参数保存宝丽来图像的属性。 如果不考虑属性更改，则可以将其设置为“ImagickDraw()”。
*   **$ANGLE：**此参数保存拍立得角度，整个图片(带边框)通过该角度旋转。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/741cf88db15a7f2cbf0510a2322631b2.png)

**程序：**

```php
<?php

// Create a new object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190708094104/g128-300x246.png');

// Use polaroidImage() function
$image->polaroidImage(new ImagickDraw(), 25);

// Image header
header('Content-type: image/png');

// Display resulting image
echo $image;

?>
```

**输出：**
![](img/25552c7b19a4f803502767371da6d09a.png)