# PHP|Imagick setImageDispose()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagedispose-function/](https://www.geeksforgeeks.org/php-imagick-setimagedispose-function/)

**Imagick：：setImageDispose()**函数是 PHP 中的内置函数，用于设置图像处理方法。

**语法：**

```
*bool* Imagick::setImageDispose( $dispose )
```

**参数：**此函数接受单个参数*$dispose*，该参数指定要设置的 Dispose Imagick 对象。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：setImageDispose()**函数：

**原图：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)
**程序 1：**

```
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageDispose function
$res = $imagick->getImageDispose();

// Display result
echo "dispose Before: " . $res . "</br>";

// Set Dispose of Imagick Object
$imagick->setImageDispose(4);

// using getImageDispose function
$res = $imagick->getImageDispose();

// Display result
echo "dispose After: " . $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
dispose Before: 0
dispose After: 4

```

**原图：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)
**程序 2：**

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
$im->setImageFormat('jpeg');

// Using getImageDispose function
$res = $im->getImageDispose();

// Display result
echo "dispose Before: " . $res . "</br>";

// Set Dispose of Imagick Object
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

**引用：**[http://php.net/manual/en/imagick.setimagedispose.php](http://php.net/manual/en/imagick.setimagedispose.php)