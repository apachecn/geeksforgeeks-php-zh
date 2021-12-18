# PHP|ImagickPixelIterator setIteratorFirstRow()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixeliterator-setiteratorfirstrow-function/](https://www.geeksforgeeks.org/php-imagickpixeliterator-setiteratorfirstrow-function/)

**ImagickPixelIterator：：setIteratorFirstRow()函数**是 PHP 中的内置函数，用于将像素迭代器设置为第一个像素行。

**语法：**

```
*bool* ImagickPixelIterator::setIteratorFirstRow( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickPixelIterator：：setIteratorFirstRow()函数**：

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

// Set the iterator to first row
$pixelIterator->setIteratorFirstRow();

// Get the current iterator row
echo "<br>Current row is " . $pixelIterator->getIteratorRow();
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the pixel iterator
$pixelIterator = $imagick->getPixelIterator();

$pixelIterator->setIteratorRow(40);

// Get the current iterator row
$row = $pixelIterator->getCurrentIteratorRow();
echo "Colors of 61th and 62nd pixel from 40th row are:<br>";
print("Pixel 60:" . "<pre>".print_r($row[60]->getColor(), true)."</pre>");
print("Pixel 61:" . "<pre>".print_r($row[61]->getColor(), true)."</pre>");

// Set the iterator to first row
$pixelIterator->setIteratorFirstRow();

// Get the current iterator row
$row = $pixelIterator->getCurrentIteratorRow();
echo "First two colors of pixels from first row are:<br>";
print("Pixel 1:" . "<pre>".print_r($row[0]->getColor(), true)."</pre>");
print("Pixel 2:" . "<pre>".print_r($row[1]->getColor(), true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickpixeliterator.setiteratorfirstrow.php](https://www.php.net/manual/en/imagickpixeliterator.setiteratorfirstrow.php)