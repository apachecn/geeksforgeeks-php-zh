# PHP|ImagickPixelIterator getNextIteratorRow()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixeliterator-getnextiteratorrow-function/](https://www.geeksforgeeks.org/php-imagickpixeliterator-getnextiteratorrow-function/)

**ImagickPixelIterator：：getNextIteratorRow()函数**是 PHP 中的一个内置函数，用于从像素迭代器获取下一行像素棒阵列。

**语法：**

```
*array* ImagickPixelIterator::getNextIteratorRow( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含 ImagickPixel 对象的数组值。

下面的程序演示了 PHP 中的**ImagickPixelIterator：：getNextIteratorRow()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
// with 10x10 pixels
$imagick->newImage(10, 10, 'black');

// Get the pixel iterator
$imageIterator = $imagick->getPixelIterator();

// Rows counter variable
$rows = 0;

// Count the number of rows
while ($pixels = $imageIterator->getNextIteratorRow()) {
    $rows++;
}

echo 'The number of rows are ' . $rows;
?>
```

发帖主题：Re：Колибри0.7.0

```
The number of rows are 10
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Get the pixel iterator
$imageIterator = $imagick->getPixelIterator();

while ($pixels = $imageIterator->getNextIteratorRow()) {
    foreach ($pixels as $column => $pixel) {
        if ($column % 20) {

            // Paint every 20th pixel black in each row
            $pixel->setColor("white");
        }
    }

    // Sync the iterator
    $imageIterator->syncIterator();
}

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/4d9ca2f2b161727baffb1b700c7fd19b.png)

**引用：**[https://www.php.net/manual/en/imagickpixeliterator.getnextiteratorrow.php](https://www.php.net/manual/en/imagickpixeliterator.getnextiteratorrow.php)