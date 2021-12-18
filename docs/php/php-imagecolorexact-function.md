# PHP|imagecolorexact()函数

> Original: [https://www.geeksforgeeks.org/php-imagecolorexact-function/](https://www.geeksforgeeks.org/php-imagecolorexact-function/)

**imagecolorexact()**函数是 PHP 中的一个内置函数，用于获取图像调色板中指定颜色的索引。 在创建的图像文件中，仅解析图像中使用的颜色。 仅存在于调色板中的颜色不会被解析。

**语法：**

```php
*int* imagecolorexact ( $image, $red, $green, $blue )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$image:** it is returned by one of the image creation functions, such as imagecreatetruecolor (). It is used to create the size of the image.
*   **$red:** this parameter is used to set the value of the red component.
*   **$green:** this parameter is used to set the value of the green component.
*   **$BLUE:** this parameter is used to set the value of the blue component.

**返回值：**如果成功，此函数将返回调色板中指定颜色的索引，如果该颜色不存在，则返回-1。

下面的程序演示了 PHP 中的**imagecolorexact()**函数。

**程序 1：**

```php
<?php

// Set the image into variable
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/imagecolor1.png');

// Create an array containing colors and image
$colors = Array();
$colors[] = imagecolorexact($image, 10, 15, 20);
$colors[] = imagecolorexact($image, 30, 180, 70);
$colors[] = imagecolorexact($image, 12, 55, 25);
$colors[] = imagecolorexact($image, 154, 25, 52);

print_r($colors);

// Free from memory
imagedestroy($image);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Set the image into variable
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/imagecolor1.png');

// Create an array containing colors and image
$colors   = Array(
    $colors[] = imagecolorexact($image, 0, 153, 0),
    $colors[] = imagecolorexact($image, 0, 0, 0),
    $colors[] = imagecolorexact($image, 255, 255, 255),
    $colors[] = imagecolorexact($image, 100, 100, 52)
);

print_r($colors);

// Free from memory
imagedestroy($image);

?>
```

发帖主题：Re：Колибри0.7.8.0

**相关文章：**

*   [php|Imagearc()函数](https://www.geeksforgeeks.org/php-imagearc-function/)
*   [php|imagefilledellipse()函数](https://www.geeksforgeeks.org/php-imagefilledellipse-function/)
*   [PHP|ImageEllse()11-13](https://www.geeksforgeeks.org/php-imageellipse-function/)

**引用：**[http://php.net/manual/en/function.imagecolorexact.php](http://php.net/manual/en/function.imagecolorexact.php)