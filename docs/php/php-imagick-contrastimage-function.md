# PHP|Imagick 对比度图像()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-contrastimage-function/](https://www.geeksforgeeks.org/php-imagick-contrastimage-function/)

**Imagick：：ConstrastImage()函数**是 PHP 中的一个内置函数，用于更改图像的对比度。 此功能可增强图像中较亮和较暗元素之间的亮度差异。

**语法：**

```php
*bool* Imagick::contrastImage(*bool* $sharpen)
```

**参数：**此函数接受单个参数**$Sharpen**，该参数决定是增大还是减小对比度。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：ConstrastImage()函数**：

**程序 1：**

```php
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Apply the contrastImage() function
$imagick->contrastImage(false);

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/117b74a55e16e94ae2c6df9a2e4f151c.png)

**程序 2：**

```php
<?php

// Create new Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Apply the contrastImage() function
$imagick->contrastImage(true);

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/293b2ed2ea39bd48d7f3088e11843f66.png)

**引用：**[https://www.php.net/manual/en/imagick.contrastimage.php](https://www.php.net/manual/en/imagick.contrastimage.php)