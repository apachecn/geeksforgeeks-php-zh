# PHP|ImagickDraw getClipUnits()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getclipunits-function/](https://www.geeksforgeeks.org/php-imagickdraw-getclipunits-function/)

**ImagickDraw：：getClipUnits()函数**是 PHP 中的一个内置函数，用于获得剪辑路径单元的解释。

**语法：**

```php
*int* ImagickDraw::getClipUnits( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回一个与其中一个分辨率常量对应的整数值

解析常量列表如下：

*   Imagick：：RESOLUTION_UNDEFINED(0)
*   Imagick：：RESOLUTION_PIXELSPERINCH(1)
*   Imagick：：RESOLUTION_PIXELSPERCENTIMETER(2)

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：getClipUnits()函数**：

**程序 1：**

```php
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get clipUnits
echo $draw->getClipUnits();
?>
```

发帖主题：Re：Колибри0.7.0

```php
0 // which corresponds to imagick::RESOLUTION_UNDEFINED.
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(500, 250, 'green');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

$draw->setClipUnits(imagick::RESOLUTION_PIXELSPERINCH);

$draw->setFontSize(24);

$draw->annotation(160, 125, 
                  'The clipUnits is '
                  . $draw->getClipUnits() . '.');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/3076aed399a38f68f84a1c835d122419.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.getclipunits.php](https://www.php.net/manual/en/imagickdraw.getclipunits.php)