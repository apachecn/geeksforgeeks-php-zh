# PHP|Imagick recolorImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-recolorimage-function/](https://www.geeksforgeeks.org/php-imagick-recolorimage-function/)

**Imagick：：recolorImage()**函数是 PHP 中的内置函数，用于平移、缩放、剪切或旋转图像颜色。 此函数用作矩阵大小变量。 通常，RGBA 使用 5×5 矩阵，CMYK 使用 6×6 矩阵。

**语法：**

```php
*bool* Imagick::recolorImage( $matrix )
```

**参数：**此函数接受单个参数*$Matrix*，该参数用于存储颜色矩阵的值。

**返回值：**成功时此函数返回 True。

**原始图像：**
![](img/0503f4823e8dcbdfa50ab25f59045d2a.png)

下面的程序演示了 PHP 中的**Imagick：：recolorImage()**函数：

**程序 1：**

```php
<?php 

// Create new Imagick object
$imagick = new \Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-19.png');

// Color Matrix
$remapColor = [ 1, 0, 0,
                0, 0, 1,
                0, 1, 0, ];

// Recolor the Image
$imagick->recolorImage($remapColor);
header("Content-Type: image/jpg");

// Display the image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/f3cc6917288606cde89fe59cf0dc88ee.png)

**程序 2：**

```php
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

// Recolor the Image
$remapColor = [ 1, 300, 70,
                10, 0, 40,
                10, 10, 0, ];

$im->recolorImage($remapColor);

$im->setImageFormat('jpeg'); 

header("Content-Type: image/jpg"); 

// Display the output image 
echo $im->getImageBlob(); 
?> 
```

**输出：**
![recolor](img/6136d6f1e68338ae7e93cebde56d5743.png)

**引用：**[http://php.net/manual/en/imagick.recolorimage.php](http://php.net/manual/en/imagick.recolorimage.php)