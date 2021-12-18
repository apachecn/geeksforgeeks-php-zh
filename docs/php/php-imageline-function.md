# PHP|Imageline()函数

> Original: [https://www.geeksforgeeks.org/php-imageline-function/](https://www.geeksforgeeks.org/php-imageline-function/)

**imageline()函数**是 PHP 中的一个内置函数，用于设置在两个给定点之间绘制一条线。

**语法：**

```php
*bool* imageline( *resource* $image, *int* $x1, *int* $y1, 
*int* $x2, *int* $y2, *int* $color )
```

**参数：**此函数接受上述 6 个参数，如下所述：

*   **$image：**它指定要处理的图像资源。
*   **$x1：**它指定起始 x 坐标。
*   **$y1：**它指定起始 y 坐标。
*   **$x2：**它指定结束的 x 坐标。
*   **$y2：**它指定结束的 y 坐标。
*   **$color：**它指定线条颜色。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**imageline()函数**：

**示例 1：**在此示例中，向图像添加一行。

```php
<?php

// Create an image instance
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Prepare the line color
$text_color = imagecolorallocate($im, 255, 0, 0);

// Add a line
imageline($im, 40, 100, 640, 100, $text_color);

// Output the image
header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/d060079a6bf058fa2b0afa561349ba60.png)

**示例 2：**在本例中，我们将向图形中添加一条线。

```php
<?php

// Create an image instance
$im = imagecreate(700, 200);

// Initialize the colors
$yellow = imagecolorallocate($im, 255, 255, 0);
$blue = imagecolorallocate($im, 0, 0, 255);

// Add a yellow background
imageline($im, 0, 0, 700, 200, $yellow);

// Add a blue line
imageline($im, 0, 0, 840, 250, $blue);

// Output the image
header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/9617de0b0717bfb86c8bb196e358c656.png)

**引用：**[https://www.php.net/manual/en/function.imageline.php](https://www.php.net/manual/en/function.imageline.php)