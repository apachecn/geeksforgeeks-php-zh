# PHP|imagefill()函数

> Original: [https://www.geeksforgeeks.org/php-imagefill-function/](https://www.geeksforgeeks.org/php-imagefill-function/)

**imagefill()**函数是 PHP 中的一个内置函数，用于用给定的颜色填充图像。 此函数使用图像中的给定颜色从给定坐标(左上角为 0，0)开始执行泛洪填充。

**语法：**

```php
*bool* imagefill( $image, $x, $y, $color )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$image：**它由图像创建函数之一返回，如 imagecreatetruecolor()。 它用于创建图像的大小。
*   **$x：**该参数用于设置起始点的 x 坐标。
*   **$y：**该参数用于设置起始点的 y 坐标。
*   **$color：**它设置图像的颜色。 由 imagecolorallocation()函数创建的颜色标识符。

**返回值：**此函数成功时返回 True，失败时返回 False。

以下程序说明了 PHP 中的**imagefill()**函数：

**程序 1：**

```php
<?php

// Create an image of given size
$image = imagecreatetruecolor(500, 400);

// Sets background to green
$green = imagecolorallocate($image, 0, 153, 0);
imagefill($image, 0, 0, $green);

header('Content-type: image/png');
imagepng($image);
imagedestroy($image);
?>
```

**输出：**
![image filled](img/9bea171f3cea381c9bb0a3a8fbea9480.png)

**程序 2：**

```php
<?php

// It create the size of image or blank image.
$image = imagecreatetruecolor(500, 300);

// Set the background color of image.
$bg = imagecolorallocate($image, 205, 220, 200);

// Fill background with above selected color.
imagefill($image, 0, 0, $bg);

// Set the color of an ellipse.
$col_ellipse = imagecolorallocate($image, 0, 102, 0);

// Function to draw the filled ellipse.
imagefilledellipse($image, 250, 150, 400, 250, $col_ellipse);

// Output of the image.
header("Content-type: image/png");
imagepng($image);

?>
```

**输出：**
![image filled](img/b3659baee9f7f8b2226da81092f9bf5e.png)

**相关文章：**

*   [PHP|imagecolorallocatealpha()函数](https://www.geeksforgeeks.org/php-imagecolorallocatealpha-function/)
*   [PHP|imagearc()函数](https://www.geeksforgeeks.org/php-imagearc-function/)
*   [PHP|ImageEllse()函数](https://www.geeksforgeeks.org/php-imageellipse-function/)

**引用：**[http://php.net/manual/en/function.imagefill.php](http://php.net/manual/en/function.imagefill.php)