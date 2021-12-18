# PHP|ImagickDraw Clear()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-clear-function/](https://www.geeksforgeeks.org/php-imagickdraw-clear-function/)

**ImagickDraw：：Clear()函数**是 PHP 中的一个内置函数，用于清除 ImagickDraw 对象中所有累积的命令，并将其包含的设置重置为默认值。

**语法：**

```php
*bool* ImagickDraw::clear( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序说明了 PHP：
**程序 1：**中的**ImagickDraw：：Clear()函数**

```php
<?php

//Create a new Imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the text properties
$draw->setFontSize(110);
$draw->setFillColor('green');

// Apply the annotation() function
$draw->annotation(20, 120, 'Random Content');

// Clear the object which means commands
// written above are all deleted now
$draw->clear();

// Set the font size
$draw->setFontSize(110);
$draw->setFillColor('white');

// Apply the annotation() function
$draw->annotation(20, 120, 'New Content');

//  Render the draw commands in the ImagickDraw object
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat("png");
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/71f18a4c181cf7832f1f3e65f0db98d6.png)

**程序 2：**

```php
<?php

//Create a new Imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the text properties
$draw->setFontSize(110);
$draw->setFillColor('green');

// Apply the annotation() function
$draw->annotation(20, 120, 'GeeksforGeeks');

// Clear the object which means commands written
// above are not all deleted now
$draw->clear();

//  Render the draw commands in the ImagickDraw object
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat("png");
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will throw ImagickException because $draw is emptied by clear(), thus cannot be drawn.
```

**引用：**[https://www.php.net/manual/en/imagickdraw.clear.php](https://www.php.net/manual/en/imagickdraw.clear.php)