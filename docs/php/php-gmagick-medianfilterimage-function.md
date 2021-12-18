# PHP|Gmagick medianfilterimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-medianfilterimage-function/](https://www.geeksforgeeks.org/php-gmagick-medianfilterimage-function/)

**Gmagick：：medianfilterimage()**函数是 PHP 中的一个内置函数，用于应用数字过滤器来改善噪声图像的质量。 此过滤器将每个像素替换为其相邻像素的中值，该中值由半径定义。

**语法：**

```php
*void* Gmagick::medianfilterimage( $radius )
```

*
**参数：**此函数接受单个参数*$Radius*，该参数用于保存像素的半径。

**返回值：**此函数返回带中值滤波的 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的**Gmagick：：medianfilterimage()**函数：

**程序 1：**
**输入图像：**
![](img/88e955c2701e97341d552eba1b5adceb.png)

```php
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// Use medianfilterimage function 
$gmagick->medianfilterimage(12);

header('Content-type: image/png'); 

// Output the image 
echo $gmagick; 
?> 
```

**输出：**
![](img/2a914611e6d08684646c5934113d165d.png)

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

// Use medianfilterimage function 
$gmagick->medianfilterimage(12);

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/1f288a6524a165e9fe995049467e84a0.png)

**引用：**[http://php.net/manual/en/gmagick.medianfilterimage.php](http://php.net/manual/en/gmagick.medianfilterimage.php)