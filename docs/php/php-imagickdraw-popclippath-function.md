# PHP|ImagickDraw popClipPath()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-popclippath-function/](https://www.geeksforgeeks.org/php-imagickdraw-popclippath-function/)

**ImagickDraw：：popClipPath()函数**是 PHP 中的内置函数，用于终止剪辑路径定义。 剪辑路径用于创建剪辑区域，该区域决定应显示图像的哪一部分。 显示区域内的零件，而隐藏区域外部的零件。

**语法：**

```php
*bool* ImagickDraw::popClipPath( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序说明了 PHP 中的**ImagickDraw：：popClipPath()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Set the stroke color
$draw->setStrokeColor('blue');

// Set the fill color
$draw->setFillColor('cyan');

// Set the stroke width
$draw->setStrokeWidth(2);

// Push the clip path
$draw->pushClipPath('testClipPath');

// This is the area which is going to be visible
$draw->rectangle(0, 0, 250, 250);

// Pop the clip path
$draw->popClipPath();

// Set the clip path
$draw->setClipPath('testClipPath');

// Draw a rectangle
$draw->rectangle(50, 50, 350, 350);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/9d6bf21ccdb3b9c76804a252edca66bf.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Set font size
$draw->setFontSize(60);

// Push the clip path
$draw->pushClipPath('testClipPath');

// This is the area which is going to be visible
$draw->rectangle(0, 0, 250, 250);

// Pop the clip path
$draw->popClipPath();

// Set the clip path
$draw->setClipPath('testClipPath');

// Annotate the text which is going to be clipped
$draw->annotation(0, 150, 'Hello World');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/3cf41ef0c248ef4f6469c46dc700647c.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.popclippath.php](https://www.php.net/manual/en/imagickdraw.popclippath.php)