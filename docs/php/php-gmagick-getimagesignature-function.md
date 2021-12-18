# PHP|Gmagick getimagesign()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagesignature-function/](https://www.geeksforgeeks.org/php-gmagick-getimagesignature-function/)

**gmagick：：getimagesign()**函数是 PHP 中的一个内置函数，用于为图像生成 SHA-256 消息摘要。

**语法：**

```
*string* Gmagick::getimagesignature( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回文件的 SHA-256 散列字符串。

下面的程序演示了 PHP 中的**Gmagick：：getimagesign()**函数：

**原始图像 1：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

**程序 1：**

```
<?php

// PHP program to illustrate getimagesignature() function
$image = new Gmagick(
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png");

// Using getimagesignature() function
$pixels = $image->getimagesignature();

print($pixels);
?>
```

发帖主题：Re：Колибри0.7.0

```
f64054f5bcb4cfb82c6126eff6d3d4e6be7d0e72d5620033442cecb4b9feabbd

```

**原始图像 2：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**程序 2：**

```
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

// Using getimagesignature function
$pixels = $im->getimagesignature();

print($pixels);
?>
```

发帖主题：Re：Колибри0.7.0

```
ed79035e13153385c344d19586e98941dd336165a3ca486200097c0bd2f4188c

```

**引用：**[http://php.net/manual/en/gmagick.getimagesignature.php](http://php.net/manual/en/gmagick.getimagesignature.php)