# PHP|Gmagick getimageformat()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimageformat-function/](https://www.geeksforgeeks.org/php-gmagick-getimageformat-function/)

**gmagick：：getimageformat()**函数是 PHP 中的一个内置函数，它返回图像的格式。

**语法：**

```php
*string* Gmagick::getimageformat( void )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数以字符串的形式返回图片格式。

下面的程序演示了 PHP 中的**Gmagick：：getimageformat()**函数：

**原图 1：**
![](img/efa5ea8e0258291fa60ad9a32c288072.png)
**程序 1：**

```php
<?php 
// require_once('path/vendor/autoload.php');

// Create an Gmagick Object
$image = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Use getimageformat function to find the 
// formats of image

$res = $image->getimageformat();

// Display the format sequence of image
echo $res; 
?>
```

发帖主题：Re：Колибри0.7.0

```php
PNG
```

**原始图像 2：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54-1.png](img/966bc3ab7c1f4bfcbccb58f1729053cf.png)

**程序 2：**

```php
<?php
$string = "Computer Science portal for Geeks!";

// creating new image of above String 
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

// Gmagick function to get format of created image
$res= $im->getimageformat();

// Display the format of image
echo $res;
?>
```

发帖主题：Re：Колибри0.7.0

```php
jpeg
```

**引用：**[http://php.net/manual/en/gmagick.getimageformat.php](http://php.net/manual/en/gmagick.getimageformat.php)