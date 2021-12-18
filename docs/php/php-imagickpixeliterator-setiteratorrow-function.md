# PHP|ImagickPixelIterator setIteratorRow()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixeliterator-setiteratorrow-function/](https://www.geeksforgeeks.org/php-imagickpixeliterator-setiteratorrow-function/)

**ImagickPixelIterator：：setIteratorRow()函数**是 PHP 中的内置函数，用于设置像素迭代器行。 此函数用于移动到当前图像像素中的任何行。

**语法：**

```
*bool* ImagickPixelIterator::setIteratorRow( *int* $row )
```

**参数：**此函数接受保存行号的单个参数**$row**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickPixelIterator：：setIteratorRow()函数**：

**程序 1：**

```
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the pixel iterator
$pixelIterator = $imagick->getPixelIterator();

// Set the pixel iterator to 50
$pixelIterator->setIteratorRow(50);

// Get the current iterator row
echo "Current row is " . $pixelIterator->getIteratorRow();
?>
```

发帖主题：Re：Колибри0.7.0

```
Current row is 50
```

**程序 2：**

```
<?php
// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

$imageIterator = $imagick->getPixelIterator();

$x = 0;

while ($x < 250) {
    // Set the iterator row
    $imageIterator->setIteratorRow($x);

    // Get the current row
    $pixels = $imageIterator->getCurrentIteratorRow();

    foreach ($pixels as $pixel) {
        if ($x % 2) {
            // Set the color of pixel
            $pixel->setColor('white');

        } else {
            // Set the color of pixel
            $pixel->setColor('red');

        }
    }
    // Sync the iterator
    $imageIterator->syncIterator();

    // Give a gap of 4 pixels between lines
    $x = $x + 5;
}

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/8bd2efcd22f65247a581ac358f933e1b.png)

**引用：**[https://www.php.net/manual/en/imagickpixeliterator.setiteratorrow.php](https://www.php.net/manual/en/imagickpixeliterator.setiteratorrow.php)