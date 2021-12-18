# PHP|ImagickPixel getIndex()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-getindex-function/](https://www.geeksforgeeks.org/php-imagickpixel-getindex-function/)

**ImagickPixel：：getIndex()函数**是 PHP 中的一个内置函数，用于获取像素的色彩映射表索引。

**语法：**

```php
*int* ImagickPixel::getIndex( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含索引的整数值。

**异常：**此函数在出错时引发 ImagickException。

下面给定的程序说明了 PHP：
**程序 1(获取单个像素的索引)中的**ImagickPixel：：getIndex()函数**：**

```php
<?php
// Create a new imagickPixel object
$imagickPixel = new ImagickPixel();

// Get the index
$index = $imagickPixel->getIndex();
echo $index;
?>
```

发帖主题：Re：Колибри0.7.0

```php
0 // which is the default index for a pixel.
```

**程序 2(获取图像所有像素的索引)：**

```php
<?php
// Create a new imagickPixel object
$imagickPixel = new ImagickPixel();

// Set the index
$imagickPixel->setIndex(5);

// Get the index
$index = $imagickPixel->getIndex();
echo $index;
?>
```

发帖主题：Re：Колибри0.7.0

```php
5
```

**程序 3：**

```php
<?php
// Create a new imagick object
$imagick = new Imagick(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the pixel iterator to iterate through each pixel
$imageIterator = $imagick->getPixelIterator();

// Loop through pixel rows
foreach ($imageIterator as $row => $pixels) {

    foreach ($pixels as $column => $pixel) {
        // Get the index of each pixel of image
        echo $pixel->getindex() . '<br>';

    }

    // Sync the iterator after each iteration
    $imageIterator->syncIterator();
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
0
0
0
0
.
.
.
```

**引用：**[https://www.php.net/manual/en/imagickpixel.getindex.php](https://www.php.net/manual/en/imagickpixel.getindex.php)