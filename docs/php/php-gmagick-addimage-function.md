# PHP|Gmagick addImage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-addimage-function/](https://www.geeksforgeeks.org/php-gmagick-addimage-function/)

**Gmagick：：addImage()**函数是 PHP 中的一个内置函数，用于将新图像添加到 Gmagick 对象图像列表。 此函数用于从源对象的当前位置向 Gmagick 对象添加新图像。 Gmagick 类能够同时保存和操作多个图像。

**语法：**

```php
*bool* Gmagick::addImage( $source )
```

**参数：**此函数接受保存源 Gmagick 对象的单个参数*$source*。

**返回值：**此函数成功时返回 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

下面的程序演示了 PHP 中的**Gmagick：：addImage()**函数：

**原始图像 1：**
![adpative threshold image](img/92655fac130f4772488bfafcfb48fc6d.png)

**程序：**

```php
<?php 

// require_once('path/to/vendor/autoload.php');

header('Content-type: image/png');

$image = new Gmagick (
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

$t = new Gmagick (
'https://media.geeksforgeeks.org/wp-content/uploads/adaptiveThresholdImage.png');

$image->addImage($t);

echo $image;
?>
```

**Output:**![adaptive threshold image](img/92655fac130f4772488bfafcfb48fc6d.png)

**原始图像 2：**
![original image](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**程序 2：**

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

$t = new Gmagick (
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

$im->addImage($t);

header("Content-Type: image/jpg"); 
echo $im->getImageBlob(); 
?> 
```

**输出：**
![](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**引用：**[http://php.net/manual/en/gmagick.addimage.php](http://php.net/manual/en/gmagick.addimage.php)