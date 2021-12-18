# PHP|Imagick borderImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-borderimage-function/](https://www.geeksforgeeks.org/php-imagick-borderimage-function/)

**Imagick：：borderImage()**函数是 PHP 中的内置函数，用于在图像中绘制边框。 此函数用于创建以给定颜色包围图像的边框。

**语法：**

```php
*bool* Imagick::borderImage( $bordercolor, $width, $height )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$borderColor：**此参数是 ImagickPixel 对象或包含边框颜色的字符串。
*   **$width：**此参数用于设置边框宽度。
*   **$Height：**该参数用于设置边框高度。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：borderImage()**函数：

**程序 1：**

```php
<?php

// Create an image object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Set the border in the given image
$image->borderImage('green', 100, 100);

header("Content-Type: image/jpg");

// Display image
echo $image;
?>
```

**输出：**
![border image](img/8dc6ac54ab8dbdf84f4ed135c502a6a3.png)

**程序 2：**

```php
<?php

// Create an image object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/adaptiveThresholdImage.png');

// Set the border in the given image
$image->borderImage('green', 20, 20);

header("Content-Type: image/jpg");

// Display image
echo $image;
?>
```

**输出：**
![border image](img/97dd4f5017c4d940daf6c9f7c16d1c5f.png)

**相关文章：**

*   [PHP|Imagick addImage()函数](https://www.geeksforgeeks.org/php-imagick-addimage-function/)
*   [PHP|Imagick addNoiseImage()函数](https://www.geeksforgeeks.org/php-imagickaddnoiseimage-function/)
*   [PHP|Imagick AdaptiveBlurImage()函数](https://www.geeksforgeeks.org/php-imagickadaptiveblurimage-function/)

**引用：**[http://php.net/manual/en/imagick.borderimage.php](http://php.net/manual/en/imagick.borderimage.php)