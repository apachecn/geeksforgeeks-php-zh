# PHP|Gmagick blurimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-blurimage-function/](https://www.geeksforgeeks.org/php-gmagick-blurimage-function/)

**Gmagick：：blurimage()**函数是 PHP 中的内置函数，用于向图像添加模糊滤镜。

**语法：**

```php
*Gmagick* Gmagick::blurimage( $radius, $sigma, $channel )
```

*
**参数：**此函数接受上述三个参数，如下所述：

*   **$Radius：**此参数用于设置图像中的模糊半径。
*   **$sigma：**它设置标准偏差。
*   **$channel：**此参数设置通道类型常量。 如果没有提供，则所有通道都是模糊的。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的**Gmagick：：blurimage()**函数：

**原始图像：**
![](img/88e955c2701e97341d552eba1b5adceb.png)

**程序 1：**

```php
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// Use blurimage() function 
$gmagick->blurimage(7, 8);

header('Content-type: image/png'); 

// Ouput the image 
echo $gmagick; 
?> 
```

**输出：**
![](img/72326d3c9d9c9bd0fdc09b016584a8bb.png)

**程序 2：**

```php
<?php 

// Create a GmagickDraw object 
$draw = new GmagickDraw(); 

// Create GmagickPixel object 
$strokeColor = new GmagickPixel('Red'); 
$fillColor = new GmagickPixel('Green'); 

// Set the color, opacity of image 
$draw->setStrokeOpacity(1); 
$draw->setStrokeColor('Red'); 
$draw->setFillColor('Green'); 

// Set the width and height of image 
$draw->setStrokeWidth(7); 
$draw->setFontSize(72); 

// Function to draw circle  
$draw->circle(250, 250, 100, 150); 

$gmagick = new Gmagick(); 
$gmagick->newImage(500, 500, 'White'); 
$gmagick->setImageFormat("png"); 
$gmagick->drawImage($draw); 

// Use blurimage() function 
$gmagick->blurimage(7, 5);

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/470f090d853e056a4934c8b85e80da14.png)

**引用：**[http://php.net/manual/en/gmagick.blurimage.php](http://php.net/manual/en/gmagick.blurimage.php)