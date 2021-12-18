# PHP|ImagickDraw ush ClipPath()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pushclippath-function/](https://www.geeksforgeeks.org/php-imagickdraw-pushclippath-function/)

**ImagickDraw：：ush ClipPath()函数**是 PHP 中的一个内置函数，用于启动剪辑路径定义。 剪辑路径用于创建剪辑区域，该区域决定应显示图像的哪一部分。 显示区域内的零件，而隐藏区域外部的零件。

**语法：**

```
*bool* ImagickDraw::pushClipPath( *string* $clip_mask_id )
```

**参数：**此函数接受保存剪辑路径名称的单个参数**$clip_ask_id**。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickDraw：：ush ClipPath()函数**：

**程序 1：**

```
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

// Create a rectangle which is
// the area to be clipped
$draw->rectangle(0, 0, 300, 300);

// Pop the clip path
$draw->popClipPath();

// Set the clip path
$draw->setClipPath('testClipPath');

$draw->circle(150, 50, 300, 150);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/3a0c7d2f69ceeeb283bc4ff138d71a93.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('green');

// Set the font size
$draw->setFontSize(90);

// Push the clip path
$draw->pushClipPath('testClipPath');

// Create a circle which is
// the area to be clipped
$draw->circle(200, 200, 300, 300);

// Pop the clip path
$draw->popClipPath();

// Set the clip path
$draw->setClipPath('testClipPath');

// Annotate a text
$draw->annotation(115, 200, 'GeeksforGeeks');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/a8ce1e48ef15dc9e748f334cdc8b6e51.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pushclippath.php](https://www.php.net/manual/en/imagickdraw.pushclippath.php)