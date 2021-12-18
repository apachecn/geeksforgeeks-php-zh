# PHP|Gmagick trimimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-trimimage-function/](https://www.geeksforgeeks.org/php-gmagick-trimimage-function/)

**Gmagick：：trimimage()函数**是 PHP 中的一个内置函数，用于从图像中删除作为背景颜色的边缘。

**语法：**

```php
*Gmagick* Gmagick::trimimage( *float* $fuzz )
```

**参数：**此函数接受保存模糊的单个参数**$fuzz**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：trimimage()函数**：

**程序-1(裁切图像)：**

```php
<?php
// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Trim the image
$gmagick->trimimage(10);

// Output the image  
header('Content-type: image/png');  
echo $gmagick;  
?>
```

**输出：**
![](img/df23d391550ada422b149452d95ffbac.png)

**程序-2(修剪图纸)：**

```php
<?php
// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the color
$draw->setFillColor('white');

// Function to draw rectangle
$draw->rectangle(0, 0, 800, 400);

// Set the fill color
$draw->setFillColor('red');

// Set the font size
$draw->setfontsize(50);

// Annotate a text
$draw->annotate(30, 100, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Trim the image
$gmagick->trimimage(10); 

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/69cea3ed1f9ff86aa112ad54f5658f62.png)

**引用：**[https://www.php.net/manual/en/gmagick.trimimage.php](https://www.php.net/manual/en/gmagick.trimimage.php)