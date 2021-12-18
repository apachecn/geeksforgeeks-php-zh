# PHP|Imagick getImageWhitePoint()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagewhitepoint-function/](https://www.geeksforgeeks.org/php-imagick-getimagewhitepoint-function/)

**Imagick：：getImageWhitePoint()**函数是 PHP 中的内置函数，用于获取 Imagick 对象的色度白点。

**语法：**

```
*bool* Imagick::getImageWhitePoint( void)
```

**参数：**此函数不接受任何参数。

**返回值：**此函数将色度白点作为具有键值 x 和 y 的关联数组返回。

下面的程序演示了 PHP 中的**Imagick：：getImageWhitePoint()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```
<?php

// Craeate new imagic object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Getting Length of image
// using getimagerelength function
$res = $imagick->getImageWhitePoint();

// Display result
print_r($res);

?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [x] => 0.31270000338554 [y] => 0.3289999961853 ) 

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

```
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

// getting Length of image
// using getimagerelength function
$res = $im->getImageWhitePoint();

// Display result
print_r($res);

?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [x] => 0.31270000338554 [y] => 0.3289999961853 ) 

```

**引用：**[http://php.net/manual/en/imagick.getimagewhitepoint.php](http://php.net/manual/en/imagick.getimagewhitepoint.php)