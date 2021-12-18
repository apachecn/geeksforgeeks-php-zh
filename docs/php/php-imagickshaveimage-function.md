# PHP|Imagick：：shaveImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagickshaveimage-function/](https://www.geeksforgeeks.org/php-imagickshaveimage-function/)

**Imagick：：shaveImage()**函数是 PHP 中的一个内置函数，用于对图像边缘的像素进行着色。 它分配新的 Image 结构所需的内存，并返回指向新图像的指针。

**语法：**

```
*bool* Imagick::shaveImage( $columns, $rows )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Columns：**此参数用于设置图像的列像素。
*   **$ROWS：**此参数用于设置图像的行像素。

**返回值：**成功时此函数返回 True。

下面的程序演示了 PHP 中的**Imagick：：shaveImage()**函数：

**程序：**

```
<?php

// Create an imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use shaveImage function
$imagick->shaveImage(100, 50);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![shaveimage](img/45883a76fff552edd04127778c74c267.png)

**引用：**[http://php.net/manual/en/imagick.shaveimage.php](http://php.net/manual/en/imagick.shaveimage.php)