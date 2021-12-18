# PHP|Gmagick setimageDeep()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimagedepth-function/](https://www.geeksforgeeks.org/php-gmagick-setimagedepth-function/)

**gmagick：：setimageDeep()**函数是 PHP 中的一个内置函数，用于设置特定图像的深度。

**语法：**

```php
*Gmagick* Gmagick::setimagedepth( $depth )
```

**参数：**此函数接受单个参数*$Depth*，该参数是一个整数值，用于设置图像的深度。

**返回值：**此函数在成功时返回 Gmagick 对象。

下面的程序说明了 PHP 中的**Gmagick：：setimageDeep()**函数：

**程序 1：**
**原始图像：**
![](img/efa5ea8e0258291fa60ad9a32c288072.png)

```php
<?php 

// require_once('path/vendor/autoload.php');

// Create an Gmagick Object
$image = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Use getImageDepth function to find the depth 
// of image
$res= $image->getImageDepth();

// Display the depth of image
echo "Previous Depth: " . $res; 

$image->setimagedepth(16);

$res = $image->getImageDepth();
echo "</br>After Set the Depth: " . $res; 
?>
```

发帖主题：Re：Колибри0.7.0

```php
Previous Depth: 8
After Set the Depth: 16

```

**程序 2：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54-1.png](img/966bc3ab7c1f4bfcbccb58f1729053cf.png)

```php
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

$dpth = $im->getImageDepth();

// Display the depth of image
print("Previous Depth = " . $dpth);

$im->setimagedepth(32);
$dpthnew = $im->getImageDepth();

// Display the depth of image
print("</br>Depth After Set  = " . $dpthnew);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Previous Depth = 8
Depth After Set = 32

```

**引用：**[http://php.net/manual/en/gmagick.setimagedepth.php](http://php.net/manual/en/gmagick.setimagedepth.php)