# PHP|Gmagick setimagechannelDeep()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimagechanneldepth-function/](https://www.geeksforgeeks.org/php-gmagick-setimagechanneldepth-function/)

**gmagick：：setimagechnelDeep()**函数是 PHP 中的内置函数，用于设置特定通道图像的深度。

**语法：**

```php
*Gmagick* Gmagick::setimagechanneldepth( $channel , $depth )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$channel：**此参数用于指定通道常量。 以下是常量通道列表：
    **通道常量：**
    *   Gmagick：：Channel_ 未定义
    *   Gmagick：：Channel_red
    *   Gmagick：：Channel_Gray
    *   Gmagick：：Channel_Cyan
    *   Gmagick：：Channel_green
    *   Gmagick：：Channel_Magenta
    *   Gmagick：：Channel_Blue
    *   Gmagick：：Channel_Huang
    *   Gmagick：：Channel_Alpha
    *   Gmagick：：Channel_Opacity
    *   Gmagick：：Channel_Matte
    *   Gmagick：：Channel_Black
    *   Gmagick：：Channel_index
    *   ==同步，由 Elderman 更正==@ELDER_MAN
    *   Gmagick：：Channel_Default
*   **$Depth：**此参数用于指定要为 Gmagick 对象设置的深度。

**返回值：**此函数在成功时返回 Gmagick 对象。

下面的程序说明了 PHP 中的**Gmagick：：setimagechnelDeep()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```php
<?php

// Create new Gmagick object
$im = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageChannelDepth function
// with red channel
echo "Before Set Channel depth: " . "</br>";
echo $im->getImageChannelDepth(Gmagick::CHANNEL_RED) . "</br>";

// Set channel Depth of CYAN and GREEN Channel
$im->setimagechanneldepth(Gmagick::CHANNEL_RED, 4);

echo "After Set Channel depth: " . "</br>";
echo $im->getImageChannelDepth(Gmagick::CHANNEL_RED) . "</br>";

?>
```

发帖主题：Re：Колибри0.7.0

```php
Before Set Channel depth:
8
After Set Channel depth:
4

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

```php
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

// Using getImageChannelDepth function
// with red channel
echo "Before Set Channel depth: " . "</br>";
echo $im->getImageChannelDepth(Gmagick::CHANNEL_GREEN) . "</br>";

// Set channel Depth of Green Channel
$im->setimagechanneldepth(Gmagick::CHANNEL_GREEN, 8);

echo "After Set Channel depth: " . "</br>";
echo $im->getImageChannelDepth(Gmagick::CHANNEL_GREEN) . "</br>";

?>
```

发帖主题：Re：Колибри0.7.0

```php
Before Set Channel depth:
16
After Set Channel depth:
8

```

**引用：**[http://php.net/manual/en/gmagick.setimagechanneldepth.php](http://php.net/manual/en/gmagick.setimagechanneldepth.php)