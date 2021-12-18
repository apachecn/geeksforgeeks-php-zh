# PHP|Imagick setImageExtent()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageextent-function/](https://www.geeksforgeeks.org/php-imagick-setimageextent-function/)

**Imagick：：setImageExtent()函数**是 PHP 中的内置函数，用于设置图像大小。 此函数不会缩放图像，但会裁剪不需要的部分。

**语法：**

```
*bool* Imagick::setImageExtent( *int* $columns, *int* $rows )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Columns：**它指定图像的宽度。
*   **$ROWS：**它指定图像的高度。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setImageExtent()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set image extent
$imagick->setImageExtent(270, 120);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/fcb0c6bbbe9254d5fb0081aeb9010d75.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set image extent
$imagick->setImageExtent(500, 170);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/cca14a3711d934e73b3db684cca2e239.png)

**引用：**[https://www.php.net/manual/en/imagick.setimageextent.php](https://www.php.net/manual/en/imagick.setimageextent.php)