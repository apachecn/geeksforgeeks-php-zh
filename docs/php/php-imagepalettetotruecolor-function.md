# PHP|imagepalettlotruecolor()函数

> Original: [https://www.geeksforgeeks.org/php-imagepalettetotruecolor-function/](https://www.geeksforgeeks.org/php-imagepalettetotruecolor-function/)

函数是 PHP 中的一个内置函数，用于将基于调色板的图像转换为真彩色。
**语法：**和

```php
*bool* imagepalettetotruecolor( *resource* $src )
```

**参数：**此函数接受单个参数**$src**，该参数保存要处理的图像。
**返回值：**如果转换完成，或者源图像已经是真彩色图像，则此函数返回 TRUE，否则返回 FALSE。
下面给出的程序说明了 PHP：
**程序 1：**和
中的**imagepalettlotruecolor()函数**

## PHP

```php
<?php

// Create an image
$image = imagecreate(700, 200);

echo '<b>Before conversion:</b> <br>';

// Check the image type
check($image);

echo '<b><br>After conversion:</b> <br>';

// Convert image to true color
imagepalettetotruecolor($image);

// Check the image type
check($image);

// Function for checking the image type
function check($image) {
    echo 'Type of image is ' . (imageistruecolor($image)
             ? 'true color' : 'palette');
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
Before conversion:
Type of image is palette
After conversion:
Type of image is true color
```

**程序 2：**和

## PHP

```php
<?php

// Create an image of palette type
$image = imagecreate(700, 200);

// Convert image to true color
imagepalettetotruecolor($image);

// Prepare red color
$red = imagecolorallocate($image, 0xFF, 0x00, 0x00);

// Add text to the image using a local font file
imagefttext($image, 100, 0, 0, 130, $red,
       './RugeBoogie-Regular.ttf', 'GeeksforGeeks');

// Output to browser
header('Content-type: image/png');
imagepng($image);
imagedestroy($image);
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/a07c90b49e85bb94c1d8405d58f7015f.png)

**引用：**[https://www.php.net/manual/en/function.imagepalettetotruecolor.php](https://www.php.net/manual/en/function.imagepalettetotruecolor.php)