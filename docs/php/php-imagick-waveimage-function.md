# PHP|Imagick WaveImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-waveimage-function/](https://www.geeksforgeeks.org/php-imagick-waveimage-function/)

**Imagick：：WaveImage()**函数是 PHP 中的内置函数，用于在图像中创建滤波器。 此功能在版本 6.2.9 或更高版本中可用。

**语法：**

```php
*bool* Imagick::waveImage( $amplitude, $length )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$振幅：**此参数用于设置波形的振幅。
*   **$Length：**该参数用于设置波形的长度。

**返回值：**成功时此函数返回 True。

以下程序说明了 PHP 中的**Imagick：：WaveImage()**函数：

**程序：**

```php
<?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use waveImage function
$imagick->waveImage(5, 20);

header("Content-Type: image/jpg");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![wave image](img/128a749e83312b30e5278356dff67a69.png)

**相关文章：**

*   [PHP|Imagick choImage()函数](https://www.geeksforgeeks.org/php-imagick-chopimage-function/)
*   [PHP|Imagick getImageWidth()函数](https://www.geeksforgeeks.org/php-imagick-getimagewidth-function/)

**引用：**[http://php.net/manual/en/imagick.waveimage.php](http://php.net/manual/en/imagick.waveimage.php)