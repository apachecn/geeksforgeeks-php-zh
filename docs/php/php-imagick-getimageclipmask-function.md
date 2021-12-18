# PHP|Imagick getImageClipMask()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getimageclipmask-function/](https://www.geeksforgeeks.org/php-imagick-getimageclipmask-function/)

**Imagick：：getImageClipMask()函数**是 PHP 中的一个内置函数，用于获取图像剪辑蒙版。

**语法：**

```
*array* Imagick::getImageClipMask( *void* )
```

**参数：**此函数不接受任何参数。

**异常：**此函数在出错时引发 ImagickException。

**返回值：**此函数返回包含剪辑蒙版的 Imagick 对象。

下面的程序演示了 PHP 中的**Imagick：：getImageClipMask()函数**：

**程序 1：**

```
<?php

// Create two new imagick objects
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');
$clipMask = new Imagick();

$clipMask->newPseudoImage($imagick->getImageWidth(),
                $imagick->getImageHeight(), "caption:ClipMaskText");

// Set the clip mask
$imagick->setImageClipMask($clipMask);

// Get the clip mask
$getclipMask = $imagick->getImageClipMask();

// Show the output
$getclipMask->setformat('png');
header("Content-Type: image/png");
echo $getclipMask->getImageBlob();
?>
```

**输出：**
![](img/41dafe915bb580d02ecee06b44b5914a.png)

**程序 2：**

```
<?php
// Create two new imagick objects
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$clipMask = new Imagick();

$clipMask->setGravity(4);

// Add text to the clipMask
$clipMask->newPseudoImage($imagick->getImageWidth(),
                 $imagick->getImageHeight(), "caption:ClipMaskText");

$clipMask->setImageBackgroundColor('green');
$clipMask->setImageAlphaChannel(9);

// Set the clip mask
$imagick->setImageClipMask($clipMask);

// Get the clip mask
$getclipMask = $imagick->getImageClipMask();

// Show the output
$getclipMask->setformat('png');
header("Content-Type: image/png");
echo $getclipMask->getImageBlob();
?>
```

**输出：**
![](img/79b685c41a5cad06e50c39db6380368d.png)

**引用：**[https://www.php.net/manual/en/imagick.getimageclipmask.php](https://www.php.net/manual/en/imagick.getimageclipmask.php)