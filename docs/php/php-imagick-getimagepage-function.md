# PHP|Imagick getImagePage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagepage-function/](https://www.geeksforgeeks.org/php-imagick-getimagepage-function/)

**Imagick：：getImagePage()**函数是 PHP 中的一个内置函数，用于获取特定图像的页面几何形状。

**语法：**

```php
*array* Imagick::getImagePage( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个与页面几何关联的数组，其中包含键值*width、Height、x、*和*y*。

下面的程序演示了 PHP 中的**Imagick：：getImagePage()**函数：

**程序 1：**
**原始图像：**
![](img/efa5ea8e0258291fa60ad9a32c288072.png)

```php
<?php 

// require_once('path/vendor/autoload.php');

// Create an Imagick Object
$image = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Use getImagePage function to find the page 
// of image
$res = $image->getImagePage();

// Display the result
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array ( [width] => 667 [height] => 184 [x] => 0 [y] => 0 ) 

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

// getImagePage function to find the page 
// of image
$res = $im->getImagePage();

// display result
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array ( [width] => 0 [height] => 0 [x] => 0 [y] => 0 ) 

```

**引用：**[http://php.net/manual/en/imagick.getimagepage.php](http://php.net/manual/en/imagick.getimagepage.php)