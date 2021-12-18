# PHP|ImagickPixel__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-__construct-function/](https://www.geeksforgeeks.org/php-imagickpixel-__construct-function/)

**ImagickPixel：：__Construct()函数**是 PHP 中的内置函数，用于构造 ImagickPixel 对象。 如果指定了颜色，则构造对象，然后使用该颜色进行初始化。

**语法：**

```php
*bool* ImagickPixel::__construct( *void* )
```

**参数：**此函数接受单个参数**$color**，该参数是可选的，包含颜色。

**返回值：**成功时此函数返回 ImagickPixel 对象。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**ImagickPixel：：__Construct()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object using __construct
// function without any arguments
$imagickPixel = new ImagickPixel();

// Set the color
$imagickPixel->setColorValue(Imagick::COLOR_ALPHA, 0.6);

// Get the color
echo print_r($imagickPixel->getColorValue(Imagick::COLOR_ALPHA));
?>
```

发帖主题：Re：Колибри0.7.0

```php
0.61
```

**程序 2：**

```php
<?php

// Create a new imagick object using __construct
// function with a color as argument
$imagickPixel = new ImagickPixel('#41bf63');

// Get the color
echo $imagickPixel->getColorAsString();
?>
```

发帖主题：Re：Колибри0.7.0

```php
srgb(65, 191, 99)
```

**程序 3：**

```php
<?php

// Create a new imagick object using __construct
// function with a color as argument
$imagickPixel = new ImagickPixel('#62c730');

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'white');

// Create a new imagickDraw object
$draw = new ImagickDraw();

// Set the color using imagickPixel
$draw->setFillColor($imagickPixel);

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
![](img/6acf48dc0e806323aa6e17cbaf9799f8.png)

**引用：**[https://www.php.net/manual/en/imagickpixel.construct.php](https://www.php.net/manual/en/imagickpixel.construct.php)