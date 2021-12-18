# PHP|Imagick getImageChannelRange()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagechannelrange-function/](https://www.geeksforgeeks.org/php-imagick-getimagechannelrange-function/)

**Imagick：：getImageChannelRange()**函数是 PHP 中的内置函数，用于获取通道范围。

**语法：**

```
*array* Imagick ::getImageChannelRange( $channel )
```

**参数：**此函数接受单个参数*$channel*，该参数指定要查找图像通道范围的通道。 CHANNEL 的默认值为 I**MAGICK：：CHANNEL_DEFAULT**。

**返回值：**此函数返回包含所需通道的最小值和最大值的数组。

下面的程序演示了 PHP 中的**Imagick：：getImageChannelRange()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```
<?php

// Create new Imagick object
$im = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageChannelRange function
// with red channel
$res = $im->getImageChannelRange(imagick::CHANNEL_RED);

// Display result
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [minima] => 0 [maxima] => 65535 ) 

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

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

// Using getImageChannelRange function
// with red channel
$res = $im->getImageChannelRange(imagick::CHANNEL_GREEN);

// Display result
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [minima] => 32896 [maxima] => 65535 ) 

```

**引用：**[http://php.net/manual/en/imagick.getimagechannelrange.php](http://php.net/manual/en/imagick.getimagechannelrange.php)