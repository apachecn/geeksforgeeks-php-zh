# PHP|ImagickDraw Composite()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-composite-function/](https://www.geeksforgeeks.org/php-imagickdraw-composite-function/)

**ImagickDraw：：Compose()函数**是 PHP 中的一个内置函数，用于使用指定的合成操作符、指定的位置和指定的大小将图像合成到当前图像中。

**语法：**

```
*bool* ImagickDraw::compose( *int* $compose, *float* $x, *float* $y,
           *float* $width, *float* $height, *Imagick* $compositeWand )
```

**参数：**此函数接受上述 6 个参数，如下所述：

*   **$compose：**它指定对应于[个复合常量](https://www.php.net/manual/en/imagick.constants.php/#imagick.constants.composite-default)的复合运算符。
*   **$x：**它指定左上角的 y 坐标。
*   **$y：**它指定左上角的 x 坐标。
*   **$width：**它指定合成图像的宽度。
*   **$Height：**它指定合成图像的高度。
*   **$CompositeWand：**它指定从中获取合成图像的 Imagick 对象。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickDraw：：Compose()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Composite the Image
$draw->composite(imagick::COMPOSITE_COLORIZE,
                   100, 100, 200, 200, $imagick);

// Create a new Imagick object
$imagick2 = new Imagick();

// Create a image on imagick object
$imagick2->newImage(800, 250, 'white');

// Render the draw commands
$imagick2->drawImage($draw);

// Add border
$imagick->borderImage('green', 1, 1);

// Show the output
$imagick2->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick2->getImageBlob();
?>
```

**输出：**
![](img/757d759583b33538640cd998e3b87276.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Composite the Image
$draw->composite(4, 200, 20, 400, 200, $imagick);

// Create a new Imagick object
$imagick2 = new Imagick();

// Create a image on imagick object
$imagick2->newImage(800, 250, 'orange');

// Render the draw commands
$imagick2->drawImage($draw);

// Show the output
$imagick2->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick2->getImageBlob();
?>
```

**输出：**
![](img/74c4cb8e71ec27d814a6ffb2d95352db.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.composite.php](https://www.php.net/manual/en/imagickdraw.composite.php)