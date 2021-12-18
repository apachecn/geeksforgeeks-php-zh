# PHP|GmagickDraw getstrokeopacity()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-getstrokeopacity-function/](https://www.geeksforgeeks.org/php-gmagickdraw-getstrokeopacity-function/)

Gmagick：：getstrokeopacity()函数是 PHP 中的一个内置函数，用于返回笔划对象轮廓的不透明度。

**语法：**

```
*public* GmagickDraw::getstrokeopacity( void )
```

*
**参数：**此函数不接受任何参数。

**返回值：**此函数返回描述不透明度的双精度。

**错误/异常：**此函数在出错时引发 GmagickException。

以下程序说明了 PHP 中的*Gmagick：：getstrokeopacity()*函数：

**程序 1：**

```
<?php 

// Create a GmagickDraw object 
$draw = new GmagickDraw(); 

// Create GmagickPixel object 
$strokeColor = new GmagickPixel('Red'); 
$fillColor = new GmagickPixel('Green'); 

// Set stroke opacity
$draw->setstrokeopacity(1); 

// Set the width and height of image 
$draw->setStrokeWidth(7); 
$draw->setFontSize(72); 

// Function to draw circle  
$draw->circle(250, 250, 100, 150); 

$gmagick = new Gmagick(); 
$gmagick->newImage(500, 500, 'White'); 
$gmagick->setImageFormat("png"); 
$gmagick->drawImage($draw); 

// Using getstrokeopacity() function

print_r($draw->getstrokeopacity());
?> 
```

发帖主题：Re：Колибри0.7.0

```
1
```

**程序 2：**

```
<?php 

// Create a GmagickDraw object 
$draw = new GmagickDraw();  

// Set the color
$draw->setFillColor('Green'); 

// Set stroke opacity
$draw->setstrokeopacity(0.5);

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

// Set Font Size
$draw->setFontSize(25); 

// Use of drawimage function
$gmagick->drawImage($draw); 
$gmagick->annotateImage($draw, 5, 120, 0, 
        'GeeksforGeeks: A computer science portal'); 

// Display the stroke opacity
echo $draw->getstrokeopacity();

?> 
```

发帖主题：Re：Колибри0.7.0

```
0.49999237048905
```

**引用：**[http://php.net/manual/en/gmagickdraw.getstrokeopacity.php](http://php.net/manual/en/gmagickdraw.getstrokeopacity.php)