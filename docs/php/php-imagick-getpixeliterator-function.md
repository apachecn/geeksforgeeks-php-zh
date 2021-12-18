# PHP|Imagick getPixelIterator()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getpixeliterator-function/](https://www.geeksforgeeks.org/php-imagick-getpixeliterator-function/)

**Imagick：：getPixelIterator()函数**是 PHP 中的内置函数，用于返回图像 MagickPixelIterator。

**语法：**

```
*ImagickPixelIterator* Imagick::getPixelIterator( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 ImagickPixelIterator 值。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：getPixelIterator()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$imageIterator = $imagick->getPixelIterator();

// Change the color of every second pixel to green
foreach ($imageIterator as $row => $pixels) {
    foreach ($pixels as $column => $pixel) {
        if ($column % 2) {
            $pixel->setColor("green");
        }
    }
    $imageIterator->syncIterator();
}

// Display the output
header("Content-Type:image/png");
echo $imagick;
?>
```

**输出：**
![](img/5e177505b087023c2912744fed836034.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$imageIterator = $imagick->getPixelIterator();

// Change the color of every second pixel to green
foreach ($imageIterator as $row => $pixels) {
    foreach ($pixels as $column => $pixel) {
        if ($row % 2) {
            $pixel->setColor("blue");
        }
    }
    $imageIterator->syncIterator();
}

// Display the output
header("Content-Type:image/png");
echo $imagick;
?>
```

**输出：**
![](img/c86e8fd1b21c3ef2b0ca16b3a83d5882.png)

**引用：**[https://www.php.net/manual/en/imagick.getpixeliterator.php](https://www.php.net/manual/en/imagick.getpixeliterator.php)