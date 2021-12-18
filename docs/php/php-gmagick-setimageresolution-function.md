# PHP|Gmagick setimageresolution()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimageresolution-function/](https://www.geeksforgeeks.org/php-gmagick-setimageresolution-function/)

**gmagick：：setimageresolution()**函数是 PHP 中的内置函数，用于设置图像对象的分辨率。

**语法：**

```php
*Gmagick* Gmagick::setImageResolution($x_resolution, $y_resolution)
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x_RESOLUTION：**指定 x 轴分辨率的必选参数。
*   **$y_Resolution：**指定 y 轴分辨率的必选参数。

**返回值：**此函数在成功时返回 Gmagick 对象。

下面的程序演示了 PHP 中的**Gmagick：：setimageresolution()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```php
<?php

$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Getting Resolution of image
// using getimageresolution function
$res = $gmagick->getImageResolution();
echo "X = ".$res['x'] . "</br>";
echo "Y = ".$res['y'] . "</br>";

// Function to set image resolution
$gmagick->setimageresolution(50, 50);

echo "After Set Resolution: </br>";

// Getting Resolution of image
// using getimageresolution function
$res = $gmagick->getImageResolution();
echo "X = " . $res['x'] . "</br>";
echo "Y = " . $res['y'] . "</br>";
?>
```

发帖主题：Re：Колибри0.7.0

```php
X = 37.8
Y = 37.8
After Set Resolution:
X = 50
Y = 50

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

```php
<?php 
$string = "Computer Science portal for Geeks!"; 

// Creating new image of above String 
// and add color and background 
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
echo "Before: </br>";

// Getting Resolution of created image
// using getimageresolution function
$res = $im->getImageResolution();
echo "X = ".$res['x'] . "</br>";
echo "Y = ".$res['y'] ." </br>";

// Set image resolution (50, 50) 
$im->setimageresolution(50, 50); 

echo "After:</br> ";

// Getting Resolution of created image
// using getimageresolution function
$res = $im->getImageResolution();
echo "X = ".$res['x'] . "</br>";
echo "Y = ".$res['y'] ." </br>";
?> 
```

发帖主题：Re：Колибри0.7.0

```php
Before:
X = 0
Y = 0
After:
X = 50
Y = 50

```

**引用：**[http://php.net/manual/en/gmagick.setimageresolution.php](http://php.net/manual/en/gmagick.setimageresolution.php)