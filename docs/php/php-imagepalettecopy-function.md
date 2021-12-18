# PHP|imagepalettecopy()函数

> Original: [https://www.geeksforgeeks.org/php-imagepalettecopy-function/](https://www.geeksforgeeks.org/php-imagepalettecopy-function/)

**imagepalettecopy()函数**是 PHP 中的一个内置函数，用于将调色板从一个图像复制到另一个图像。

**语法：**

```
*void* imagepalettecopy( *resource* $destination, *resource* $source )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$Destination：**它指定目标图像资源。
*   **$source：**它指定源图像资源。

**返回值：**此函数不返回任何内容。

下面给出的程序演示了 PHP 中的**imagepalettecopy()函数**：

**程序 1：**

```
<?php
// Create two palette images
$palette1 = imagecreate(700, 200);
$palette2 = imagecreate(700, 200);

// Create a green color
$green = imagecolorallocate($palette1, 0, 255, 0);

// Add green color as background to pallete 1
imagefilledrectangle($palette1, 0, 0, 99, 99, $green);

// Copy the palette from image 1 to image 2
imagepalettecopy($palette2, $palette1);

// Output image to the browser and see the color is green
header('Content-type: image/png');
imagepng($palette2);
?>
```

**输出：**
![](img/3a6443c7a30423251c7e74f5ebd3f0af.png)

**程序 2：**

```
<?php
// Create two palette images
$palette1 = imagecreate(700, 200);
$palette2 = imagecreate(700, 200);

// Create a green color
$green = imagecolorallocate($palette1, 0, 255, 0);

// Add green color as background to pallete 1
imagefilledrectangle($palette1, 0, 0, 99, 99, $green);

// Copy the palette from image 1 to image 2
imagepalettecopy($palette2, $palette1);

// Get the number of colors in image
$color1 = imagecolorstotal($palette1);
$color2 = imagecolorstotal($palette2);

echo "Number of colors at image 1 is " . $color1 . "<br>";
echo "Number of colors at image 2 is " . $color2;
?>
```

发帖主题：Re：Колибри0.7.0

```
Number of colors at image 1 is 1
Number of colors at image 2 is 1
```

**引用：**[https://www.php.net/manual/en/function.imagepalettecopy.php](https://www.php.net/manual/en/function.imagepalettecopy.php)