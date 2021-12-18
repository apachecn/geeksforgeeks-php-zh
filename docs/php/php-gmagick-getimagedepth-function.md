# PHP|Gmagick getimageDeep()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimagedepth-function/](https://www.geeksforgeeks.org/php-gmagick-getimagedepth-function/)

**gmagick：：getimageDeep()**函数是 PHP 中的一个内置函数，用于获取图像的深度。

**语法：**

```
*int* Gmagick::getimagedepth( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回图像的深度。

下面的程序说明了 PHP 中的**Gmagick：：getimageDeep()**函数：

**原始图像 1：**
![](img/efa5ea8e0258291fa60ad9a32c288072.png)

**程序 1：**

```
<?php 

// require_once('vendor/autoload.php');

// Create an Gmagick Object
$image = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Use getimagedepth function to calculate image depth

$height = $image->getimagedepth();

// Display the depth of image
print_r($height);
?>
```

发帖主题：Re：Колибри0.7.0

```
8
```

**原始图像 2：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54-1.png](img/966bc3ab7c1f4bfcbccb58f1729053cf.png)

**程序 2：**

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

$im->setImageFormat('jpeg');

$dpth = $im->getimagedepth();

// Display the depth of image
print_r($dpth);
?>
```

发帖主题：Re：Колибри0.7.0

```
8 
```

**引用：**[http://php.net/manual/en/gmagick.getimagedepth.php](http://php.net/manual/en/gmagick.getimagedepth.php)