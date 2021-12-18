# PHP|imagecolorResolution vealpha()函数

> Original: [https://www.geeksforgeeks.org/php-imagecolorresolvealpha-function/](https://www.geeksforgeeks.org/php-imagecolorresolvealpha-function/)

**imagecolorResolution vealpha()**函数是 PHP 中的一个内置函数，用于获取指定颜色和 Alpha 值或其最接近的备用值的索引。 此函数返回所请求颜色的索引，可以是确切的颜色，也可以是最接近的替代颜色。

**语法：**

```php
*int* imagecolorresolvealpha ( $image, $red, $green, $blue, $alpha )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$image:** it is returned by one of the image creation functions, such as imagecreatetruecolor (). It is used to create the size of the image.
*   **$red:** this parameter is used to set the value of the red component.
*   **$green:** this parameter is used to set the value of the green component.
*   **$BLUE:** this parameter is used to set the value of the blue component.
*   **$alpha:** this parameter is used to set the transparency of the image. The value of $alpha is between 0 and 127, where 0 is completely opaque and 127 is completely transparent.

**返回值：**此函数返回颜色的索引值。

下面的程序演示了 PHP 中的**imagecolorResolution vealpha()**函数：

**程序 1：**

```php
<?php

// Load an image
$image = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');

// Get closest colors from the image
$colors = array();
$colors[] = imagecolorresolvealpha($image, 156, 0, 255, 0);
$colors[] = imagecolorresolvealpha($image, 0, 255, 200, 50);
$colors[] = imagecolorresolvealpha($image, 16, 134, 35, 70);
$colors[] = imagecolorresolvealpha($image, 143, 255, 254, 100);

// Output
print_r($colors);

imagedestroy($image);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Load an image
$image = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');

// Get closest colors from the image
$colors = array(
    imagecolorresolvealpha($image, 156, 0, 255, 0),
    imagecolorresolvealpha($image, 0, 255, 200, 50),
    imagecolorresolvealpha($image, 16, 134, 35, 70),
    imagecolorresolvealpha($image, 143, 255, 254, 100)
);

// Output
print_r($colors);

imagedestroy($image);
?>
```

发帖主题：Re：Колибри0.7.8.0

**相关文章：**

*   [php|imagecolorclosestatpha()函数](https://www.geeksforgeeks.org/php-imagecolorclosestalpha-function/)
*   [php|imagecolorest()函数](https://www.geeksforgeeks.org/php-imagecolorclosest-function/)

**引用：**[http://php.net/manual/en/function.imagecolorresolvealpha.php](http://php.net/manual/en/function.imagecolorresolvealpha.php)