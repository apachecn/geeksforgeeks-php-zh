# PHP|Imagick level Image()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-levelimage-function/](https://www.geeksforgeeks.org/php-imagick-levelimage-function/)

**Imagick：：level Image()函数**是 PHP 中的一个内置函数，用于调整图像的级别。

**语法：**

```php
*bool* Imagick::levelImage( $blackPoint, $gamma, 
                   $whitePoint, $channel = Imagick::CHANNEL_DEFAULT ) 
```

**参数：**此函数接受上述四个参数，如下所述：

*   **黑点：**此参数保存图像的黑点。
*   **Gamma：**此参数保存 Gamma 的值。
*   **白点：**此参数保存图像的白点。
*   **通道：**此参数保存对通道模式有效的通道常量。 使用按位运算符合并多个通道。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的 Imagick：：LevImage()函数：

**程序：**

```php
<?php

// Store the image into variable
$imagick=
"https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png";

// Declare new Imagick object
$imagick = new \Imagick($imagick);

// Use Imagick::newPseudoImage() function to create
// a new image using ImageMagick pseudo-formats
$imagick->newPseudoimage(700, 250, 'radial-gradient:red-blue');

// Function to set image format
$imagick->setFormat('png');

//  Use Imagick::getQuantum() function to
// return the ImageMagick quantum range
$quantum = $imagick->getQuantum();

// Use Imagick::levelImage() function
$imagick->levelImage($blackPoint / 100, $gamma, $quantum * $whitePoint / 100);

header("Content-Type: image/png");

// Display the image as output
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/dee0c3320f1a3e70a6f10e2e585c1b7f.png)

**引用：**[https://www.php.net/manual/en/imagick.levelimage.php](https://www.php.net/manual/en/imagick.levelimage.php)