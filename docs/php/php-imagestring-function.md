# PHP|imagestring()函数

> Original: [https://www.geeksforgeeks.org/php-imagestring-function/](https://www.geeksforgeeks.org/php-imagestring-function/)

Imagestring()函数是 PHP 中的一个内置函数，用于水平绘制字符串。 此函数用于在给定位置绘制字符串。

**语法：**

```
bool imagestring( $image, $font, $x, $y, $string, $color )
```

**参数：**此函数接受上述 6 个参数，如下所述：

*   **$image：**imagecreatetruecolor()函数用于创建给定大小的空白图像。
*   **$FONT：**该参数用于设置字体大小。 Latin2 编码中的内置字体可以是 1、2、3、4、5 或使用 imageloadfont()函数注册的其他字体标识符。
*   **$x：**此参数用于保存左上角的 x 坐标。
*   **$y：**此参数用于保存左上角的 y 坐标。
*   **$string：**此参数用于保存要写入的字符串。
*   **$COLOR：**此参数用于保存图像的颜色。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的 imagestring()函数。
**程序 1：**

```
<?php

// Create the size of image or blank image
$image = imagecreate(500, 300);

// Set the background color of image
$background_color = imagecolorallocate($image, 0, 153, 0);

// Set the text color of image
$text_color = imagecolorallocate($image, 255, 255, 255);

// Function to create image which contains string.
imagestring($image, 5, 180, 100,  "GeeksforGeeks", $text_color);
imagestring($image, 3, 160, 120,  "A computer science portal", $text_color);

header("Content-Type: image/png");

imagepng($image);
imagedestroy($image);
?>
```

**输出：**
![create image function](img/683a559443f172078c5e511133a3bf6f.png)

**程序 2：**

```
<?php

// Create the size of image or blank image
$image = imagecreate(500, 300);

// Set the background color of image
$background_color = imagecolorallocate($image, 255, 255, 255);

// Set the text color of image
$text_color = imagecolorallocate($image, 0, 153, 0);

// Function to create image which contains string.
imagestring($image, 5, 50, 100, 
     "GeeksforGeeks: A computer science portal", $text_color);

header("Content-Type: image/png");

imagepng($image);
imagedestroy($image);
?>
```

**输出：**
![imagestring function](img/645e16512cd9f510920f6dcb834332fb.png)

**相关文章：**

*   [PHP|imagedashedline()函数](https://www.geeksforgeeks.org/php-imagedashedline-function/)
*   [PHP|imagecolorat()函数](https://www.geeksforgeeks.org/php-imagecolorat-function/)
*   [PHP|imagepolygon()函数](https://www.geeksforgeeks.org/php-imagepolygon-function/)

**引用：**[http://php.net/manual/en/function.imagestring.php](http://php.net/manual/en/function.imagestring.php)