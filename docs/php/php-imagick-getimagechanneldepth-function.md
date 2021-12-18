# PHP|Imagick getImageChannelDepth()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagechanneldepth-function/](https://www.geeksforgeeks.org/php-imagick-getimagechanneldepth-function/)

**Imagick：：getImageChannelDepth()**函数是 PHP 中的内置函数，用于获取通道图像的深度。

**语法：**

```php
*int* Imagick::getImageChannelDepth( $channel )
```

**参数：**此函数接受单个参数*$channel*，该参数指定对通道模式有效的通道常量。 CHANNEL 的默认值为**Imagick：：Channel_Default**。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：getImageChannelDepth()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```php
<?php

// Create new imagick object
$im = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageChannelDepth function
// with different channel
echo $im->getImageChannelDepth(imagick::CHANNEL_RED) . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_GRAY) . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_CYAN) . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_GREEN) . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_BLUE) . "</br>";
?>
```

发帖主题：Re：Колибри0.7.0

```php
8
8
8
8
8

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

```php
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

// Using getImageChannelDepth function
// with different channel
echo $im->getImageChannelDepth(imagick::CHANNEL_RED) . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_GRAY) . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_CYAN) . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_GREEN) . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_BLUE) . "</br>";
?>
```

发帖主题：Re：Колибри0.7.0

```php
8
8
8
16
8

```

**引用：**[http://php.net/manual/en/imagick.getimagechanneldepth.php](http://php.net/manual/en/imagick.getimagechanneldepth.php)