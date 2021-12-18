# PHP|ImagickDraw setGravic()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-setgravity-function/](https://www.geeksforgeeks.org/php-imagickdraw-setgravity-function/)

**ImagickDraw：：set 重力()**函数是 PHP 中的一个内置函数，用于在使用文本进行批注时设置文本放置重力。

**语法：**

```
*bool* ImagickDraw::setGravity( $gravity )
```

**参数：**此函数接受单个参数*$grasion*，该参数用于将重力值保持为重力常量。

重力常数列表如下：

*   Imagick：：Grasion_Northwest(整数)
*   Imagick：：Grasion_North(整数)
*   Imagick：：重力 _ 东北(整数)
*   Imagick：：Grasion_West(整数)
*   Imagick：：Grasion_Center(整数)
*   Imagick：：Grasion_East(整数)
*   Imagick：：Grasion_Southwest(整数)
*   Imagick：：Grasion_South(整数)
*   Imagick：：Grasion_ 东南(整数)

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的**ImagickDraw：：set 重力()**函数：

**程序 1：**

```
<?php

// Create an ImagickDraw object
$draw = new ImagickDraw();

// Set the image filled color 
$draw->setFillColor('Green');

// Set the Font Size
$draw->setFontSize(30);

// Set the Gravity Position
$draw->setGravity(5);

// Set the font family
$draw->setFontFamily('Ani');

// Set the text to be added
$draw->annotation(30, 40, "GeeksForGeeks");

// Create new Imagick object 
$imagick = new Imagick();'

// Set the image dimension
$imagick->newImage(300, 150, 'white');

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
![setGravity](img/f3e4cbca3ad154972cd09e53acc19daa.png)

**程序 2：**

```
<?php

// Create an ImagickDraw object 
$draw = new ImagickDraw();

// Set the image filled color 
$draw->setFillColor('green');

// Set the font size
$draw->setFontSize(60);

// Set the Gravity Position
$draw->setGravity(2);

// Set the text decoration
$draw->setTextDecoration(4);

// Set the text to be added
$draw->annotation(50, 75, "GeeksForGeeks");

// Create new Imagick object  
$imagick = new Imagick();

// Set the image dimensions
$imagick->newImage(600, 160, 'white');

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
![setGravity](img/67f1556c868ec62de88ff63e2c763c67.png)

**引用：**[http://php.net/manual/en/imagickdraw.setgravity.php](http://php.net/manual/en/imagickdraw.setgravity.php)