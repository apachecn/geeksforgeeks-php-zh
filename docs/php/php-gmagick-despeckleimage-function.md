# PHP|Gmagick deseckleimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-despeckleimage-function/](https://www.geeksforgeeks.org/php-gmagick-despeckleimage-function/)

**Gmagick：：deseckleimage()函数**是 PHP 中的一个内置函数，用于减少图像中的斑点噪声，同时保留原始图像的边缘。

**语法：**

```
*Gmagick* Gmagick::despeckleimage( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数在成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

**使用 Image：**捕获画布区域。
![](img/4e85ee1b6ceb1ae40d4b1edeead890df.png)

下面给出的程序演示了 PHP 中的**Gmagick：：deseckleimage()函数**：

**程序 1：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeksgnoised.png');

// Apply the despeckle function
$gmagicknew = $gmagick->despeckleimage();

// Output the image
header('Content-type: image/png');
echo $gmagicknew;
?>
```

**输出：**
![](img/6e64d09c06883afd8b2d7fdd803e7687.png)

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('./geeksforgeeksnoised.png');

// Get the image histogram
$pixels = $gmagick->getimagehistogram();

echo "Color of 100th pixel before removing noise: ";
echo $pixels[99]->getcolor();

// Apply the despeckle function
$gmagicknew = $gmagick->despeckleimage();

// Get the image histogram
$pixels = $gmagick->getimagehistogram();

echo "<br>Color of 100th pixel after removing noise: ";
echo $pixels[99]->getcolor();
?>
```

发帖主题：Re：Колибри0.7.0

```
Color of 100th pixel before removing noise: rgb(0, 6682, 8995)
Color of 100th pixel after removing noise: rgb(3084, 5397, 7967)
```

**引用：**[https://www.php.net/manual/en/gmagick.despeckleimage.php](https://www.php.net/manual/en/gmagick.despeckleimage.php)