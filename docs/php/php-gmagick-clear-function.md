# PHP|Gmagick clear()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-clear-function/](https://www.geeksforgeeks.org/php-gmagick-clear-function/)

**Gmagick：：Clear()**函数是 PHP 中的一个内置函数，用于清除与 Gmagick 对象关联的所有资源。

**语法：**

```php
*Gmagick* Gmagick::clear( void )
```

*
**参数：**此函数不接受任何参数。

**返回值：**此函数返回清除的 Gmagick 对象。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的**Gmagick：：Clear()**函数：

**程序 1：**

```php
<?php 

// Create a GmagickDraw object 
$draw = new GmagickDraw(); 

// Create GmagickPixel object 
$fillColor = new GmagickPixel('Green'); 

// Set stroke opacity
$draw->setfillcolor('red');

// Set the width and height of image 
$draw->setStrokeWidth(7); 
$draw->setFontSize(72); 

// Function to draw circle  
$draw->circle(250, 250, 100, 150); 

$gmagick = new Gmagick(); 
$gmagick->newImage(500, 500, 'White'); 
$gmagick->setImageFormat("png"); 
$gmagick->drawImage($draw); 

// Using clear() function
print_r($gmagick->clear());
?> 
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**程序 2：**

```php
<?php 

// Create a GmagickDraw object 
$draw = new ImagickDraw();  

// Set the color
$draw->setFillColor('Green'); 

// Set the width and height of image 
$draw->setStrokeWidth(17); 

// Function to draw line
for($x = 0; $x < 40; $x++) {
    $draw->line(rand(0, 100), rand(0, 60), rand(0, 500), rand(0, 500));
    $draw->line(rand(0, 100), rand(0, 60), rand(0, 500), rand(0, 500));
    $draw->line(rand(0, 100), rand(0, 60), rand(0, 500), rand(0, 500));
    $draw->line(rand(0, 100), rand(0, 60), rand(0, 500), rand(0, 500));
}

$gmagick = new Imagick(); 
$gmagick->newImage(500, 500, 'White'); 
$gmagick->setImageFormat("png"); 

// Set the color
$draw->setFillColor('Black'); 

// Set Font Size
$draw->setFontSize(20); 

// Use of drawimage function
$gmagick->drawImage($draw); 

$gmagick->annotateImage($draw, 5, 220, 0, 
     'Stroke Width using getstrokewidth() function :'
                        . $draw->getstrokewidth());

// Using clear() function
print_r($gmagick->clear());
?> 
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**引用：**[http://php.net/manual/en/gmagick.clear.php](http://php.net/manual/en/gmagick.clear.php)