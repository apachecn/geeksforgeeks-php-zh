# PHP|Imagick pingImageFile()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-pingimagefile-function/](https://www.geeksforgeeks.org/php-imagick-pingimagefile-function/)

Imagick：：pingImageFile()函数是 PHP 中的一个内置函数，用于以轻量级方式返回图像属性。 此函数用于查找有关图像的元数据，而无需将整个图像读取到内存。
**语法：**和

```php
*bool* Imagick::pingImageFile( $filehandle, $fileName )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$fileHandle：**必选参数。 它打开图像的文件句柄。
*   **$filename：**可选参数。 它保存此图像的文件名。

**返回值：**成功时返回 True。
下面的程序说明 PHP：
**程序：**和
中的 Imagick：：pingImageFile()函数。

## PHP

```php
<?php

// Use fopen() function to open file
$fp = fopen(
"https://media.geeksforgeeks.org/wp-content/uploads/20190707132104/Capture40.jpg",
              "rb");

// Create new imagick object
$im = new Imagick();

// Pass the handle to imagick
// without loading the memory
$im -> pingImageFile($fp);

// Getting height of the image
echo "The Height of the image is: " . $im->getImageHeight() . "pixel<br>";

// Getting width of the image
echo "The Width of the image is: " . $im->getImageWidth() . "pixel";

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
The Height of the image is: 215 pixel
The Width of the image is: 604 pixel
```

**引用：**[https://php.net/manual/en/imagick.pingimagefile.php](https://php.net/manual/en/imagick.pingimagefile.php)