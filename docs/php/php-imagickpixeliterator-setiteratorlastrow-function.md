# PHP|ImagickPixelIterator setIteratorLastRow()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixeliterator-setiteratorlastrow-function/](https://www.geeksforgeeks.org/php-imagickpixeliterator-setiteratorlastrow-function/)

**ImagickPixelIterator：：setIteratorLastRow()函数**是 PHP 中的内置函数，用于将像素迭代器设置为最后一个像素行。

**语法：**

```
*bool* ImagickPixelIterator::setIteratorLastRow( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickPixelIterator：：setIteratorLastRow()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the pixel iterator
$pixelIterator = $imagick->getPixelIterator();

// Get the current iterator row
echo "Current row is " . $pixelIterator->getIteratorRow();

// Set the iterator to last row
$pixelIterator->setIteratorLastRow();

// Get the current iterator row
echo "<br>Current row is " . $pixelIterator->getIteratorRow();
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Get the pixel iterator
$pixelIterator = $imagick->getPixelIterator();

// Set the iterator to last row
$pixelIterator->setIteratorLastRow();

$row = $pixelIterator->getIteratorRow() + 1;
echo "<br>Total number of rows in image is " . $row;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickpixeliterator.setiteratorlastrow.php](https://www.php.net/manual/en/imagickpixeliterator.setiteratorlastrow.php)