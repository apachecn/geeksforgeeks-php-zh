# PHP|Imagick drawImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-drawimage-function/](https://www.geeksforgeeks.org/php-imagick-drawimage-function/)

Imagick：：drawImage()函数是 PHP 中的一个内置函数，用于在 Imagick 对象上呈现 ImagickDraw 对象。 用于在 Imagick 实例上绘制图像。 我们借助 ImagickDraw 方法设置图像矩阵、参数和绘制图像的边界，然后使用 Imagick：：DrawImage()函数呈现它。

**语法：**

```php
*bool* Imagick::drawImage( ImagickDraw $draw )
```

**参数：**此函数接受单个参数**$Draw**，该参数保存 ImagickDraw 实例以获取有关要在屏幕上呈现的图像的详细信息。

**返回值：**执行成功时返回值为 True。

**程序：**此程序创建一个图像，设置其尺寸和边框属性，然后在屏幕上渲染。

```php
<?php 

// Declare a string which to be drawn 
$geek = "GeeksforGeeks"; 

// Declare an Imagick object
$image = new Imagick();

// Declare an ImagickDraw object
$draw = new ImagickDraw(); 

// Set the color of Imagickdraw object
$draw->setFillColor(new ImagickPixel('Green')); 

// Set the font size of text
$draw->setFontSize(120); 

// Array representing the font metrics
$metrix = $image->queryFontMetrics($draw, $geek); 

// Set the position of text with respect
// to the border 
$draw->annotation(0, 100, $geek); 

// Create image of given size
$image->newImage(875, 150, new ImagickPixel('white')); 

// Use drawImage() function to draw the image
$image->drawImage($draw); 

// Set the border of image
$image->borderImage(new ImagickPixel('green'), 5, 5); 

// Set the image format
$image->setImageFormat('png'); 

header('Content-type: image/png');

// Display the image
echo $image;

?>
```

**输出：**
![](img/6566e28ac84a7ab747b4b21eb2dd614e.png)

**引用：**[https://www.php.net/manual/en/imagick.drawimage.php](https://www.php.net/manual/en/imagick.drawimage.php)