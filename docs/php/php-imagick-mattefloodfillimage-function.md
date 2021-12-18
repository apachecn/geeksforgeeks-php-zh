# PHP|Imagick matteFlodfulImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-mattefloodfillimage-function/](https://www.geeksforgeeks.org/php-imagick-mattefloodfillimage-function/)

**Imagick：：matteFlodfulImage()函数**是 PHP 中的一个内置函数，用于更改颜色的透明度值。 此函数用于更改与目标匹配且是其直接邻居的任何像素的透明度值。

**语法：**

```
*bool* Imagick::matteFloodfillImage(*float* $alpha, *float* $fuzz, 
                                   *mixed* $bordercolor, *int* $x, *int* $y)
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$alpha：**此参数保持透明度级别，1 表示完全不透明，0 表示完全透明。
*   **$alpha：**此参数保持可接受的公差，将两种颜色视为相同。
*   **$borderColor：**此参数保存表示边框颜色的 ImagickPixel 对象或字符串。
*   **$x：**此参数保存操作的起始 x 坐标。
*   **$y：**此参数保存操作的起始 y 坐标。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的 Imagick：：matteFlodfulImage()函数：

**程序：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Applying the matteFloodfillImage() function
$imagick->matteFloodfillImage(0.5, 0, 'red', 0, 0); 

header("Content-Type: image/jpg"); 

// Display the output image 
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/94522c1763008d1afe0a3df71b253e1c.png)

**引用：**[https://www.php.net/manual/en/imagick.mattefloodfillimage.php](https://www.php.net/manual/en/imagick.mattefloodfillimage.php)