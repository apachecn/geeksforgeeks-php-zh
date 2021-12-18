# PHP|Imagick setImageClipMask()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageclipmask-function/](https://www.geeksforgeeks.org/php-imagick-setimageclipmask-function/)

**Imagick：：setImageClipMask()函数**是 PHP 中的内置函数，用于设置图像剪辑蒙版。

**语法：**

```php
*bool* Imagick::setImageClipMask( *Imagick* $clip_mask )
```

**参数：**此函数接受**$CLIP_MASK**作为保存图像剪辑蒙版的参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**Imagick：：setImageClipMask()函数**：

**程序 1：**

```php
<?php

// Create two new imagick objects
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$clipMask = new Imagick();

$clipMask->setGravity(4);

// Add text to the object
$clipMask->newPseudoImage($imagick->getImageWidth(),
             $imagick->getImageHeight(), "caption:ClipMaskText");

// Set the clip mask
$imagick->setImageClipMask($clipMask);
$imagick->negateImage(false);

// Show the output
$imagick->setformat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/3985781f293980ac30631551e17d3728.png)

**程序 2：**

```php
<?php

// Create two new imagick objects
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$clipMask = new Imagick();

// Create a rectangular mask
$clipMask->newPseudoImage($imagick->getImageWidth(), 
            $imagick->getImageHeight(), "canvas:Transparent");

$drawMask = new ImagickDraw();
$drawMask->setFillColor('white');
$drawMask->rectangle(170, 0, 470, 300);
$clipMask->drawImage($drawMask);

// Set the clip mask
$imagick->setImageClipMask($clipMask);
$imagick->negateImage(false);

// Show the output
$imagick->setformat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/35b365894ed3d0e05a0697ff828f48d3.png)

**引用：**[https://www.php.net/manual/en/imagick.setimageclipmask.php](https://www.php.net/manual/en/imagick.setimageclipmask.php)