# PHP|ImagickDraw Reset VectorGraphics()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-resetvectorgraphics-function/](https://www.geeksforgeeks.org/php-imagickdraw-resetvectorgraphics-function/)

**ImagickDraw：：Reset VectorGraphics()函数**是 PHP 中的内置函数，用于重置矢量图形。 矢量图形包含所有绘制命令。 重置矢量图形将删除所有旧命令。 此功能的另一个用途是当您想要将所有填充颜色重置为默认颜色(即黑色)时，您可以使用此功能。

**语法：**

```php
*bool* ImagickDraw::resetVectorGraphics( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：Reset VectorGraphics()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'cyan');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Annotate a text
$draw->annotation(400, 200, 'Hello');

// This will delete all the previous draw commands
$draw->resetVectorGraphics();

// Set the color to green
$draw->setFillColor('green');

// Draw a rectangle
$draw->rectangle(0, 0, 200, 900);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/574a642a0a94c6ff3628e2ada952966b.png)
**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'gray');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Set the color to green
$draw->setFillColor('white');

// Set the font size
$draw->setFontSize(40);

// Annotate a text
$draw->annotation(500, 100, 'GeeksforGeeks');

// Render the draw commands
$imagick->drawImage($draw);

// This will delete all the previous draw commands
// and will reset fill color to black color
$draw->resetVectorGraphics();

// Draw a circle
$draw->circle(300, 200, 300, 20);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/0ab97e2712c0e4522ff91d19d1977e12.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.resetvectorgraphics.php](https://www.php.net/manual/en/imagickdraw.resetvectorgraphics.php)