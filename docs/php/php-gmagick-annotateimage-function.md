# PHP|Gmagick 注解图像()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-annotateimage-function/](https://www.geeksforgeeks.org/php-gmagick-annotateimage-function/)

**Gmagick：：AnnotateImage()**函数是 PHP 中的一个内置函数，用于注释带有文本的图像。 此函数在成功时返回 True。

**语法：**

```
*Gmagick* Gmagick::annotateimage( $GmagickDraw, $x, $y, $angle, 
$text )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$GmagickDraw：**此参数用于创建包含绘制文本设置的 GmagickDraw 对象。
*   **$x：**此参数设置为文本左侧的水平偏移(以像素为单位)。
*   **$y：**此参数设置为文本基线的垂直偏移(以像素为单位)。
*   **$angle：**书写文本的角度。
*   **$text：**需要绘制的字符串。

**返回值：**此函数返回带有批注的 Gmagick 对象。

下面的程序演示了 PHP 中的**Gmagick：：AnnotateImage()**函数：

**程序 1：**

```
<?php

/* Create some objects */
$image = new Gmagick();
$draw = new GmagickDraw();
$pixel = new GmagickPixel('white');

/* New image */
$image->newImage(800, 300, $pixel);

/* Black text */
$draw->setFillColor('green');

/* Font properties */
$draw->setFont('Bookman-DemiItalic');
$draw->setFontSize( 30 );

/* Create text */
$image->annotateImage($draw, 30, 140, 0, 
   'GeeksforGeeks: A computer science portal');

/* Give image a format */
$image->setImageFormat('png');

/* Output the image with headers */
header('Content-type: image/png');
echo $image;

?>
```

**输出：**
![annonate Image](img/2f4c0095b070ebe5c0eb6ab06c32d5ce.png)

**程序 2：**

```
<?php

/* Create some objects */
$image = new Gmagick();
$draw = new GmagickDraw();
$image = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

/* Black text */
$draw->setFillColor('green');

/* Font properties */
$draw->setFont('Bookman-DemiItalic');
$draw->setFontSize( 30 );

/* Create text */
$image->annotateImage($draw, 5, 120, 0, 
   'GeeksforGeeks: A computer science portal');

/* Give image a format */
$image->setImageFormat('png');

/* Output the image with headers */
header('Content-type: image/png');
echo $image;

?>
```

**输出：**
![annonate image](img/0d540ba447cd2eb902abe39f17d42116.png)

**引用：**[http://php.net/manual/en/gmagick.annotateimage.php](http://php.net/manual/en/gmagick.annotateimage.php)