# PHP|Gmagick WriteImage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-writeimage-function/](https://www.geeksforgeeks.org/php-gmagick-writeimage-function/)

**Gmagick：：WriteImage()函数**是 PHP 中的一个内置函数，用于将图像写入指定的文件名。

**语法：**

```
*Gmagick* Gmagick::writeimage( *string* $filename, *bool* $all_frames )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename：**它指定文件的名称。
*   **$ALL_FRAMES(可选)：**它指定需要的所有帧。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 GmagickException。
**使用 Image：**捕获画布区域。
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)
下面给出的程序说明了 PHP 中的**Gmagick：：WriteImage()函数**：

**程序 1：**写入镜像

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Write the image to a local folder
$gmagick->writeimage('my_image.png');
echo 'Image saved successfully';
?>
```

发帖主题：Re：Колибри0.7.0

```
This will save the image successfully.
```

**程序 2：**写入图纸

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('white');

// Function to draw rectangle
$draw->rectangle(0, 0, 800, 400);

// Set the fill color
$draw->setFillColor('#1bd911');

// Set the font size
$draw->setfontsize(50);

// Annotate a text
$draw->annotate(30, 100, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Write the image to a local folder
$gmagick->writeimage('my_drawing.png');
echo 'Image saved successfully';
?>
```

**输出：**这会将图形保存在本地文件夹中。

```
Image saved successfully
```

**引用：**[https://www.php.net/manual/en/gmagick.writeimage.php](https://www.php.net/manual/en/gmagick.writeimage.php)