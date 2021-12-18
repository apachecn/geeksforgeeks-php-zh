# PHP|Imagick import ImagePixels()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-importimagepixels-function/](https://www.geeksforgeeks.org/php-imagick-importimagepixels-function/)

**Imagick：：import ImagePixels()函数**是 PHP 中的内置函数，用于将像素从数组导入图像。

**语法：**

```
*bool* Imagick::importImagePixels( *int* $x, *int* $y, *int* $width, *int* $height, *string* $map, 
                        *int* $storage, *array* $pixels )
```

**参数：**此函数接受上述 7 个参数，如下所述：

*   **$x：**它指定图像 x 的位置。
*   **$y：**它指定图像 y 的位置。
*   **$width：**它指定图像宽度。
*   **$Height：**它指定图像高度。
*   **$map：**它将像素排序的映射指定为字符串。
*   **$storage：**它指定像素存储方法，该方法是一个像素常量对应的整数值。
*   **$Pixels：**它指定像素数组。

像素常量列表如下：

*   Imagick：：Pixel_Char(0)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   Imagick：：Pixel_Float(2)
*   Imagick：：Pixel_Integer(3)
*   Imagick：：Pixel_Long(4)
*   ==同步，由 Elderman 更正==@ELDER_MAN
*   Imagick：：Pixel_Short(6)

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：import ImagePixels()函数**：

**程序 1：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick();

// Generate array of pixels
$pixels =
   array_merge(array_pad(array(), 15000, 0),
               array_pad(array(), 15000, 255));

$imagick->newImage(100, 100, 'white');

// Import the pixels into image.
$imagick->importImagePixels(0, 0, 100, 100, "RGB", imagick::PIXEL_FLOAT, $pixels);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick;
?>
```

**输出：**
![](img/34759d0ae5e6e046665354dc3d55368f.png)

**程序 2：**

```
<?php

// Create a new Imagick object
$imagick = new Imagick();

// Generate array of pixels
$pixels =
   array_merge(array_pad(array(), 5000, 0),
               array_pad(array(), 5000, 255),
               array_pad(array(), 5000, 0),
               array_pad(array(), 5000, 255),
               array_pad(array(), 5000, 0),
               array_pad(array(), 5000, 255));

$imagick->newImage(100, 100, 'white');

// Import the pixels into image.
$imagick->importImagePixels(0, 0, 100, 100, "RGB", imagick::PIXEL_FLOAT, $pixels);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick;
?>
```

**输出：**
![](img/46a08305fa12225031ee1837def2fc17.png)

**引用：**[https://www.php.net/manual/en/imagick.importimagepixels.php](https://www.php.net/manual/en/imagick.importimagepixels.php)