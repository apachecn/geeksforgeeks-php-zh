# PHP|Gmagick cropimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-cropimage-function/](https://www.geeksforgeeks.org/php-gmagick-cropimage-function/)

**Gmagick：：cropimage()**函数是 PHP 中的一个内置函数，用于提取图像的区域。 此函数用于裁剪图像的一部分。

**语法：**

```php
*public* Gmagick::cropimage( $width , $height , $x , $y )
```

**参数：**此函数接受上述四个参数，如下所述。

*   **$width：**此参数用于指定裁剪图像的宽度。
*   **$Height：**此参数用于指定裁剪图像的高度。
*   **$x：**此参数用于指定左上角裁剪图像的 X 坐标。
*   **$y：**此参数用于指定左上角裁剪图像的 Y 坐标。

**返回值：**此函数返回裁剪后的 Gmagick 对象。

下面的程序演示了 PHP 中的**Gmagick：：cropimage()**函数：

**原图 1：**
![](img/efa5ea8e0258291fa60ad9a32c288072.png)
**程序 1：**

```php
<?php 

// require_once('path/vendor/autoload.php'); 

// Create an Gmagick object 
 $image = new Gmagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png'); 

// Gmagick function to crop Image  
$image->cropimage(390, 100, 0, 0); 

header("Content-Type: image/jpg"); 

// Display the image 
echo $image->getImageBlob(); 
?>  
```

发帖主题：Re：Колибри0.7.0

**原始图像 2：**
![](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**程序 2：**

```php
<?php
$string = "Computer Science portal for Geeks!";

// Creating new image of above String
// and add color and background color
$im = new Gmagick();
$draw = new GmagickDraw();

// Fill the color in image
$draw->setFillColor(new GmagickPixel('green'));

// Set the text font size
$draw->setFontSize(50);

$metrix = $im->queryFontMetrics($draw, $string);
$draw->annotation(0, 40, $string);
$im->newImage($metrix['textWidth'], $metrix['textHeight'],
         new GmagickPixel('white'));

// Draw the image         
$im->drawImage($draw);

// Set the image format
$im->setImageFormat('png');

// Gmagick function to crop Image
$im->cropimage(420, 120, 0, 0); 

header("Content-Type: image/jpg"); 

// Display the image 
echo $im->getImageBlob(); 
?>
```

**输出：**
![](img/27e6d82bce6e606fa78ea78452009081.png)

**引用：**[http://php.net/manual/en/gmagick.cropimage.php](http://php.net/manual/en/gmagick.cropimage.php)