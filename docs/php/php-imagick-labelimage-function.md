# PHP|Imagick labelImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-labelimage-function/](https://www.geeksforgeeks.org/php-imagick-labelimage-function/)

**Imagick：：labelImage()函数**是 PHP 中的一个内置函数，用于向图像添加标签。

**语法：**

```
*bool* Imagick::labelImage( *string* $label )
```

**参数：**此函数接受单个参数**$Label**，该参数保存要添加到图像的标签。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的 Imagick：：labelImage()函数：

**程序：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://cdncontribute.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Adding the label to the image
$imagick->labelImage("This is my label.");

// Getting the label of the image
$labelInImage = $imagick->getImageProperties("label");

// Display the label of image
echo $labelInImage['label'];

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.labelimage.php](https://www.php.net/manual/en/imagick.labelimage.php)