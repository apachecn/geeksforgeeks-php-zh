# PHP|Imagick setImageRenderingIntent()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagerenderingintent-function/](https://www.geeksforgeeks.org/php-imagick-setimagerenderingintent-function/)

**Imagick：：setImageRenderingIntent()**函数是 PHP 中的内置函数，用于设置图像渲染意图。

**语法：**

```
*bool* Imagick::setImageRenderingIntent( $rend_intent )
```

**参数：**此函数接受指定图像渲染意图的单个参数*$REND_INTENT*。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：setImageRenderingIntent()**函数：

**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

**程序 1：**

```
<?php

// Create new Imagick object
$im = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageRenderingIntent function
$res = $im->getImageRenderingIntent();
echo "Before: " . $res ."</br>";

// setImageRenderingIntent function
$im->setImageRenderingIntent(17);

// using getImageRenderingIntent function
$res = $im->getImageRenderingIntent();

// Display result
echo "After: " . $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
Before: 2
After: 17

```

**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**程序 2：**

```
<?php 
$string = "Computer Science portal for Geeks!"; 

// creating new image of above String 
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

// using getImageRenderingIntent function
$res = $im->getImageRenderingIntent();
echo "Before: " . $res ."</br>";

// setImageRenderingIntent function
$im->setImageRenderingIntent(10);

// using getImageRenderingIntent function
$res = $im->getImageRenderingIntent();

// Display result
echo "After: " . $res;
?>
```

发帖主题：Re：Колибри0.7.0

```
Before: 2
After: 10 

```

**引用：**[http://php.net/manual/en/imagick.setimagerenderingintent.php](http://php.net/manual/en/imagick.setimagerenderingintent.php)