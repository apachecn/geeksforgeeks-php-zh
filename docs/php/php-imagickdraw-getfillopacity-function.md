# PHP|ImagickDraw getFillOpacity()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getfillopacity-function/](https://www.geeksforgeeks.org/php-imagickdraw-getfillopacity-function/)

**ImagickDraw：：getFillOpacity()函数**是 PHP 中的一个内置函数，用于获取使用填充颜色或填充纹理绘制时使用的不透明度。 完全不透明为 1，完全透明为 0。

**语法：**

```
*float* ImagickDraw::getFillOpacity( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含不透明度的浮点值。

**异常：**此函数在出错时引发 ImagickException。

下面给出的程序演示了 PHP 中的**ImagickDraw：：getFillOpacity()函数**：

**程序 1：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the Fill Opacity
$fillOpacity = $draw->getFillOpacity();
echo $fillOpacity;
?>
```

发帖主题：Re：Колибри0.7.0

```
1 // which is the default value.
```

**程序 2：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the Fill Opacity
$draw->setFillOpacity(0.6);

// Get the Fill Opacity
$fillOpacity = $draw->getFillOpacity();
echo $fillOpacity;
?>
```

发帖主题：Re：Колибри0.7.0

```
0.6
```

**程序 3：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Create a image on imagick object
$imagick->newImage(800, 250, 'black');

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('yellow');

// Set the font size
$draw->setFontSize(20);

// Annotate a text
$draw->annotation(50, 100, 'The fill opacity here is ' 
                           . $draw->getFillOpacity());

// Set the fill opacity
$draw->setFillOpacity(0.4);

// Annotate a text
$draw->annotation(50, 200, 'The fill opacity here is ' 
                           . $draw->getFillOpacity());

// Render the draw commands
$imagick->drawImage($draw);

// Show the output
$imagick->setImageFormat('png');
header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/913672159ac46d1be29756f1b1373b31.png)

**引用：**[https://www.php.net/manual/en/imagickdraw.getfillopacity.php](https://www.php.net/manual/en/imagickdraw.getfillopacity.php)