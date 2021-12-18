# PHP|Imagick setImageOpacity()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageopacity-function/](https://www.geeksforgeeks.org/php-imagick-setimageopacity-function/)

**Imagick：：setImageOpacity()**函数是 PHP 中的内置函数，用于设置 Imagick 对象的不透明度级别。 ImageMagick 6.3.1 或更高版本中提供了此方法。

**语法：**

```
*bool* Imagick::setImageOpacity( $opct )
```

**参数：**此函数接受单个参数*$opct*，该参数指定要设置的 Imagick 对象的不透明度。

**返回值：**成功时此函数返回 True。

以下程序说明了 PHP 中的**Imagick：：setImageOpacity()**函数：

**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

**程序 1：**

```
<?php

// Create new Imagick object
$im = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Using setImageOpacity function
$im->setImageOpacity(0.3);

// Display result
header("Content-Type: image/jpg");
echo $im->getImageBlob();

?>
```

**输出：**
![https://media.geeksforgeeks.org/wp-content/uploads/set_opacity_gfg_imagick.png](img/00c47fad4229094fa79cba33ee27a7d2.png)

**原始图像：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**程序 2：**

```
<?php 

$string = "Computer Science portal for Geeks!"; 

// Creating new image of above String 
// and add color
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
$im->setImageFormat('jpeg'); 

// Using setImageOpacity function
$im->setImageOpacity(0.9);

header("Content-Type: image/jpg");
echo $im->getImageBlob();
?>
```

**输出：**
![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**引用：**[http://php.net/manual/en/imagick.setimageopacity.php](http://php.net/manual/en/imagick.setimageopacity.php)