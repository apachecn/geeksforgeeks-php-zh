# PHP|Gmagick cyclecolormapimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-cyclecolormapimage-function/](https://www.geeksforgeeks.org/php-gmagick-cyclecolormapimage-function/)

**Gmagick：：cyclecolormapimage()函数**是 PHP 中的一个内置函数，用于将图像色彩映射表置换给定数量的位置。 如果将颜色映射表循环多次，则可以产生迷幻效果。

**语法：**

```
*Gmagick* Gmagick::cyclecolormapimage( *int* $displace )
```

**参数：**此函数接受保存位移的单个参数**$displace**。

**返回值：**此函数成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：cyclecolormapimage()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Apply the cyclecolormapimage() function
$gmagick->cyclecolormapimage(2); 

// Output the image to browser
header('Content-type: image/png');  
echo $gmagick;  
?>  
```

**输出：**
![](img/6cde3584c07ca6930528f84c8db90174.png)

**程序 2：**

```
<?php

// Create a new Gmagick object
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

// Apply the cyclecolormapimage() function
$gmagick->cyclecolormapimage(1); 

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/32ddeed1c7877daa8e493246a9789b17.png)

**引用：**[https://www.php.net/manual/en/gmagick.cyclecolormapimage.php](https://www.php.net/manual/en/gmagick.cyclecolormapimage.php)