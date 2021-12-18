# PHP|Imagick getImageFilename()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimagefilename-function/](https://www.geeksforgeeks.org/php-imagick-getimagefilename-function/)

**Imagick：：getImageFilename()函数**是 PHP 中的一个内置函数，用于获取序列中特定图像的文件名。 **getImageFilename()**和**getFilename()**的区别在于前者可以接受本地图像文件，并提供其名称和绝对地址。

**语法：**

```
*string* Imagick::getImageFilename( void )
```

**参数：**此函数不接受任何参数。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**此函数返回一个字符串值，其中包含文件的路径值，包括图像的文件名。

下面的程序说明了 PHP 中的**Imagick：：getImageFilename()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Get the Filename
$name = $imagick->getImageFilename();
echo $name;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object with a image
// which is also on same local computer folder
$imagick = new Imagick('my_image.png');

// Get the Filename
$name = $imagick->getImageFilename();
echo $name;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getimagefilename.php](https://www.php.net/manual/en/imagick.getimagefilename.php)