# PHP|Imagick setImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimage-function/](https://www.geeksforgeeks.org/php-imagick-setimage-function/)

**Imagick：：setImage()函数**是 PHP 中的内置函数，用于替换对象中的图像。

**语法：**

```
*bool* Imagick::setImage( *Imagick* $replace )
```

**参数：**此函数接受包含 Imagick 对象的单个参数**$REPLACE**。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：setImage()函数**：

**程序：**

```
<?php

// Create two Imagick objects
$imagick_source = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

$imagick_replace= new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190918234528/colorize1.png');

// Replacing geeksforgeeks24.png with colorize1.png
$imagick_source->setImage($imagick_replace);

// Display the output image
header('Content-type: image/jpeg');

echo $imagick_source;
?>
```

**输出：**
![](img/d2cdeddf65779f170b39764ad552411f.png)

**引用：**[https://www.php.net/manual/en/imagick.setimage.php](https://www.php.net/manual/en/imagick.setimage.php)