# PHP|Imagick setImageResolution()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageresolution-function/](https://www.geeksforgeeks.org/php-imagick-setimageresolution-function/)

**Imagick：：setImageResolution()**函数是 PHP 中的内置函数，用于设置图像对象的分辨率。
**语法：**和

```php
*bool* Imagick::setImageResolution($x_resolution, $y_resolution)
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x_RESOLUTION：**指定 x 轴分辨率的必选参数。
*   **$y_Resolution：**指定 y 轴分辨率的必选参数。

**返回值：**此函数以数组形式返回分辨率。
下面的程序说明了 PHP：
**原始图像：**和
中的**Imagick：：setImageResolution()**函数

![https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png](img/a377156ca25e3fe93469e179d416418f.png)

**程序 1：**和

## PHP

```php
<?php

$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-15.png');

// Getting Resolution of image
// using getimageresolution function
$res = $imagick->getImageResolution();
echo "X = ".$res['x'] . "</br>";
echo "Y = ".$res['y'] . "</br>";

// Function to set image resolution
$imagick->setImageResolution(50, 50);

echo "After Set Resolution: </br>";

// Getting Resolution of image
// using getimageresolution function
$res = $imagick->getImageResolution();
echo "X = " . $res['x'] . "</br>";
echo "Y = " . $res['y'] . "</br>";
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
X = 37.8
Y = 37.8
After Set Resolution:
X = 50
Y = 50
```

**原图：**

![https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-from-2018-10-16-23-23-54.png](img/583fb2a26e2d28d4d8bbc47a02020896.png)

**程序 2：**和

## PHP

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

$matrix = $im->queryFontMetrics($draw, $string);
$draw->annotation(0, 40, $string);
$im->newImage($matrix['textWidth'], $matrix['textHeight'],
         new ImagickPixel('white'));

// Draw the image         
$im->drawImage($draw);
echo "Before: </br>";

// Getting Resolution of created image
// using getimageresolution function
$res = $im->getImageResolution();
echo "X = ".$res['x'] . "</br>";
echo "Y = ".$res['y'] ." </br>";

// Set image resolution (50, 50)
$im->setImageResolution(50, 50);

echo "After:</br> ";

// Getting Resolution of created image
// using getimageresolution function
$res = $im->getImageResolution();
echo "X = ".$res['x'] . "</br>";
echo "Y = ".$res['y'] ." </br>";
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
Before:
X = 0
Y = 0
After:
X = 50
Y = 50
```

**引用：**[http://php.net/manual/en/imagick.setimageresolution.php](http://php.net/manual/en/imagick.setimageresolution.php)