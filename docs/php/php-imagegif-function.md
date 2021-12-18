# PHP|imagegif()函数

> Original: [https://www.geeksforgeeks.org/php-imagegif-function/](https://www.geeksforgeeks.org/php-imagegif-function/)

**imagegif()**函数是 PHP 中的一个内置函数，用于从给定的图像创建 GIF 图像文件。 如果图像已经通过 imagecolor 透明()函数转换为透明的，则将生成 GIF89a 图像格式，否则将生成 GIF87a 图像格式。
**语法：**

```
*bool* imagegif( $image, $to )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$image：**它由图像创建函数之一返回，如 imagecreatetruecolor()。 它用于创建图像的大小。
*   **$to：**此参数用于设置输入图像的路径。 如果没有设置或设置为 NULL，则会生成原始图像流。

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序演示了 PHP 中的**imagegif()**函数：

**程序 1：**

```
<?php
// Create a new image of given size
$image = imagecreatetruecolor(500, 300);

// Set background color
$bg = imagecolorallocate($image, 255, 255, 255);

// Set text color
$textcolor = imagecolorallocate($image, 0, 153, 0);

// Make the background white
imagefilledrectangle($image, 0, 0, 500, 300, $bg);

// Draw a text string on the image
imagestring($image, 6, 160, 140, 'GeeksforGeeks', $textcolor);

// Output the image to browser
header('Content-Type: image/gif');

// Create GIF image
imagegif($image);

imagedestroy($image);
?>
```

**输出：**
![imagegif](img/d33401fc93a95ede97ce6f1f2b0f129b.png)

**程序 2：**

```
<?php

// Load the PNG image file
$png = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Output the image to browser
header('Content-Type: image/gif');

// Convert PNG image to GIF image
imagegif($png);

imagedestroy($png);
?>
```

**输出：**
![imagegif](img/b2d17f207dbb1e365501d7444df1ee09.png)

**相关文章：**

*   [PHP|imagecolorexactalpha()函数](https://www.geeksforgeeks.org/php-imagecolorexactalpha-function/)
*   [PHP|imagecolorMatch()函数](https://www.geeksforgeeks.org/php-imagecolormatch-function/)
*   [PHP|imagecolorexact()函数](https://www.geeksforgeeks.org/php-imagecolorexact-function/)

**引用：**[http://php.net/manual/en/function.imagegif.php](http://php.net/manual/en/function.imagegif.php)