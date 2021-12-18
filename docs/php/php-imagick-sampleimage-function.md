# PHP|Imagick sampleImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-sampleimage-function/](https://www.geeksforgeeks.org/php-imagick-sampleimage-function/)

**Imagick：：sampleImage()函数**是 PHP 中的一个内置函数，用于通过像素采样将图像缩放到所需的尺寸。与其他调整大小的方法不同，该方法不会在缩放后的图像中引入任何额外的颜色。

**语法：**

```
*bool* Imagick::sampleImage( *int* $rows, *int* $columns )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$ROWS：**它指定高度。
*   **$Columns：**它指定宽度。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：sampleImage()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Sample the image
$imagick->sampleImage(300, 300);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/55efabab5536622996e0d5f479d6c4ee.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Sample the image
$imagick->sampleImage(400, 300);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/5477d6af3451c53e9ed3c935d0faf1cd.png)

**引用：**[https://www.php.net/manual/en/imagick.sampleimage.php](https://www.php.net/manual/en/imagick.sampleimage.php)