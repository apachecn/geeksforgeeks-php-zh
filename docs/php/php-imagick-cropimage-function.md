# PHP|Imagick cropImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-cropimage-function/](https://www.geeksforgeeks.org/php-imagick-cropimage-function/)

**Imagick：：cropImage()**函数是 PHP 中的一个内置函数，用于提取图像的区域。
**语法：**和

```php
*int* Imagick::cropImage( $width, $height, $x, $y )
```

**参数：**此函数接受上述四个参数，如下所述。

*   **$width：**此参数用于指定裁剪图像的宽度。
*   **$Height：**此参数用于指定裁剪图像的高度。
*   **$x：**此参数用于指定左上角裁剪图像的 X 坐标。
*   **$y：**此参数用于指定左上角裁剪图像的 Y 坐标。

**返回值：**成功时此函数返回 True。
以下程序说明 PHP：
**原始图像：**和
中的**Imagick：：cropImage()**函数

![](img/efa5ea8e0258291fa60ad9a32c288072.png)

**程序 1：**和

## PHP

```php
<?php

// require_once('path/vendor/autoload.php');

// Create an imagick object
 $image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Imagick function to crop Image 
$image->cropImage(390, 100, 0, 0);

header("Content-Type: image/jpg");

// Display the image
echo $image->getImageBlob();
?> 
```

发帖主题：Re：Колибри0.7.8.0

![](img/75980d8ccae228d7913f6a2bc77999bc.png)

**原图：**和

![](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**程序 2：**和

## PHP

```php
<?php
$string = "Computer Science portal for Geeks!";

// creating new image of above String
// and add color and background
$im = new Imagick();
$draw = new ImagickDraw();

// Fill the color in image
$draw->setFillColor(new ImagickPixel('green'));

// Set the text font size
$draw->setFontSize(50);

$matrix = $im->queryFontMetrics($draw, $string);
$draw->annotation(0, 40, $string);
$im->newImage($matrix['textWidth'], $matrix['textHeight'],
         new ImagickPixel('white'));

// Draw the image        
$im->drawImage($draw);

// Set the image format
$im->setImageFormat('png');

// Imagick function to crop Image
$im->cropImage(420, 120, 0, 0);

header("Content-Type: image/jpg");

// Display the image
echo $im->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/27e6d82bce6e606fa78ea78452009081.png)

**引用：**[http://php.net/manual/en/imagick.cropimage.php](http://php.net/manual/en/imagick.cropimage.php)