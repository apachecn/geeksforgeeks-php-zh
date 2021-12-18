# PHP|Imagick orderedPosterizeImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-orderedposterizeimage-function/](https://www.geeksforgeeks.org/php-imagick-orderedposterizeimage-function/)

**Imagick：：orderedPosterizeImage()**函数是 PHP 中的一个内置函数，用于基于多个预定义的抖动阈值贴图执行有序抖动，但根据输入参数的不同，不同的通道可能会有不同的强度级别。

**语法：**

```
*bool* Imagick::orderedPosterizeImage( $threshold_map, $channel )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$THRESHOLD_MAP：**此参数用于包含要使用的阈值抖动贴图的字符串名称。
*   **$channel：**此参数提供对通道模式有效的通道常量。 可以使用按位运算符组合多个通道。 Imagick 函数中的默认通道是 Imagick：：Channel_Default。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：orderedPosterizeImage()**函数：

**程序：**

```
?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Use orderedPosterizeImage function
$imagick->orderedPosterizeImage('o8x8, 3, 3');

// Set image format
$imagick->setImageFormat('png');

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();
?>
```

**输出：**
![order posterize image](img/24ad302b5423269009801bb11f58ceeb.png)

**引用：**[http://php.net/manual/en/imagick.orderedposterizeimage.php](http://php.net/manual/en/imagick.orderedposterizeimage.php)