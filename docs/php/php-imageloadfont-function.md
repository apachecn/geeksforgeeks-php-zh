# PHP|imageloadfont()函数

> Original: [https://www.geeksforgeeks.org/php-imageloadfont-function/](https://www.geeksforgeeks.org/php-imageloadfont-function/)

函数的作用是：**imageloadfont()函数**是 PHP 的内置函数，用于加载新字体。 支持 GDF 字体，可从[此处](http://www.danceswithferrets.org/lab/gdfs/)下载。

**语法：**

```
*int* imageloadfont( *string* $file )
```

**参数：**此函数接受保存字体的单个参数**$file**。

**返回值：**此函数返回的字体标识总是大于 5，避免与内置字体冲突，出错时返回 False。

下面给出的程序演示了 PHP 中的**imageloadfont()函数**：

**程序 1(在图纸上书写)：**

```
<?php

// Create a new image instance
$im = imagecreatetruecolor(105, 15);

// Prepare the colors
$black = imagecolorallocate($im, 0, 0, 0);
$white = imagecolorallocate($im, 255, 255, 255);

// Make the background white
imagefilledrectangle($im, 0, 0, 700, 250, $white);

// Load the gd font from local folder
// and write 'GeeksforGeeks'
$font = imageloadfont('./Hollow_8x16_LE.gdf');
imagestring($im, $font, 0, 0, 'GeeksforGeeks', $black);

// Scale the image bigger
$im1 = imagescale($im, 700);

// Output to browser
header('Content-type: image/png');
imagepng($im1);
imagedestroy($im);
?>
```

**输出：**
![](img/1cfd9a3bf798869715bf9613fc035f85.png)

**程序 2(在图像上写入)：**

```
<?php

// Create an image instance
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Prepare the red color
$red = imagecolorallocate($im, 255, 0, 0);

// Load the gd font from local folder and write 'GeeksforGeeks'
$font = imageloadfont('./Hollow_8x16_LE.gdf');
imagestring($im, $font, 200, 100, 'GeeksforGeeks', $red);

// Output to browser
header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/685d9571dbde7094ecced236a883daf8.png)

**引用：**[https://www.php.net/manual/en/function.imageloadfont.php](https://www.php.net/manual/en/function.imageloadfont.php)