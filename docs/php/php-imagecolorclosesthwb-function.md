# PHP|imagecolorclosesthwb()函数

> Original: [https://www.geeksforgeeks.org/php-imagecolorclosesthwb-function/](https://www.geeksforgeeks.org/php-imagecolorclosesthwb-function/)

**imagecolorclosesthwb()**函数是 PHP 中的一个内置函数，用于获取给定图像的色调、白色和黑色的索引。 此函数返回一个整数值，其中包含与给定颜色最接近的色调、白色和黑色的颜色索引。

**语法：**

```php
*int* imagecolorclosesthwb ( $image, $red, $green, $blue )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$image:** it is returned by one of the image creation functions, such as imagecreatetruecolor (). It is used to create the size of the image.
*   **$red:** this parameter is used to set the value of the red component.
*   **$green:** this parameter is used to set the value of the green component.
*   **$BLUE:** this parameter is used to set the value of the blue component.

**返回值：**此函数返回一个整数值，其颜色色调、白色和黑色的索引最接近图像中的给定颜色。

下面的程序演示了 PHP 中的**imagecolorclosesthwb()**函数。

**程序 1：**

```php
<?php

// Create new image from given URL
$image = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');

// Display the index of color
echo 'Hue White and Blackness closest color index: ' 
    . imagecolorclosesthwb($image, 5, 165, 10);

imagedestroy($image);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new image from given URL
$image = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');

// Array contains rgb color value
$color = array(
    array(7, 150, 0),
    array(53, 190, 255),
    array(255, 165, 54)
);

// Loop to find closest HWB color
foreach($color as $id => $rgb)
{
    echo 'Hue White and Blackness closest color index: '
    . imagecolorclosesthwb($image, $rgb[0], $rgb[1], $rgb[2]) . "<br>";
}

imagedestroy($image);
?>
```

发帖主题：Re：Колибри0.7.8.0

**相关文章：**

*   [php|Imagearc()函数](https://www.geeksforgeeks.org/php-imagearc-function/)
*   [php|Imagesy()函数](https://www.geeksforgeeks.org/php-imagesy-function/)
*   [PHP|ImageEllse()11-13](https://www.geeksforgeeks.org/php-imageellipse-function/)

**引用：**[http://php.net/manual/en/function.imagecolorclosesthwb.php](http://php.net/manual/en/function.imagecolorclosesthwb.php)