# PHP|Gmagick getversion()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getversion-function/](https://www.geeksforgeeks.org/php-gmagick-getversion-function/)

**Gmagick：：getversion()**函数是 PHP 中的内置函数，用于返回 Gmagick API 版本。

**语法：**

```php
*array* Gmagick::getversion( void )
```

*
**参数：**此函数不接受任何参数。

**返回值：**此函数返回 Gmagick API 版本。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的**Gmagick：：getversion()**函数：

**程序 1：**

```php
<?php 

// Create a Gmagick object 
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png'); 

// Using getversion() function
print_r($gmagick->getversion());
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array ( 
    [versionNumber] => 2168833 
    [versionString] => 
    GraphicsMagick 1.4 snapshot-20180922 Q16 
    http://www.GraphicsMagick.org/ 
)

```

**程序 2：**

```php
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

// Using getversion() function

print_r($gmagick->getversion());
?> 
```

发帖主题：Re：Колибри0.7.0

```php
Array ( 
    [versionNumber] => 2168833 
    [versionString] => 
    GraphicsMagick 1.4 snapshot-20180922 Q16 
    http://www.GraphicsMagick.org/ 
)
```

**引用：**[http://php.net/manual/en/gmagick.getversion.php](http://php.net/manual/en/gmagick.getversion.php)