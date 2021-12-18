# PHP|Gmagick getimageBluepriary()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimageblueprimary-function/](https://www.geeksforgeeks.org/php-gmagick-getimageblueprimary-function/)

Gmagick：：getimageBluepriary()函数是 PHP 中的一个内置函数，用于返回色度蓝色主点。

**语法：**

```php
*public* Gmagick::getimageblueprimary( void ) : array
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个包含点的 x 和 y 坐标的数组。

下面的程序演示了 PHP 中的 Gmagick：：getimageBluepriary()函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```php
<?php

// Create new Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getimageblueprimaryfunction
$res = $gmagick->getimageblueprimary();
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array ( [x] => 0.15000000596046 [y] => 0.059999998658895 ) 

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

```php
<?php 

$string = "Computer Science portal for Geeks!"; 

// Creating new image of above String 
// and add color  
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

$im->setImageFormat('jpeg'); 
$im->setImageBluePrimary(2.6, 2.9);

// Using getImageBluePrimary function
$res = $im->getimageblueprimary();

// Display Result
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array ( [x] => 2.6 [y] => 2.9 ) 

```

**引用：**[http://php.net/manual/en/gmagick.getimageblueprimary.php](http://php.net/manual/en/gmagick.getimageblueprimary.php)