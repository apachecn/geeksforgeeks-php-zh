# PHP|ImagickDraw getVectorGraphics()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getvectorgraphics-function/](https://www.geeksforgeeks.org/php-imagickdraw-getvectorgraphics-function/)

**ImagickDraw：：getVectorGraphics()函数**是 PHP 中的内置函数，用于获取包含矢量图形的字符串。 简而言之，它包含字符串形式的所有绘制命令。 它还用于从 ImagickDraw 对象提取注释。 它返回一个包含如此多不需要的数据的大字符串，可以使用 PHP*substr()*函数对其进行修剪。

**语法：**

```
*string* ImagickDraw::getVectorGraphics( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含矢量图形的字符串值。

下面的程序演示了 PHP 中的**ImagickDraw：：getVectorGraphics()函数**：

**程序 1：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Get the vector graphics
$vectorGraphics = $draw->getVectorGraphics();

// Trim unwanted part
$vectorGraphics = substr($vectorGraphics, 807);
echo $vectorGraphics;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Add some draw commands
$draw->setTextUnderColor('green');
$draw->setFontSize(30);
$draw->line(30, 40, 100, 300);

// Get the vector graphics
$vectorGraphics = $draw->getVectorGraphics();

// Trim unwanted part
$vectorGraphics = substr($vectorGraphics, 806);
echo $vectorGraphics;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 3：**

```
<?php

// Create a new ImagickDraw object
$draw = new ImagickDraw();

// Add comment
$draw->comment('GeeksforGeeks');

// Get the vector graphics as string
$graphics = $draw->getVectorGraphics();

// Get comment from vector graphics
$comment = substr($graphics, 807); 
echo $comment;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickdraw.getvectorgraphics.php](https://www.php.net/manual/en/imagickdraw.getvectorgraphics.php)