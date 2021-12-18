# PHP|ImagickPixelIterator getCurrentIteratorRow()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixeliterator-getcurrentiteratorrow-function/](https://www.geeksforgeeks.org/php-imagickpixeliterator-getcurrentiteratorrow-function/)

**ImagickPixelIterator：：getCurrentIteratorRow()函数**是 PHP 中的内置函数，用于从像素迭代器以 ImagickPixel 对象数组的形式获取当前行。

**语法：**

```php
*array* ImagickPixelIterator::getCurrentIteratorRow( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含 ImagickPixel 对象的数组值，这些对象本身可以迭代。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickPixelIterator：：getCurrentIteratorRow()函数**：

**程序 1(获取第一行的前五个像素)：**

```php
<?php
// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object with 
// 5 pixels on row and 10 pixels on columns
$imagick->newImage(5, 10, 'black');

// Get the pixel iterator
$pixelIterator = $imagick->getPixelIterator();

// Get the current iterator row
$row = $pixelIterator->getCurrentIteratorRow();
print("<pre>".print_r($row, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2(获取第一行前五个像素的颜色)：**

```php
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the pixel iterator
$pixelIterator = $imagick->getPixelIterator();

// Get the current iterator row
$row = $pixelIterator->getCurrentIteratorRow();
echo "First five colors of pixels are:<br>";
print("Pixel 1:" . "<pre>".print_r($row[0]->getColor(), true)."</pre>");
print("Pixel 2:" . "<pre>".print_r($row[1]->getColor(), true)."</pre>");
print("Pixel 3:" . "<pre>".print_r($row[2]->getColor(), true)."</pre>");
print("Pixel 4:" . "<pre>".print_r($row[3]->getColor(), true)."</pre>");
print("Pixel 5:" . "<pre>".print_r($row[4]->getColor(), true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickpixeliterator.getcurrentiteratorrow.php](https://www.php.net/manual/en/imagickpixeliterator.getcurrentiteratorrow.php)