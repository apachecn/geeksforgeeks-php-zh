# PHP|imagecolorstotal()函数

> Original: [https://www.geeksforgeeks.org/php-imagecolorstotal-function/](https://www.geeksforgeeks.org/php-imagecolorstotal-function/)

**imagecolorstotal()**函数是 PHP 中的一个内置函数，用于查找图像调色板中的颜色数量。 此函数用于返回图像调色板中的颜色数量。

**语法：**

```
*int* imagecolorstotal ( $image )
```

**参数：**此函数接受单个参数*$image*，该参数是必需的。 函数的作用是：创建给定大小的图像。 此函数用于创建给定大小的空白图像。

**返回值：**此函数返回给定图像调色板中的颜色数，或者返回真彩色图像的 0。

以下程序说明了 PHP 中的**imagecolorstotal()**函数：

**程序 1：**

```
<?php

// store the image in variable.
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

echo 'Colors in image: ' . imagecolorstotal($image);

// Free image
imagedestroy($image);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// store the image in variable.
$image = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');

echo 'Colors in image: ' . imagecolorstotal($image);

// Free image
imagedestroy($image);
?>
```

发帖主题：Re：Колибри0.7.8.0

**相关文章：**

*   [php|imagecolorclosestatpha()函数](https://www.geeksforgeeks.org/php-imagecolorclosestalpha-function/)
*   [php|imagecolorat()函数](https://www.geeksforgeeks.org/php-imagecolorat-function/)
*   [php|imagecolorest()函数](https://www.geeksforgeeks.org/php-imagecolorclosest-function/)

**引用：**[http://php.net/manual/en/function.imagecolorstotal.php](http://php.net/manual/en/function.imagecolorstotal.php)