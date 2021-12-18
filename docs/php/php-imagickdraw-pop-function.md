# PHP|ImagickDraw POP()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-pop-function/](https://www.geeksforgeeks.org/php-imagickdraw-pop-function/)

**ImagickDraw：：op()函数**是 PHP 中的一个内置函数，用于销毁堆栈中的当前 ImagickDraw，并返回之前推送的 ImagickDraw。 对于每个*POP()*函数，必须已经有一个等效的*Push()*函数。

**语法：**

```
*bool* ImagickDraw::pop( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

下面的程序演示了 PHP 中的**ImagickDraw：：POP()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create an image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('blue');

// Set the font size
$draw->setFontSize(70);

// Push 
$draw->push();

// Annotate a text
$draw->annotation(250, 70, 'Hello');

// Pop
$draw->pop();

// Set the fill color for new object
$draw->setFillColor('green');

// Annotate a text
$draw->annotation(250, 170, 'World');

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/30d5103dda87e32c2a003c9d9c2d7247.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the stroke color
$draw->setStrokeColor('red');

// Set the fill color
$draw->setFillColor('blue');

// Set the stroke width
$draw->setStrokeWidth(5);

// Set the font size
$draw->setFontSize(72);

// Push 
$draw->push();

// Translate the object
$draw->translate(50, 50);

// Draw a circle
$draw->circle(250, 70, 250, 130);

// Pop because we want to draw a new
// circle with new properties.
$draw->pop();

// Set the stroke color for new object
$draw->setStrokeColor('violet');

// Set the fill color for new object
$draw->setFillColor('green');

// Draw a new circle
$draw->circle(250, 70, 250, 130);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/8d2f011d980d7e552956114287b5b8c6.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.pop.php](https://www.php.net/manual/en/imagickdraw.pop.php)