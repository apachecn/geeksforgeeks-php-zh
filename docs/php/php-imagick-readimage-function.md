# PHP|Imagick readImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-readimage-function/](https://www.geeksforgeeks.org/php-imagick-readimage-function/)

**Imagick：：readImage()函数**是 PHP 中的一个内置函数，用于从文件名读取图像。

**语法：**

```
*bool* Imagick::readImage( *string* $filename )
```

**参数：**此函数接受保存文件名的单个参数**$fileName**。 它还可以接受文件的 URL。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：readImage()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Read the image
$imagick->readImage(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Read the image
$imagick->readImage(
'https://media.geeksforgeeks.org/wp-content/uploads/20191117194549/g4ganimatedcolor.gif');

// Display the image
header("Content-Type: image/gif");
echo $imagick->getImagesBlob();
?>
```

**输出：**
![](img/df7e9c5957f2cb509bf9afaa1f0bbbfd.png)

**引用：**[https://www.php.net/manual/en/imagick.readimage.php](https://www.php.net/manual/en/imagick.readimage.php)