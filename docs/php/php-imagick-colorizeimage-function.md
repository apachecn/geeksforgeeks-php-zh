# PHP|Imagick ColorizeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-colorizeimage-function/](https://www.geeksforgeeks.org/php-imagick-colorizeimage-function/)

**Imagick：：ColorizeImage()函数**是 PHP 中的一个内置函数，用于将填充颜色与图像中具有指定不透明度的每个像素混合。

**语法：**

```php
*bool* Imagick::colorizeImage( *mixed* $colorize, *mixed* $opacity, *bool* $legacy = FALSE )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$Colorize：**此参数保存 ImagickPixel 对象或包含着色颜色的字符串。
*   **$opacity：**此参数保存包含不透明度的 ImagickPixel 对象或浮点。 值 1.0 表示完全不透明，0.0 表示完全透明。
*   **$Legacy：**此参数包含一个布尔值，用于告知是否需要遗留行为。 建议将其保持为 true 以使用字符串颜色。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：ColorizeImage()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Colorize the image
$imagick->colorizeImage('blue', 1, true);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/d2cdeddf65779f170b39764ad552411f.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Colorize the image
$imagick->colorizeImage('orange', 0.5, true);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/e214c0bc50254f758145bab0e45460f3.png)

**引用：**[https://www.php.net/manual/en/imagick.colorizeimage.php](https://www.php.net/manual/en/imagick.colorizeimage.php)