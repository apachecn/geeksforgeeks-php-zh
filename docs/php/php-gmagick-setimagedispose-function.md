# PHP|Gmagick setImageDispose()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimagedispose-function/](https://www.geeksforgeeks.org/php-gmagick-setimagedispose-function/)

**Gmagick：：setImageDispose()**函数是 PHP 中的内置函数，用于设置图像处理方法。

**语法：**

```
*Gmagick* Gmagick::setimagedispose( $disposeType )
```

**参数：**此函数接受指定图像处理类型的单个参数*$disposeType*。

**返回值：**此函数在成功时返回 Gmagick 对象。

下面的程序演示了 PHP 中的**Gmagick：：setImageDispose()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```
<?php

// Create new Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageDispose function
$res = $gmagick->getImageDispose();

// Display result
echo "dispose Before: " . $res . "</br>";

// Set Dispose of Gmagick Object
$gmagick->setImageDispose(4);

// using getImageDispose function
$res = $gmagick->getImageDispose();

// Display result
echo "dispose After: " . $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
dispose Before: 0
dispose After: 4

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

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

// Using getImageDispose function
$res = $im->getImageDispose();

// Display result
echo "dispose Before: " . $res . "</br>";

// Set Dispose of Gmagick Object
$im->setImageDispose(10);

// Using getImageDispose function
$res = $im->getImageDispose();

// Display result
echo "dispose After: " . $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
dispose Before: 0
dispose After: 10 

```

**引用：**[http://php.net/manual/en/gmagick.setimagedispose.php](http://php.net/manual/en/gmagick.setimagedispose.php)