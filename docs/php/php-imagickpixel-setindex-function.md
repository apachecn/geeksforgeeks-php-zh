# PHP|ImagickPixel setIndex()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-setindex-function/](https://www.geeksforgeeks.org/php-imagickpixel-setindex-function/)

**ImagickPixel：：setIndex()函数**是 PHP 中的一个内置函数，用于设置像素的色彩映射表索引。

**语法：**

```
*bool* ImagickPixel::setIndex( *int* $index )
```

**参数：**此函数接受单个参数**$index**，该参数保存要设置的索引。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickPixel：：setIndex()函数**：

**程序 1：**此程序设置并返回单个像素的索引。

```
<?php

// Create a new imagickPixel object
$imagickPixel = new ImagickPixel();

// Set the index
$imagickPixel->setIndex(15);

// Get the index
$index = $imagickPixel->getIndex();
echo $index;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**此程序返回图像的索引值。

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the pixel iterator to iterate through each pixel
$imageIterator = $imagick->getPixelIterator();

$i = 0;

// Loop through pixel rows
foreach ($imageIterator as $row => $pixels) {

    foreach ($pixels as $column => $pixel) {

        // Set the index
        $pixel->setIndex($i);
        echo $pixel->getIndex() . '<br>';
        $i++;
    }

    // Sync the iterator after each iteration
    $imageIterator->syncIterator();
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickpixel.setindex.php](https://www.php.net/manual/en/imagickpixel.setindex.php)