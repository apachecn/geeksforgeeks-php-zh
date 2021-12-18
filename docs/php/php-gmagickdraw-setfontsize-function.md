# PHP|GmagickDraw setfontsize()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-setfontsize-function/](https://www.geeksforgeeks.org/php-gmagickdraw-setfontsize-function/)

Gmagick：：setfontsize()函数是 PHP 中的一个内置函数，用于设置使用文本进行批注时要使用的字体大小。

**语法：**

```php
*public* GmagickDraw::setfontsize( $pointsize ) 
```

参数
**：**此函数接受单个参数*$pointsize*，该参数用于存储字体大小。

**返回值：**此函数在成功时返回 GmagickDraw 对象。

以下程序说明了 PHP 中的*Gmagick：：setfontsize()*函数：

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

//Set the fontsize
$draw->setfontsize(72); 

// Function to draw circle  
$draw->circle(250, 250, 100, 150); 

$gmagick = new Gmagick(); 
$gmagick->newImage(500, 500, 'White'); 
$gmagick->setImageFormat("png"); 
$gmagick->drawImage($draw); 

// Using getfontsize() function
print_r($draw->getfontsize());
?> 
```

发帖主题：Re：Колибри0.7.0

```php
72
```

**程序 2：**

```php
<?php 

// Create a GmagickDraw object 
$draw = new GmagickDraw();  

// Set the color
$draw->setFillColor('Green'); 

// Set the width and height of image 
$draw->setStrokeWidth(1); 

// Function to draw line
for($x = 0; $x < 40; $x++) {
    $draw->line(rand(0, 100), rand(0, 60), rand(0, 500), rand(0, 500));
    $draw->line(rand(0, 100), rand(0, 60), rand(0, 500), rand(0, 500));
    $draw->line(rand(0, 100), rand(0, 60), rand(0, 500), rand(0, 500));
    $draw->line(rand(0, 100), rand(0, 60), rand(0, 500), rand(0, 500));
}

$gmagick = new Gmagick(); 
$gmagick->newImage(500, 500, 'White'); 
$gmagick->setImageFormat("png"); 

// Set the color
$draw->setFillColor('Black'); 

//set Font Size
$draw->setFontSize(25); 

// Use of drawimage function
$gmagick->drawImage($draw); 

$gmagick->annotateImage($draw, 5, 120, 0, 
        'GeeksforGeeks: A computer science portal'); 

// Display the output image 
header("Content-Type: image/png"); 
echo $gmagick->getImageBlob(); 
?> 
```

**输出：**
![](img/bf4af2f2821a08f7382dc4be44d6d42c.png)

**引用：**[http://php.net/manual/en/gmagickdraw.setfontsize.php](http://php.net/manual/en/gmagickdraw.setfontsize.php)