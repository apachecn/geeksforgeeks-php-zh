# PHP|Imagick getPixelRegionIterator()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getpixelregioniterator-function/](https://www.geeksforgeeks.org/php-imagick-getpixelregioniterator-function/)

**Imagick：：getPixelRegionIterator()函数**是 PHP 中的内置函数，用于获取图像节的 ImagickPixelIterator。

**语法：**

```
*ImagickPixelIterator* Imagick::getPixelRegionIterator( *int* $x, *int* $y, *int* $columns, *int* $rows )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$x：**它指定区域的 x 坐标。
*   **$y：**它指定区域的 y 坐标。
*   **$Columns：**它指定区域的宽度。
*   **$ROWS：**它指定区域的高度。

**返回值：**此函数返回图像节的 ImagickPixelIterator。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getPixelRegionIterator()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

$imageIterator = $imagick->getPixelRegionIterator(0, 0, 330, 200);

// Change the color of every second pixel of region to blue
foreach ($imageIterator as $row => $pixels) {
    foreach ($pixels as $column => $pixel) {
        if ($column % 2) {
            $pixel->setColor("blue");
        }
    }
    $imageIterator->syncIterator();
}

// Display the output
header("Content-Type:image/png");
echo $imagick;
?>
```

**输出：**
![](img/572f21285fa461b06b748627873cc784.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

$imageIterator = $imagick->getPixelRegionIterator(330, 0, 338, 200);

// Change the color of every second pixel of region to green
foreach ($imageIterator as $row => $pixels) {
    foreach ($pixels as $column => $pixel) {
        if ($column % 2) {
            $pixel->setColor("green");
        }
    }
    $imageIterator->syncIterator();
}

// Display the output
header("Content-Type:image/png");
echo $imagick;
?>
```

**输出：**
![](img/352b0d14cf6c41c3755f122ef32ab98e.png)

**引用：**[https://www.php.net/manual/en/imagick.getpixelregioniterator.php](https://www.php.net/manual/en/imagick.getpixelregioniterator.php)