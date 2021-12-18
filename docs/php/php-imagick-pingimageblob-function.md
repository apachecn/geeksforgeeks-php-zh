# PHP|Imagick pingImageBlob()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-pingimageblob-function/](https://www.geeksforgeeks.org/php-imagick-pingimageblob-function/)

**Imagick：：pingImageBlob()函数**是 PHP 中的一个内置函数，用于查询图像属性，而无需将整个图像加载到内存中。 可以查询图片的宽度、高度、大小、格式。 它以整个图像流为参数。

**语法：**

```
*bool* Imagick::pingImageBlob( $image )
```

**参数：**此函数接受单个参数**$image**，它是包含图像流的字符串。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的 Imagick：：pingImageBlob()函数：

**程序：**此程序将显示图像的高度和宽度，而不会将其实际加载到屏幕上。

```
<?php

// Read a file in form of string
$image = file_get_contents(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-6.png');

// Create new Imagick object
$imagick = new Imagick();

// Use Imagick::pingImageBlob() function
$imagick->pingImageBlob($image);

// Get the details of the image
echo "Width of image: " . $imagick->getImageWidth() . "<br>" . 
     "Height of image: " . $imagick->getImageHeight();

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.pingimageblob.php](https://www.php.net/manual/en/imagick.pingimageblob.php)