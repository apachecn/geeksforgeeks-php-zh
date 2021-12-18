# PHP|Gmagick setimageBluepriary()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimageblueprimary-function/](https://www.geeksforgeeks.org/php-gmagick-setimageblueprimary-function/)

**gmagick：：setimageBluepriary()**函数是 PHP 中的一个内置函数，用于设置特定图像通道的深度。

**语法：**

```
*Gmagick* Gmagick::setimageblueprimary( $x, $y )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x：**它指定蓝色主 x 点。
*   **$y：**它指定蓝色主要 y 点。

**返回值：**此函数返回一个包含点的 x 和 y 坐标的数组。

下面的程序说明了 PHP 中的**Gmagick：：setimageBluepriary()**函数：

**程序 1：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

```
<?php

// Create new Gmagick object
$Gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using getImageBluePrimary function
echo "Before Set Blue Primary: ";
$res = $Gmagick->getImageBluePrimary();
print_r($res);

// Set blue primary point
$Gmagick->setImageBluePrimary( 1.765, 2.5698 );

echo "</br>  After Set Blue Primary: ";
$res = $Gmagick->getImageBluePrimary();

print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```
Before Set Blue Primary: Array ( [x] => 0.15000000596046 [y] => 
0.059999998658895 )
After Set Blue Primary: Array ( [x] => 1.765 [y] => 2.5698 ) 

```

**程序 2：**
**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

```
<?php 

$string = "Computer Science portal for Geeks!"; 

// Creating new image of above String 
// and add color  
$im = new Gmagick(); 
$draw = new GmagickDraw(); 

// Fill the color in image 
$draw->setFillColor(new GmagickPixel('green')); 

// Set the text font size 
$draw->setFontSize(50); 

$metrix = $im->queryFontMetrics($draw, $string); 
$draw->annotation(0, 40, $string); 
$im->newImage($metrix['textWidth'], $metrix['textHeight'], 
        new GmagickPixel('white')); 

// Draw the image         
$im->drawImage($draw); 
$im->setImageFormat('jpeg'); 

// Using getImageBluePrimary function
echo "Before Set Blue Primary: ";
$res = $im->getImageBluePrimary();
print_r($res);

// Set blue primary point
$im->setImageBluePrimary(20.765, 14.1698);

echo "</br>  After Set Blue Primary: ";
$res = $im->getImageBluePrimary();
print_r($res);
?>
```

发帖主题：Re：Колибри0.7.0

```
Before Set Blue Primary: Array ( [x] => 0.15000000596046 [y] => 
0.059999998658895 )
After Set Blue Primary: Array ( [x] => 20.765 [y] => 14.1698 ) 

```

**引用：**[http://php.net/manual/en/gmagick.setimageblueprimary.php](http://php.net/manual/en/gmagick.setimageblueprimary.php)