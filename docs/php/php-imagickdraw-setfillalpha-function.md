# PHP|ImagickDraw setFillAlpha()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setfillalpha-function/](https://www.geeksforgeeks.org/php-imagickdraw-setfillalpha-function/)

**ImagickDraw：：setFillAlpha()函数**是 PHP 中的一个内置函数，用于设置使用填充颜色或填充纹理绘制时要使用的不透明度。

**语法：**

```php
*bool* ImagickDraw::setFillAlpha( *float* $opacity )
```

**参数：**此函数接受单个参数**$opacity**，该参数保存颜色的不透明度，其中 1 表示不透明，0 表示透明。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：setFillAlpha()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Set the color to green
$draw->setFillColor('green');

// Set the opacity
$draw->setFillAlpha(0.3);

// Set the font size
$draw->setFontSize(80);

// Annotate a text
$draw->annotation(100, 150, 'GeeksforGeeks');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/38ff0642115da3fec576c8de14f4c27d.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Set the color to green
$draw->setFillColor('green');

// Set the opacity
$draw->setFillAlpha(0.3);

// Draw a circle
$draw->circle(300, 200, 230, 20);

// Set the color to red
$draw->setFillColor('red');

// Set the opacity
$draw->setFillAlpha(0.5);

// Draw a rectangle
$draw->rectangle(200, 300, 20, 100);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/23b4692a6bc1d4e51fb0fff342e70c1c.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.setfillalpha.php](https://www.php.net/manual/en/imagickdraw.setfillalpha.php)