# PHP|Imagick setImageChannelDepth()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagechanneldepth-function/](https://www.geeksforgeeks.org/php-imagick-setimagechanneldepth-function/)

**Imagick：：setImageChannelDepth()**函数是 PHP 中的内置函数，用于设置特定通道图像的深度。

**语法：**

```php
*bool* Imagick::setImageChannelDepth( $channel, $depth )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$channel：**此参数用于指定通道常量。 以下是常量通道列表：
    **通道常量：**
    *   Imagick：：Channel_ 未定义
    *   Imagick：：Channel_red
    *   Imagick：：Channel_Gray
    *   Imagick：：Channel_Cyan
    *   Imagick：：Channel_Green
    *   Imagick：：Channel_Magenta
    *   Imagick：：Channel_Blue
    *   Imagick：：Channel_ 黄色
    *   Imagick：：Channel_Alpha
    *   Imagick：：Channel_Opacity
    *   ==同步，由 Elderman 更正==@ELDER_MAN
    *   Imagick：：Channel_Black
    *   ==同步，由 Elderman 更正==@ELDER_MAN
    *   ==同步，由 Elderman 更正==@ELDER_MAN
    *   Imagick：：Channel_Default
*   **$Depth：**此参数用于指定 Imagick 对象要设置的深度。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：setImageChannelDepth()**函数：

**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

**程序 1：**

```php
<?php

// Create new Imagick object
$im = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageChannelDepth function
// with red channel
echo "Before Set Channel depth: " . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_RED) . "</br>";

// Set channel Depth of CYAN and GREEN Channel
$im->setImageChannelDepth(imagick::CHANNEL_RED, 4);

echo "After Set Channel depth: " . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_RED) . "</br>";
?>
```

发帖主题：Re：Колибри0.7.0

```php
Before Set Channel depth:
8
After Set Channel depth:
4

```

**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**程序 2：**

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
// with red channel
echo "Before Set Channel depth: " . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_GREEN) . "</br>";

// Set channel Depth of Green Channel
$im->setImageChannelDepth(imagick::CHANNEL_GREEN, 8);

echo "After Set Channel depth: " . "</br>";
echo $im->getImageChannelDepth(imagick::CHANNEL_GREEN) . "</br>";
?>
```

发帖主题：Re：Колибри0.7.0

```php
Before Set Channel depth:
16
After Set Channel depth:
8

```

**引用：**[http://php.net/manual/en/imagick.setimagechanneldepth.php](http://php.net/manual/en/imagick.setimagechanneldepth.php)