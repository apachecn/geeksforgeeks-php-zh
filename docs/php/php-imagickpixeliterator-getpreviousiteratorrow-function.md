# PHP|ImagickPixelIterator getPreviousIteratorRow()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixeliterator-getpreviousiteratorrow-function/](https://www.geeksforgeeks.org/php-imagickpixeliterator-getpreviousiteratorrow-function/)

**ImagickPixelIterator：：getPreviousIteratorRow()函数**是 php 中的一个内置函数，用于从像素迭代器获取作为像素棒数组的前一行。

**语法：**

```php
*array* ImagickPixelIterator::getPreviousIteratorRow( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含 ImagickPixel 对象的数组值。

下面的程序演示了 php 中的**ImagickPixelIterator：：getPreviousIteratorRow()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the pixel iterator
$pixelIterator = $imagick->getPixelIterator();

// Set the pixel iterator to 50
$pixelIterator->setIteratorRow(50);

// Move one step to previous row
$pixelIterator->getPreviousIteratorRow();

// Get the current iterator row
echo "Current row is " . $pixelIterator->getIteratorRow();
?>
```

发帖主题：Re：Колибри0.7.0

```php
Current row is 49
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

$imageIterator = $imagick->getPixelIterator();

$x = 0;

// Set the iterator row to last row
$imageIterator->setIteratorRow(249);

while ($x < 250) {

    // Get the previous row
    $pixels = $imageIterator->getPreviousIteratorRow();

    foreach ($pixels as $pixel) {
        if ($x % 4) {

            // Set the color of pixel
            $pixel->setColor('green');

        } else {

            // Set the color of pixel
            $pixel->setColor('red');
        }
    }

    // Sync the iterator
    $imageIterator->syncIterator();

    $x++;
}

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/5d5be16cb46b4b26b10c9ed595304d54.png)

**引用：**[https://www.php.net/manual/en/imagickpixeliterator.getpreviousiteratorrow.php](https://www.php.net/manual/en/imagickpixeliterator.getpreviousiteratorrow.php)