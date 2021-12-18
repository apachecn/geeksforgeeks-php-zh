# PHP|图像集笔刷()函数

> Original: [https://www.geeksforgeeks.org/php-imagesetbrush-function/](https://www.geeksforgeeks.org/php-imagesetbrush-function/)

函数**的作用是：**是 PHP 的内置函数，用于设置画线的笔刷图像。 线条绘制是使用*imageline()*或*imagepolygon()*等函数完成的。 可以使用*IMG_COLOR_BRASED*或*IMG_COLOR_STYLEDBRUSHED*绘制特殊颜色。

**语法：**

```
*bool* imagesetbrush( *resource* $image, *resource* $brush )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$image：**它指定要处理的图像资源。
*   **$brush：**它指定另一个图像资源作为笔刷。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序演示了 PHP 中的**imagesetbrush()函数**：

**程序 1：**

```
<?php
// Load the png image
$image1 = imagecreatefrompng(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Create a another image, 700x200 to be used as brush
$image2 = imagecreatetruecolor(700, 200);

// Fill the background
$pink = imagecolorallocate($image2, 255, 0, 255);
imagefilledrectangle($image2, 0, 0, 800, 299, $pink);

// Set the brush
imagesetbrush($image2, $image1);

// Draw line
imageline($image2, 350, 100, 50, 6, IMG_COLOR_BRUSHED);

// Output image to the browser
header('Content-type: image/png');
imagepng($image2);
?>
```

**输出：**
![](img/45cbf417ff1d1cebd08ecc1689e5f4fd.png)

**程序 2：**

```
<?php
// Load the png image
$image = imagecreatefrompng(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Create a red color brush of size 3
$brush = imagecreatetruecolor(3, 3);
$brush_color = imagecolorallocate($brush, 255, 0, 0);
imagefill($brush, 0, 0, $brush_color);

// Set the brush
imagesetbrush($image, $brush);

// Draw line with brush
imageline($image, 150, 100, 500, 6, IMG_COLOR_BRUSHED);

// Output image to the browser
header('Content-type: image/png');
imagepng($image);
?>
```

**输出：**
![](img/463bb253a4b76a7459752219586c205b.png)

**引用：**[https://www.php.net/manual/en/function.imagesetbrush.php](https://www.php.net/manual/en/function.imagesetbrush.php)