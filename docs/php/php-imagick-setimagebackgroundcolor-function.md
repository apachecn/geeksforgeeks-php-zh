# PHP|Imagick setImageBackround Color()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagebackgroundcolor-function/](https://www.geeksforgeeks.org/php-imagick-setimagebackgroundcolor-function/)

**Imagick：：setImageBackround Color()函数**是 PHP 中的一个内置函数，用于设置图像背景颜色。

**语法：**

```
*bool* Imagick::setImageBackgroundColor( *mixed* $background )
```

**参数：**此函数接受保存背景颜色的单个参数**$background**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageBackround Color()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set background color
$imagick->setImageBackgroundColor('yellow');

// Set the ImageAlphaChannel to 9 which corresponds
// to imagick::ALPHACHANNEL_TRANSPARENT
$imagick->setImageAlphaChannel(9);

// Display the image
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/3b1fce08a075b5f9125fd56c6d051988.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Write the caption in a image
$imagick->newPseudoImage(800, 270, "caption:GeekforGeeks");

// Set background color
$imagick->setImageBackgroundColor('grey');

// Set the ImageAlphaChannel to 9 which corresponds
// to imagick::ALPHACHANNEL_TRANSPARENT
$imagick->setImageAlphaChannel(9);

// Display the image
$imagick->setformat('png');
header("Content-Type: image/png");

echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/8355eb0ac80f4826253477360b823179.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagebackgroundcolor.php](https://www.php.net/manual/en/imagick.setimagebackgroundcolor.php)