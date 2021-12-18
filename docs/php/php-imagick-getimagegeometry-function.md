# PHP|Imagick getImageGeometry()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagegeometry-function/](https://www.geeksforgeeks.org/php-imagick-getimagegeometry-function/)

**Imagick：：getImageGeometry()**函数是 PHP 中的一个内置函数，用于以关联数组的形式获取宽度和高度。

**语法：**

```php
*array* Imagick::getImageGeometry( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数以关联数组的形式返回宽度和高度。
**错误/异常：**此函数在出错时抛出 ImagickException。

下面的程序说明 PHP：
**程序 1：**
**原始图像：**
![](img/efa5ea8e0258291fa60ad9a32c288072.png)中的**Imagick：：getImageGeometry()**函数

```php
<?php 
// require_once('path/vendor/autoload.php');

// Create an Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Use getImageHeight function to 
// calculate image height
$res= $image->getImageGeometry();

// Display the width and height of image
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array ( [width] => 667 [height] => 184 ) 
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

$res= $im->getImageGeometry();

// Display the width and height of image
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array ( [width] => 798 [height] => 62 ) 
```

**引用：**[http://php.net/manual/en/imagick.getimagegeometry.php](http://php.net/manual/en/imagick.getimagegeometry.php)