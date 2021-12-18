# PHP|Gmagick getrelease asedate()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getreleasedate-function/](https://www.geeksforgeeks.org/php-gmagick-getreleasedate-function/)

**Gmagick：：getRelease asedate()**函数是 PHP 中的一个内置函数，用于以字符串形式返回 GraphicsMagick 发布日期。

**语法：**

```
*string* Gmagick::getreleasedate( void )
```

*
**参数：**此函数不接受任何参数。

**返回值：**此函数以字符串形式返回 GraphicsMagick 发布日期。

**错误/异常：**此函数在出错时引发 GmagickException。

下面的程序说明了 PHP 中的**Gmagick：：getRelease asedate()**函数：

**程序 1：**

```
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// Using getreleasedate() function

print_r($gmagick->getreleasedate());
?>
```

发帖主题：Re：Колибри0.7.0

```
2017-05-23
```

**程序 2：**

```
<?php 

// Create a GmagickDraw object 
$draw = new GmagickDraw(); 

// Create GmagickPixel object 
$strokeColor = new GmagickPixel('Red'); 
$fillColor = new GmagickPixel('Green'); 

// Set the color, opacity of image 
$draw->setStrokeOpacity(1); 
$draw->setStrokeColor('Red'); 
$draw->setFillColor('Green'); 

// Set the width and height of image 
$draw->setStrokeWidth(7); 
$draw->setFontSize(72); 

// Function to draw circle  
$draw->circle(250, 250, 100, 150); 

$gmagick = new Gmagick(); 
$gmagick->newImage(500, 500, 'White'); 
$gmagick->setImageFormat("png"); 
$gmagick->drawImage($draw); 

// Using getreleasedate() function

print_r($gmagick->getreleasedate());
?> 
```

发帖主题：Re：Колибри0.7.0

```
2017-05-23
```

**引用：**[http://php.net/manual/en/gmagick.getreleasedate.php](http://php.net/manual/en/gmagick.getreleasedate.php)