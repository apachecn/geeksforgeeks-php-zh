# PHP|Imagick getImageResolution()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageresolution-function/](https://www.geeksforgeeks.org/php-imagick-getimageresolution-function/)

**Imagick：：getImageResolution()**函数是 PHP 中的内置函数，用于获取图像对象的分辨率。

**语法：**

```php
*bool* Imagick::getImageResolution( void)
```

**参数：**此函数不接受任何参数。

**返回值：**此函数以数组形式返回分辨率。

下面的程序演示了 PHP 中的**Imagick：：getImageResolution()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```php
<?php

// Create an imagick image object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Getting Resolution of created image
// using getimageresolution function
$res = $im->getImageResolution();
echo "X = ".$res['x'] . "</br>";
echo "Y = ".$res['y'] ." </br>";
?>
```

发帖主题：Re：Колибри0.7.0

```php
X = 37.8
Y = 37.8

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

```php
<?php 

$string = "Computer Science portal for Geeks!"; 

// Creating new image of above String 
// and add color and background 
$im = new Imagick(); 
$draw = new ImagickDraw(); 

// Fill the color in image 
$draw->setFillColor(new ImagickPixel('green')); 

// Set the text font size 
$draw->setFontSize(50); 

$metrix = $im->queryFontMetrics($draw, $string); 
$draw->annotation(0, 40, $string); 
$im->newImage($metrix['textWidth'], $metrix['textHeight'], 
         new ImagickPixel('white')); 

// Draw the image          
$im->drawImage($draw); 
$im->setImageResolution(50, 50); 

// getting Resolution of created image
// using getimageresolution function
$res = $im->getImageResolution();
echo "X = ".$res['x'] . "</br>";
echo "Y = ".$res['y'] ." </br>";
?> 
```

发帖主题：Re：Колибри0.7.0

```php
X = 50
Y = 50 

```

**引用：**[http://php.net/manual/en/imagick.getimageresolution.php](http://php.net/manual/en/imagick.getimageresolution.php)