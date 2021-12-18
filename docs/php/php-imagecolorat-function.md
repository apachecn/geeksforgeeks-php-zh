# PHP|imagecolorat()函数

> Original: [https://www.geeksforgeeks.org/php-imagecolorat-function/](https://www.geeksforgeeks.org/php-imagecolorat-function/)

**imagecolorat()**函数是 PHP 中的一个内置函数，用于获取像素颜色的索引。 此函数用于返回指定位置的像素值。
**语法：**和

```php
*int* imagecolorat( $image, $x, $y )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$image：**imagecreatetruecolor()函数用于创建给定大小的图像。
*   **$x：**此参数用于保存点的 x 坐标。
*   **$y：**此参数用于保存点的 y 坐标。

**返回值：**此函数返回颜色索引(颜色像素值)，失败时返回 False。
下面的程序演示了 PHP 中的**imagecolorat()**函数。
**注意：**下面给出的图像用于以下程序。

![geeks image](img/c6e0a168008bc4a43314f9fb895e5c7c.png)

**程序 1：**和

## PHP

```php
<?php

// store the image in variable
$image = imagecreatefrompng("gfg.png");

// Calculate rgb pixel value at particular point.
$rgb = imagecolorat($image, 30, 25);
$red = ($rgb >> 16) & 255;
$green = ($rgb >> 8) & 255;
$blue = $rgb & 255;

var_dump($red, $green, $blue);
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
int(34) 
int(170) 
int(66)
```

**程序 2：**和

## PHP

```php
<?php

// store the image in variable.
$image = imagecreatefrompng("gfg.png");

// Calculate rgb pixel value at particular point.
$rgb = imagecolorat($image, 30, 25);

// Assign color name and its value.
$colors = imagecolorsforindex($image, $rgb);

var_dump($colors);
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
array(4) { 
    ["red"]=> int(34) 
    ["green"]=> int(170) 
    ["blue"]=> int(66) 
    ["alpha"]=> int(0) 
}
```

**引用：**[http://php.net/manual/en/function.imagecolorat.php](http://php.net/manual/en/function.imagecolorat.php)