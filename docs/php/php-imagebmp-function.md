# PHP|imagebmp()函数

> Original: [https://www.geeksforgeeks.org/php-imagebmp-function/](https://www.geeksforgeeks.org/php-imagebmp-function/)

**imagebmp()函数**是 PHP 中的一个内置函数，用于返回输出或保存给定图像的 BMP 版本。

**语法：**

```
*bool* imagebmp( *resource* $image, *mixed* $to, *bool* $compressed )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$image：**它指定要转换的图像。
*   **$to(可选)：**它指定保存文件的路径。
*   **$COMPRESSED(可选)：**它指定是否应该使用游程编码来压缩 BMP。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时抛出异常。

下面给出的程序演示了 PHP 中的**imagebmp()函数**：

**程序 1(从头开始创建 BMP 图像)：**

```
<?php

// Create a blank image
$im = imagecreatetruecolor(120, 100);

// Add text in image
$text_color = imagecolorallocate($im, 200, 240, 21);
imagestring($im, 1, 5, 50,  'GeeksforGeeks', $text_color);

// Output that image as bmp
header("Content-Type: image/bmp");
imagebmp($im);
?>
```

**输出：**
[![](img/1254b3a144ab349ad9f3969cb35a1a45.png)](https://media.geeksforgeeks.org/wp-content/uploads/20200122193322/geeksforgeeks789.bmp)

**程序 2(将图像转换为 BMP)：**

```
<?php

// Create a image from URL
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Output that image as bmp
header("Content-Type: image/bmp");
imagebmp($im);
?>
```

**输出：**
[![](img/1a76f8648946c7943b0c932253e95bb9.png)](https://media.geeksforgeeks.org/wp-content/uploads/20200122193540/g4gbmp.bmp)

**引用：**[https://www.php.net/manual/en/function.imagebmp.php](https://www.php.net/manual/en/function.imagebmp.php)