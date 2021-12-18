# PHP|Gmagick getimageunit()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimageunits-function/](https://www.geeksforgeeks.org/php-gmagick-getimageunits-function/)

**gmagick：：getimageunit()**函数是 PHP 中的一个内置函数，用于获取特定图像的分辨率单位。

**语法：**

```
*int* Gmagick::getimageunits( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回包含图像单位分辨率的整数。
以下程序说明 PHP：
**原始图像 1：**和
中的**Gmagick：：getimageunit()**函数

![](img/efa5ea8e0258291fa60ad9a32c288072.png)

**程序 1：**

## PHP

```
<?php

// PHP program to illustrate getimageunits function
$image = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Use getimageunits Function
$unit = $image->getimageunits();

// Display the output
echo "</br>Units = ";
print_r($unit);
?>
```

发帖主题：Re：Колибри0.7.8.0

```
Units = 2
```

**原图 2：**和

![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54-1.png](img/966bc3ab7c1f4bfcbccb58f1729053cf.png)

**程序 2：**

## PHP

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

// Gmagick function to gets
// units of created image
$res= $im->getimageunits();

// Display the units of image
echo "Units =  ";
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```
Units = 0
```

**引用：**[http://php.net/manual/en/gmagick.getimageunits.php](http://php.net/manual/en/gmagick.getimageunits.php)