# PHP|GmagickPixel setcolor()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickpixel-setcolor-function/](https://www.geeksforgeeks.org/php-gmagickpixel-setcolor-function/)

**GmagickPixel：：setcolor()函数**是 PHP 中的一个内置函数，用于设置 GmagickPixel 对象的颜色。

**语法：**

```php
*GmagickPixel* GmagickPixel::setcolor( *string* $color )
```

**参数：**此函数接受保存颜色的单个参数**$color**。

**返回值：**此函数成功时返回 GmagickPixel 对象。

**异常：**此函数在出错时引发 GmagickPixelException。

下面给出的程序说明了 PHP：
**程序 1：**中的**GmagickPixel：：setcolor()函数**

```php
<?php 
// Create a new gmagickPixel object 
$gmagickPixel = new GmagickPixel(); 

// Set the color 
$gmagickPixel->setColor('#428554'); 

// Get the color 
$color = $gmagickPixel->getColor(); 
print("<pre>".print_r($color, true)."</pre>"); 
?> 
```

发帖主题：Re：Колибри0.7.0

```php
rgb(16962, 34181, 21588)
```

**程序 2：**

```php
<?php
// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a new GmagickPixel object
$gmagickPixel = new GmagickPixel();

// Set the color
$gmagickPixel->setcolor('blue');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set fill color using gmagickpixel
$draw->setfillcolor($gmagickPixel);

// Set the font size
$draw->setfontsize(40);

// Annotate a text
$draw->annotate(50, 180, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/80bdc9b00f651c94770a81fa58e800c5.png)

**引用：**[https://www.php.net/manual/en/gmagickpixel.setcolor.php](https://www.php.net/manual/en/gmagickpixel.setcolor.php)