# PHP|Imagick setImageMatte()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagematte-function/](https://www.geeksforgeeks.org/php-imagick-setimagematte-function/)

**Imagick：：setImageMatte()**函数是 PHP 中的内置函数，用于设置 Imagick 对象的遮罩通道。

**语法：**

```
*bool* Imagick::setImageMatte( $matte )
```

**参数：**此函数接受单个参数*$matte*。 如果参数设置为 True，则激活遮罩通道；如果参数设置为 False，则禁用遮罩通道。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：setImageMatte()**函数：

**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

**程序 1：**

```
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageMatte function
$res = $imagick->getImageMatte();

// Display result
echo "Matte Before: " . $res . "</br>";

// Set Image matte true.
// If it set to false then matte will 
// disable and return nothing when 
// using getimagematte function
$imagick->setImageMatte(true);

// Using getImageMatte function
$res = $imagick->getImageMatte();

// Display result
echo "Matte After: " . $res . "</br>";
?>
```

发帖主题：Re：Колибри0.7.0

```
Matte Before: 1
Matte After: 1

```

**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**程序 2：**

```
<?php 

$string = "Computer Science portal for Geeks!"; 

// Creating new image of above String 
// and add color
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
$im->setImageFormat('jpeg'); 

// Using getImageMatte function
$res = $im->getImageMatte();

// Display result
echo "Matte Before: " . $res . "</br>";

// Set Image matte true/false or (0/1)
// if set false then matte will disable 
// and return nothing when 
// using getimagematte function
$im->setImageMatte(false);

// Using getImageMatte function
$res = $im->getImageMatte();

// Display result
echo "Matte After: " . $res . "</br>";
?>
```

发帖主题：Re：Колибри0.7.0

```
Matte Before: 1
Matte After: 

```

**引用：**[http://php.net/manual/en/imagick.setimagematte.php](http://php.net/manual/en/imagick.setimagematte.php)