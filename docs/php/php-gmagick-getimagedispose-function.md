# PHP|Gmagick getImageDispose()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagedispose-function/](https://www.geeksforgeeks.org/php-gmagick-getimagedispose-function/)

**Gmagick：：getImageDispose()**函数是 PHP 中的内置函数，用于返回图像处理方法。

**语法：**

```
*int* Gmagick::getImageDispose( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数在成功时返回 Dispose 方法。

以下程序说明了 PHP 中的**Gmagick：：getImageDispose()**函数：

**原始图像 1：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

**程序 1：**

```
<?php

// Create new Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageDispose function
$res = $gmagick->getImageDispose();

// Display result
echo($res);
?>
```

发帖主题：Re：Колибри0.7.0

```
0

```

**原始图像 2：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**程序 2：**

```
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
$im->setImageFormat('jpeg'); 
$im->setImageDispose(5);

// Using getImageDispose function
$res = $im->getImageDispose();

// Display Result
echo($res);

?>
```

发帖主题：Re：Колибри0.7.0

```
5

```

**引用：**[http://php.net/manual/en/gmagick.getimagedispose.php](http://php.net/manual/en/gmagick.getimagedispose.php)