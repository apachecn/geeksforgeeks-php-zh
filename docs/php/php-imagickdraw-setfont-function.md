# PHP|ImagickDraw setFont()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setfont-function/](https://www.geeksforgeeks.org/php-imagickdraw-setfont-function/)

**ImagickDraw：：setFont()**函数是 PHP 中的一个内置函数，用于设置在注释文本时使用的完全指定的字体。

**语法：**

```
*bool* ImagickDraw::setFont( $font_name )
```

**参数：**此函数接受单个参数*$font_name*，该参数用于将字体名称的值保存为字符串。

**返回值：**成功时此函数返回 True。

下面的程序说明了 PHP 中的**ImagickDraw：：setFont()函数**：

**程序 1：**

```
<?php 

// Create an ImagickDraw object. 
$draw = new ImagickDraw();

// Set the fill color
$draw->setFillColor('green');

// Set the Font Size
$draw->setFontSize(40);

// Set the Font Style
$draw->setFont("./font/IndieFlower.ttf");

// Set the text to be added
$draw->annotation(50, 50, "GeeksForGeeks");

// Set the Font Style
$draw->setFont("./font/DancingScript-Regular.ttf");

// Set the text to be added
$draw->annotation(10, 100, "A Computer Science Portal For Geeks!");

// Set the Font Style
$draw->setFont("./font/NanumGothic-Regular.ttf");

// Set the text to be added
$draw->annotation(50, 150, "@sarthak_ishu11");

// Create new Imagick object  
$imagick = new Imagick();

// Set the image dimension
$imagick->newImage(560, 200, 'white');

// Set the image format
$imagick->setImageFormat("png");

// Draw the image
$imagick->drawImage($draw);
header("Content-Type: image/png");

// Display the image
echo $imagick->getImageBlob();
?>
```

**输出：**
![setFont](img/7d5c30e5a9193caa5b2eb51d7d4a04a1.png)

**程序 2：**

```
<?php 

// Create an ImagickDraw object
$draw = new ImagickDraw();

// Set the Font Size
$draw->setFontSize(40);

// Set the image filled color
$draw->setFillColor('green');

// Draw the rectangle
$draw->rectangle(30, 100, 300, 300);

// Set the image filled color
$draw->setFillColor('black');

// Set the font style
$draw->setFont("./font/IndieFlower.ttf");

// Set the text to be added
$draw->annotation(35, 280, "GeeksForGeeks");

// Create new Imagick object
$imagick = new Imagick();

// Set the image dimensions
$imagick->newImage(330, 330, 'white');

// Set the image format
$imagick->setImageFormat("png");

// Draw the image 
$imagick->drawImage($draw);
header("Content-Type: image/png");

// Display the image
echo $imagick->getImageBlob();
?>
```

**输出：**
![setFont](img/7e8682aa711b7969cb3530d9bf40c8e9.png)

**引用：**[http://php.net/manual/en/imagickdraw.setfont.php](http://php.net/manual/en/imagickdraw.setfont.php)