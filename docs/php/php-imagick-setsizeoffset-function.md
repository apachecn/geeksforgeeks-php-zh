# PHP|Imagick setSizeOffset()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setsizeoffset-function/](https://www.geeksforgeeks.org/php-imagick-setsizeoffset-function/)

**Imagick：：setSizeOffset()函数**是 PHP 中的一个内置函数，用于设置 Imagick 对象的大小和偏移量。

**语法：**

```
*bool* Imagick::setSizeOffset( *int* $columns, *int* $rows, *int* $offset )
```

**参数：**此函数接受三个参数，如上所述，如下所述：

*   **$Columns:** it specifies the width in pixels.
*   **$row:** it specifies the height in pixels.
*   **$Offset:** it specifies the image offset.

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：setSizeOffset()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the size offset
$imagick->setSizeOffset(100, 400, 35);

// Get the size offset
$sizeOffset = $imagick->getSizeOffset();
echo $sizeOffset;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the size offset
$imagick->setSizeOffset(300, 800, 21);

// Get the size offset
$sizeOffset = $imagick->getSizeOffset();
echo $sizeOffset;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.setsizeoffset.php](https://www.php.net/manual/en/imagick.setsizeoffset.php)