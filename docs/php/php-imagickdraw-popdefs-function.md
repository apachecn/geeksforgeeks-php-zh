# PHP|ImagickDraw popDefs()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-popdefs-function/](https://www.geeksforgeeks.org/php-imagickdraw-popdefs-function/)

**ImagickDraw：：popDefs()函数**是 PHP 中的内置函数，用于终止定义列表。 这些命令通常用于定义绘制命令，出于效率的考虑，这些命令应该在较早时安全处理。 此命令不会影响绘图命令的外观。

**语法：**

```
*bool* ImagickDraw::popDefs( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序说明了 PHP 中的**ImagickDraw：：popDefs()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Set some properties of objects
$draw->setStrokeColor('red');
$draw->setFillColor('purple');
$draw->setStrokeWidth(2);
$draw->setFontSize(72);

// Create a definition
$draw->pushDefs();
$draw->setStrokeColor('green');
$draw->rectangle(150, 50, 300, 200);
$draw->popDefs();

// Draw a rectangle
$draw->rectangle(400, 50, 550, 200);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/1bc879ccbf11f13e93ed2f2ceccea15d.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Set some properties of objects
$draw->setStrokeColor('red');
$draw->setFillColor('purple');
$draw->setStrokeWidth(2);
$draw->setFontSize(72);

// Create a definition
$draw->pushDefs();
$draw->setStrokeColor('green');
$draw->circle(150, 50, 200, 200);
$draw->popDefs();

// Draw a circle
$draw->circle(400, 50, 450, 200);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/4b82043ee66101426c91a93ac6a7227d.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.popdefs.php](https://www.php.net/manual/en/imagickdraw.popdefs.php)