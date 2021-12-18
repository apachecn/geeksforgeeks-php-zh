# PHP|ImagickPixelIterator newPixelRegionIterator()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixeliterator-newpixelregioniterator-function/](https://www.geeksforgeeks.org/php-imagickpixeliterator-newpixelregioniterator-function/)

**ImagickPixelIterator：：newPixelRegionIterator()函数**是 php 中的一个内置函数，用于从 Imagick 棒中的特定区域获取新的像素迭代器。

**语法：**

```
*bool* ImagickPixelIterator::newPixelRegionIterator( *Imagick* $wand,
         *int* $x, *int* $y, *int* $columns, *int* $rows )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$wand：**它指定想象棒。
*   **$x：**它指定 x 坐标。
*   **$y：**它指定 y 坐标。
*   **$Columns：**它指定列数。
*   **$ROWS：**它指定行数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 php 中的**ImagickPixelIterator：：newPixelRegionIterator()函数**：

**程序 1：**此程序在空白图像上绘制正方形。

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new ImagickPixelIterator instance
$imageIterator = new ImagickPixelIterator();

// Get the pixels from a image region
$imageIterator->newPixelRegionIterator($imagick, 40, 30, 200, 200);

// Loop through pixel rows
foreach ($imageIterator as $row => $pixels) {

    foreach ($pixels as $column => $pixel) {

        // Set the color of each pixel
        $pixel->setColor('red');
    }

    // Sync the iterator after each iteration
    $imageIterator->syncIterator();
}

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/f7c13b1779d4721556c78a386e68f09a.png)

**程序 2：**此程序在 PNG 图像上绘制一个矩形。

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Create a new ImagickPixelIterator instance
$imageIterator = new ImagickPixelIterator();

// Get the pixels from a image region
$imageIterator->newPixelRegionIterator($imagick, 40, 100, 1200, 20);

// Loop through pixel rows
foreach ($imageIterator as $row => $pixels) {

    foreach ($pixels as $column => $pixel) {

        // Set the color of each pixel
        $pixel->setColor('#62AC45');
    }

    // Sync the iterator after each iteration
    $imageIterator->syncIterator();
}

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/02644806543f4763808cb875020fe956.png)

**引用：**[https://www.php.net/manual/en/imagickpixeliterator.newpixelregioniterator.php](https://www.php.net/manual/en/imagickpixeliterator.newpixelregioniterator.php)