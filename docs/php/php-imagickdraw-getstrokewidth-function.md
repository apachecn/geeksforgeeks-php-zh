# PHP|ImagickDraw getStrokeWidth()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getstrokewidth-function/](https://www.geeksforgeeks.org/php-imagickdraw-getstrokewidth-function/)

ImagickDraw：：getStrokeWidth()函数是 PHP 的内置函数，用于返回用于绘制对象轮廓的笔划宽度。

**语法：**

```
*float* ImagickDraw::getStrokeWidth( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数成功时返回笔划宽度。

**错误/异常：**它在出错时抛出 ImagickException。

下面的程序演示了 PHP 中的 ImagickDraw：：getStrokeWidth()函数：

**程序：**

```
<?php

// Create an ImagickDraw object
$draw = new \ImagickDraw();

// Set the Stroke Color 
$draw->setStrokeColor('Green');

// Set the Fill Color
$draw->setFillColor('Red');

// Set the stroke opacity
$draw->setStrokeOpacity(0.5);

// Draw the rectangle
$draw->rectangle(40, 30, 200, 260);

// Set the stroke width
$draw->setStrokeWidth(7);

// Display the StrokeWidth 
echo $draw->getStrokeWidth();
?>
```

**输出：**

```
7
```

**参考：**[http://php.net/manual/en/imagickdraw.getstrokewidth.php](http://php.net/manual/en/imagickdraw.getstrokewidth.php)