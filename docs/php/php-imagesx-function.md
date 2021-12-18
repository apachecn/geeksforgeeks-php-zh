# PHP|imagesx()函数

> Original: [https://www.geeksforgeeks.org/php-imagesx-function/](https://www.geeksforgeeks.org/php-imagesx-function/)

**imagesx()**函数是 PHP 中的内置函数，用于返回给定图像的宽度。

**语法：**

```
*int* imagesx( $image )
```

**参数：**此函数接受单个参数*$image*，这是必需的。 此*$image*变量可以存储由 imagecreatetruecolor()图像创建函数创建的图像。

**返回值：**此函数返回图像的宽度，如果出错则返回 False。

下面的程序演示了 PHP 中的**imagesx()**函数。

**程序 1：**

```
<?php

// store the image in variable.
$image = imagecreatefrompng("gfg.png");

// Display the width of image.
echo imagesx($image);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create the size of image or blank image.
$image = imagecreatetruecolor(500, 300);

// Display the width of image.
echo imagesx($image);

?>
```

发帖主题：Re：Колибри0.7.8.0

**相关文章：**

*   [php|Imagedashedline()函数](https://www.geeksforgeeks.org/php-imagedashedline-function/)
*   [php|imagecolorat()函数](https://www.geeksforgeeks.org/php-imagecolorat-function/)
*   [PHP|ImagePolygon()11-13](https://www.geeksforgeeks.org/php-imagepolygon-function/)

**引用：**[http://php.net/manual/en/function.imagesx.php](http://php.net/manual/en/function.imagesx.php)