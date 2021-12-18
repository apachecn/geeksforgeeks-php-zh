# PHP|Imagick trimImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-trimimage-function/](https://www.geeksforgeeks.org/php-imagick-trimimage-function/)

**Imagick：：trimImage()**函数是 PHP 中的一个内置函数，用于从图像中移除边缘。

**语法：**

```
*bool* Imagick::trimImage( $fuzz )
```

**参数：**此函数接受单个参数*$fuzz*。 Image 的模糊成员定义了将两种颜色视为相同的公差可以接受的程度。 此参数表示量子范围的变化。

**返回值：**成功时此函数返回 True。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：trimImage()**函数：

**程序：**

```
?php

// Create an Imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Trim the image.
$imagick->trimImage(0);

// Ouput the image
header("Content-Type: image/" . $imagick->getImageFormat());
echo $imagick;
?>
```

**输出：**
![trim image](img/f390f752294f3ecd35814493a69b4773.png)

**相关文章：**

*   [PHP|Imagick borderImage()函数](https://www.geeksforgeeks.org/php-imagick-borderimage-function/)
*   [PHP|Imagick addImage()函数](https://www.geeksforgeeks.org/php-imagick-addimage-function/)

**引用：**[http://php.net/manual/en/imagick.trimimage.php](http://php.net/manual/en/imagick.trimimage.php)