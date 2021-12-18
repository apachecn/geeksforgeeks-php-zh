# PHP|ImagickDraw__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-__construct-function/](https://www.geeksforgeeks.org/php-imagickdraw-__construct-function/)

**ImagickDraw：：__Construct()函数**是 PHP 中的内置函数，用于初始化 ImagickDraw 对象。

**语法：**

```
*bool* ImagickDraw::__construct( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：__Construct()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'blue');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Draw a rectangle
$draw->rectangle(200, 50, 600, 200);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/db95e7c002d2921ef8b97bf49bf091f8.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'green');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Draw a line
$draw->line(0, 0, 800, 250);

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/e39b8a3b78b3883fc255b20db0cbd8f9.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.construct.php](https://www.php.net/manual/en/imagickdraw.construct.php)