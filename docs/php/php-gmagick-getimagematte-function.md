# PHP|Gmagick getImageMatte()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagematte-function/](https://www.geeksforgeeks.org/php-gmagick-getimagematte-function/)

**Gmagick：：getImageMatte()**函数是 PHP 中的一个内置函数，用于获取 Gmagick 对象的遮罩通道。

**语法：**

```php
*int* Gmagick::getimagematte( void )
```

**参数：**此函数不接受任何参数。

**返回值：**如果图像包含遮罩通道，则此函数返回 True，否则返回 False。

下面的程序演示了 PHP 中的**Gmagick：：getImageMatte()**函数：

**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

**程序 1：**

```php
<?php

// Create new Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageMatte function
$res = $Gmagick->getImageMatte();

// header("Content-Type: image/jpg");
echo $res;

?>
```

发帖主题：Re：Колибри0.7.0

```php
1

```

**原始图像 2：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**程序 2：**

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

$res = $im->getImageMatte();

// Display Result
echo $res;
?>
```

发帖主题：Re：Колибри0.7.0

```php
1

```

**引用：**[http://php.net/manual/en/gmagick.getimagematte.php](http://php.net/manual/en/gmagick.getimagematte.php)