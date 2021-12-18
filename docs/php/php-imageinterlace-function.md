# PHP|imageinterlace()函数

> Original: [https://www.geeksforgeeks.org/php-imageinterlace-function/](https://www.geeksforgeeks.org/php-imageinterlace-function/)

函数**imageinterlace()**是 PHP 中内置函数，用于启用或禁用图像中的隔行扫描。 隔行扫描(也称为隔行扫描)是对位图图像进行编码的一种方法，以便部分接收它的人可以看到整个图像的降级副本。 网站上隔行和非隔行图片的一个区别是，前者先以低质量的版本加载，然后随着网站的加载质量不断提高，而非隔行图片则是在网站加载时从上到下逐行加载质量固定的图像。

**语法：**

```php
*int* imageinterlace( *resource* $image, *int* $interlace )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$image：**它指定要隔行扫描的图像。
*   **$interlace：**它指定是启用还是禁用隔行扫描。

**返回值：**如果图像的隔行扫描位已设置，则此函数返回 1，否则返回 0。

下面的示例说明了 PHP 中的**imageinterlace()函数**：

**程序 1：**在本例中，我们将启用隔行扫描。

```php
<?php

// Create an image from URL
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Enable interlacing
imageinterlace($im, 1);

// View the output
header('Content-type: image/jpeg');
imagejpeg($im);
imagedestroy($im);
?>
```

**输出：**
![](img/47a8b808a61aa176b8c62ae0c586b6b5.png)

**程序 2：**在本例中，我们将禁用隔行扫描。

```php
<?php

// Create an image from URL
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Disable interlacing
imageinterlace($im, 0);

// View the output
header('Content-type: image/jpeg');
imagejpeg($im);
imagedestroy($im);
?>
```

**输出：**
![](img/cbb51e83f0ec514619f620d46a46dd8f.png)

**引用：**[https://www.php.net/manual/en/function.imageinterlace.php](https://www.php.net/manual/en/function.imageinterlace.php)