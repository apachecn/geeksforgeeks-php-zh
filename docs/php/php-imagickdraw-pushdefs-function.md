# PHP|ImagickDraw ush Defs()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pushdefs-function/](https://www.geeksforgeeks.org/php-imagickdraw-pushdefs-function/)

**ImagickDraw：：ushDefs()函数**是 PHP 中的一个内置函数，用于指示以下命令创建命名元素以供早期处理。 这些命令通常用于定义绘制命令，出于效率的考虑，这些命令应该在较早时安全处理。 此命令不会影响绘图命令的外观。

**语法：**

```php
*bool* ImagickDraw::pushDefs( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序说明了 PHP 中的**ImagickDraw：：Push Defs()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Set some properties of objects
$draw->setFillColor('cyan');
$draw->setStrokeWidth(2);
$draw->setFontSize(72);

// Create a definition
$draw->pushDefs();
$draw->setStrokeColor('white');
$draw->annotation(200, 100, 'GeeksforGeeks');
$draw->popDefs();

// Annotate a text
$draw->annotation(200, 170, 'GeeksforGeeks');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/978f89edc77eb7772417e8f0103757d0.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Create a definition
$draw->pushDefs();
$draw->setStrokeColor('white');
$draw->line(300, 200, 230, 23);
$draw->popDefs();

// Draw a line
$draw->line(230, 200, 310, 23);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/8ab51a7039e12d02797abe5454a52f62.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pushdefs.php](https://www.php.net/manual/en/imagickdraw.pushdefs.php)