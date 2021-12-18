# PHP|Imagick displayImages()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-displayimages-function/](https://www.geeksforgeeks.org/php-imagick-displayimages-function/)

**Imagick：：displayImages()函数**是 PHP 中的内置函数，用于在 X 服务器上显示图像或图像序列。

**语法：**

```
*bool* Imagick::displayImages( *string* $servername )
```

**参数：**此函数接受保存 X 服务器名称的单个参数**$servername**。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的 Imagick：：displayImages()函数：

**程序 1：**

```
<?php 

// Create an Imagick object 
$imagick = new Imagick( 
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png'); 

// Use displayImage function 
$imagick->displayImage('servername'); 

header("Content-Type: image/jpg"); 

// Display the output image 
echo $imagick->getImageBlob(); 
?> 
```

**输出：**
![imagick::displayImages](img/c056e7024c421beded61007c4e1078bf.png)

**程序 2：**

```
<?php 

$string = "Computer Science portal for Geeks!"; 

// Creating new image of above String 
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

// Use displayImage function 
$im->displayImage('servername'); 

$im->setImageFormat('png'); 

header("Content-Type: image/jpg"); 

// Display the output image 
echo $im->getImageBlob(); 
?> 
```

**输出：**
![imagick::displayImages](img/3da072002edf43cdb7bab01a6d771bbd.png)

**引用：**[https://www.php.net/manual/en/imagick.displayimages.php](https://www.php.net/manual/en/imagick.displayimages.php)