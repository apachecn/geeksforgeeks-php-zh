# PHP|imageflip()函数

> Original: [https://www.geeksforgeeks.org/php-imageflip-function/](https://www.geeksforgeeks.org/php-imageflip-function/)

**imageflip()**函数是 PHP 中的一个内置函数，用于使用给定模式水平、垂直或同时水平和垂直翻转图像。

**语法：**

```php
*bool* imageflip( $image, $mode )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$image：****imagecreatetruecolor()**函数用于创建给定大小的空白图像。
*   **$mode：**此参数用于保存图像的翻转模式。 这可以是 img_flip_*常量之一：
    *   **img_fllip_Horizular-**水平翻转图像。
    *   **img_FLIP_VERIAL-**垂直翻转图像。
    *   **img_flip_Both-**水平和垂直翻转图像。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的程序演示了 PHP 中的**imageflip()**函数。

**注意：**下面给出的图像用于以下程序。
![](img/a377156ca25e3fe93469e179d416418f.png)

**程序 1：**

```php
<?php

// Assign image file in variable.
$image_name = 'geeks.png';

// Load image file
$image = imagecreatefrompng($image_name);

// Flip the image vertically
imageflip($image, IMG_FLIP_VERTICAL);

// Content type
header('Content-type: image/png');

// Output
imagejpeg($image);
?>
```

**输出：**
![image flip](img/dc15e395a87c0af9e75b90e5e750a1eb.png)

**程序 2：**

```php
<?php

// Assign image file to variable
$image_name = 'geeks.png';

// Load image file
$image = imagecreatefrompng($image_name);

// Flip the image horizontally
imageflip($image, IMG_FLIP_HORIZONTAL);

// Content type
header('Content-type: image/png');

// Output
imagejpeg($image);
?>
```

**输出：**
![flip image](img/7f92594d9001c79e08241970210360b0.png)

**程序 3：**

```php
<?php

// Assign image file to variable
$image_name = 'geeks.png';

// Load image file
$image = imagecreatefrompng($image_name);

// Flip the image file both horizontally
// and vertically.
imageflip($image, IMG_FLIP_BOTH);

// Content type
header('Content-type: image/png');

// Output
imagejpeg($image);
?>
```

**输出：**
![image flip](img/beabccefbe96c976b4966ee628961c48.png)

**相关文章：**

*   [PHP|imagedashedline()函数](https://www.geeksforgeeks.org/php-imagedashedline-function/)
*   [PHP|imagefilledpolygon()函数](https://www.geeksforgeeks.org/php-imagefilledpolygon-function/)
*   [PHP|imagefilledellipse()函数](https://www.geeksforgeeks.org/php-imagefilledellipse-function/)

**引用：**[http://php.net/manual/en/function.imageflip.php](http://php.net/manual/en/function.imageflip.php)