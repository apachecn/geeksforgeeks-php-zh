# PHP|ImagickPixelIterator newPixelIterator()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixeliterator-newpixeliterator-function/](https://www.geeksforgeeks.org/php-imagickpixeliterator-newpixeliterator-function/)

**ImagickPixelIterator：：newPixelIterator()函数**是 PHP 中的内置函数，用于获取新的像素迭代器来迭代图像的像素。

**语法：**

```
*bool* ImagickPixelIterator::newPixelIterator( *Imagick* $wand )
```

**参数：**此函数接受单个参数**$wand**，该参数保存图像以迭代像素。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickPixelIterator：：newPixelIterator()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new ImagickPixelIterator instance
$imageIterator = new ImagickPixelIterator();

// Get the pixels from the image
$imageIterator->newPixelIterator($imagick);

$i = 0;

// Loop through pixel rows
foreach ($imageIterator as $row => $pixels) {
    $i++;
}

echo 'Total rows are ' . $i;
?>
```

发帖主题：Re：Колибри0.7.0

```
Total rows are 250
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new ImagickPixelIterator instance
$imageIterator = new ImagickPixelIterator();

// Get the pixels from the image
$imageIterator->newPixelIterator($imagick);

$colors = ['red', 'green', 'blue', 'yellow'];
$i = 0;

// Loop through pixel rows
foreach ($imageIterator as $row => $pixels) {

    foreach ($pixels as $column => $pixel) {

        // Set the color of each pixel lines to colors
        $pixel->setColor($colors[$i % 4]);
    }
    $i++;

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
![](img/d9e01c9cd8b561a138d7ef9988a2d3cc.png)

**引用：**[https://www.php.net/manual/en/imagickpixeliterator.newpixeliterator.php](https://www.php.net/manual/en/imagickpixeliterator.newpixeliterator.php)