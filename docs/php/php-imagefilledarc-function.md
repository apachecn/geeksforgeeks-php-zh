# PHP|imagefilledarc()函数

> Original: [https://www.geeksforgeeks.org/php-imagefilledarc-function/](https://www.geeksforgeeks.org/php-imagefilledarc-function/)

**imagefilledarc()**函数是 PHP 中的一个内置函数，用于在给定图像中以指定坐标为中心绘制部分圆弧。 此函数成功时返回 True，失败时返回 False

**语法：**

```
*bool* imagefilledarc ( $image, $cx, $cy, $width, $height, $start, 
$end, $color, $style )
```

**参数：**此函数接受上述 9 个参数，如下所述：

*   **$image：**它由图像创建函数之一返回，如 imagecreatetruecolor()。 它用于创建图像的大小。
*   **$cx：**此参数用于设置中心的 x 坐标。
*   **$cy：**此参数用于设置中心的 y 坐标。
*   **$width：**该参数用于设置弧宽。
*   **$Height：**此参数用于设置弧高。
*   **$start：**圆弧起点角度，以度为单位。
*   **$end：**圆弧末端角度，以度为单位。 0°位于三点位置，圆弧是顺时针绘制的。
*   **$color：**使用 imagecolorallocation()创建的颜色标识符。
*   **$style：**建议如何填充图像，其值可以是下面列出的值中的任意一个。
    *   Img_ARC_PIE
    *   Img_ARC_Chord
    *   Img_ARC_NOFILL
    *   Img_ARC_EDGE

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序演示了 PHP 中的**imagefilledarc()**函数：

**程序 1：**

```
<?php

define("WIDTH", 300);
define("HEIGHT", 300);

// Create image.
$img = imagecreate(WIDTH, HEIGHT);

// Allocate colors.
$bg = $white = imagecolorallocate($img, 0xFF, 0xFF, 0xFF);
$green = imagecolorallocate($img, 0, 255, 0);

// make pie arc.
$center_x = (int)WIDTH/2;
$center_y = (int)HEIGHT/2;
imagerectangle($img, 0, 0, WIDTH-1, HEIGHT-1, $green);
imagefilledarc($img, $center_x, $center_y, WIDTH/2,
               HEIGHT/2, 0, 220, $green, IMG_ARC_PIE);

// Flush image.
header("Content-Type: image/png");
imagepng($img);
?>
```

**输出：**
![](img/674bba873989df6df488516ed3caac6a.png)

**程序 2：**

```
<?php

// Create image
$image = imagecreatetruecolor(100, 100);

// Allocate some colors
$red      = imagecolorallocate($image, 0xFF, 0x00, 0x00);
$darkred  = imagecolorallocate($image, 0x90, 0x00, 0x00);

// Make the 3D effect
for ($i = 60; $i > 50; $i--) {
   imagefilledarc($image, 50, $i, 100, 50, 75, 360, $darkred, IMG_ARC_PIE);
}
imagefilledarc($image, 50, 50, 100, 50, 75, 360, $red, IMG_ARC_PIE);

// flush image
header('Content-type: image/png');
imagepng($image);
imagedestroy($image);
?>
```

**输出：**
![](img/509225ace9937672a214f95b41bfd76f.png)

**引用：**[http://php.net/manual/en/function.imagefilledarc.php](http://php.net/manual/en/function.imagefilledarc.php)