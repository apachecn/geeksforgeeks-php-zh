# PHP|Imagick getImageDepth()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagedepth-function/](https://www.geeksforgeeks.org/php-imagick-getimagedepth-function/)

**Imagick：：getImageDepth()**函数是 PHP 中的一个内置函数，用于获取图像的深度。

**语法：**

```php
*int* Imagick::getImageDepth( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回图像深度。

以下程序说明 PHP：
**程序 1：**
**原始图像：**
![](img/efa5ea8e0258291fa60ad9a32c288072.png)中的**Imagick：：getImageDepth()**函数

```php
<?php 

// require_once('vendor/autoload.php');

// Create an Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Use getImageDepth function to calculate image depth

$height = $image->getImageDepth();

// Display the depth of image
print_r($height);
?>
```

发帖主题：Re：Колибри0.7.0

```php
8
```

**程序 2：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54-1.png](img/966bc3ab7c1f4bfcbccb58f1729053cf.png)

```php
<?php 
$string = "Computer Science portal for Geeks!"; 

// creating new image of above String 
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

$dpth = $im->getImageDepth();

// Display the depth of image
print_r($dpth);
?>
```

发帖主题：Re：Колибри0.7.0

```php
8 
```

**引用：**[http://php.net/manual/en/imagick.getimagedepth.php](http://php.net/manual/en/imagick.getimagedepth.php)