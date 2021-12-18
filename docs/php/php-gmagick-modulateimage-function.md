# PHP|Gmagick modateimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-modulateimage-function/](https://www.geeksforgeeks.org/php-gmagick-modulateimage-function/)

**gmagick：：modateimage()**函数是 PHP 中的内置函数，用于控制图像的亮度、饱和度和色调。

**语法：**

```php
*Gmagick* Gmagick::modulateimage( $brightness, $saturation, $hue )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Brightness：**此参数用于保存亮度值。
*   **$饱和度：**此参数用于保持饱和度的值。
*   **$hue：**此参数用于保存色调的值。

**返回值：**此函数成功时返回 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的**Gmagick：：modateImage()**函数：

**程序 1：**
**输入图像：**
![](img/88e955c2701e97341d552eba1b5adceb.png)

```php
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// Use modulateimage function 
$gmagick->modulateimage(60, 100, 100);

header('Content-type: image/png'); 

// Output the image 
echo $gmagick; 
?> 
```

**输出：**
![](img/49e3b6b2f34cbabd9ecf2c4a9445f894.png)

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

// Use modulateimage function 
$gmagick->modulateimage(60, 100, 100);

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/2c9c56e436349404bf4d394f06520d70.png)

**引用：**[http://php.net/manual/en/gmagick.modulateimage.php](http://php.net/manual/en/gmagick.modulateimage.php)