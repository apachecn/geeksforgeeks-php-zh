# PHP|GmagickDraw setfont()函数

> Original: [https://www.geeksforgeeks.org/php-gmagickdraw-setfont-function/](https://www.geeksforgeeks.org/php-gmagickdraw-setfont-function/)

**GmagickDraw：：setfont()函数**是 PHP 中的一个内置函数，用于设置在使用文本进行批注时使用的完全指定的字体。

**语法：**

```php
*GmagickDraw* GmagickDraw::setfont( *string* $font )
```

**参数：**此函数接受单个参数**$font**，该参数用于将字体名称的值保存为字符串。

**返回值：**此函数成功时返回 GmagickDraw 对象。

**异常：**此函数在出错时引发 GmagickDrawException。

下面给出的程序说明了 PHP：
**程序 1：**中的**GmagickDraw：：setfont()函数**

```php
<?php
// Create a GmagickDraw object
$draw = new GmagickDraw();

// Set the font using a local ttf file
$draw->setfont('roboto.ttf');

// Get the font
$font = $draw->getfont();
echo $font;
?>
```

发帖主题：Re：Колибри0.7.0

```php
/home/user/php/roboto.ttf
```

**程序 2：**

```php
<?php
// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Create a GmagickDraw object
$draw = new GmagickDraw();

// Draw rectangle for background
$draw->rectangle(-100, -1000, 800, 400);

// Set the font size
$draw->setfontsize(90);

// Set the stroke color
$draw->setstrokecolor('red');

// Set the font
$draw->setfont('Pacifico.ttf');

// Create a rectangle
$draw->annotate(20, 110, 'GeeksforGeeks');

// Use of drawimage function
$gmagick->drawImage($draw);

// Display the output image
header("Content-Type: image/png");
echo $gmagick->getImageBlob();
?>
```

**输出：**
![](img/249680cb39e04a4bc8b6f42d125578d7.png)

**引用：**[https://www.php.net/manual/en/gmagickdraw.setfont.php](https://www.php.net/manual/en/gmagickdraw.setfont.php)