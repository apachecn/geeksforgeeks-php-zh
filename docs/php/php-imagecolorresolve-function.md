# PHP|ImagecolorResolve()函数

> Original: [https://www.geeksforgeeks.org/php-imagecolorresolve-function/](https://www.geeksforgeeks.org/php-imagecolorresolve-function/)

**imagecolorResolve()**函数是 PHP 中的一个内置函数，用于获取指定颜色或其最接近的替代颜色的索引。 此函数返回请求颜色的颜色索引值，可以是完全匹配的颜色，也可以是最接近的备选颜色。

**语法：**

```php
*int* imagecolorresolve ( $image, $red, $green, $blue )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$image:** it is returned by one of the image creation functions, such as imagecreatetruecolor (). It is used to create the size of the image.
*   **$red:** this parameter is used to set the value of the red component.
*   **$green:** this parameter is used to set the value of the green component.
*   **$BLUE:** this parameter is used to set the value of the blue component.

**返回值：**此函数返回颜色索引。

下面的程序说明了 PHP 中的**imagecolorResolve()**函数：

**程序 1：**

```php
<?php

// Load an image
$image = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');

// Get closest colors from the image
$colors = array();
$colors[] = imagecolorresolve($image, 167, 75, 55);
$colors[] = imagecolorresolve($image, 150, 25, 250);
$colors[] = imagecolorresolve($image, 161, 234, 135);
$colors[] = imagecolorresolve($image, 143, 255, 254);

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
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/col1.png');

// Get closest colors from the image
$colors = array(
    imagecolorresolve($image, 156, 0, 255),
    imagecolorresolve($image, 0, 255, 200),
    imagecolorresolve($image, 16, 134, 35),
    imagecolorresolve($image, 143, 255, 254)
);

// Output
print_r($colors);

imagedestroy($image);
?>
```

发帖主题：Re：Колибри0.7.8.0

**相关文章：**

*   __T0__PHP|imagecolor()_
*   [php|Imagearc()函数](https://www.geeksforgeeks.org/php-imagearc-function/)

**引用：**[http://php.net/manual/en/function.imagecolorresolve.php](http://php.net/manual/en/function.imagecolorresolve.php)