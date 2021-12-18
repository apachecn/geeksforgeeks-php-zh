# PHP|Gmagick getImageRenderingIntent()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagerenderingintent-function/](https://www.geeksforgeeks.org/php-gmagick-getimagerenderingintent-function/)

**Gmagick：：getImageRenderingIntent()**函数是 PHP 中的内置函数，用于获取图像渲染意图。

**语法：**

```
*int* Gmagick::getImageRenderingIntent( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回图像的渲染意图。

下面的程序演示了 PHP 中的**Gmagick：：getImageRenderingIntent()**函数：

**原始图像 1：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

**程序 1：**

```
<?php

// Create new Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageRenderingIntent function
$res = $gmagick->getImageRenderingIntent();

// Display result
echo($res);
?>
```

发帖主题：Re：Колибри0.7.0

```
2

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

// Using getImageRenderingIntent function
$res = $im->getImageRenderingIntent();
echo "Before: " . $res . "</br>";

// Set image renderingintent 
$im->setImageRenderingIntent(8);

// Using getImageRenderingIntent function
$res = $im->getImageRenderingIntent();

// Display result
echo "After " . $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
Before: 2
After 8 

```

**引用：**[http://php.net/manual/en/gmagick.getimagerenderingintent.php](http://php.net/manual/en/gmagick.getimagerenderingintent.php)