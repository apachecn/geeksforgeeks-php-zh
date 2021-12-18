# PHP|ImagickDraw getStrokeOpacity()函数

> Original: [https://www.geeksforgeeks.org/php-imagickdraw-getstrokeopacity-function/](https://www.geeksforgeeks.org/php-imagickdraw-getstrokeopacity-function/)

ImagickDraw：：getStrokeOpacity()函数是 PHP 中的一个内置函数，用于返回笔划对象轮廓的不透明度。

**语法：**

```
*float* ImagickDraw::getStrokeOpacity( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数在成功时返回笔划不透明。

**错误/异常：**它在出错时抛出 ImagickException。

下面的程序演示了 PHP 中的 ImagickDraw：：getStrokeOpacity()函数：

**程序：**

```
<?php

// Create an ImagickDraw object
$draw = new \ImagickDraw();

// Set the Stroke Color 
$draw->setStrokeColor('Green');

// Set the Fill Color
$draw->setFillColor('Red');

// Set the stroke width
$draw->setStrokeWidth(7);

// Draw the rectangle
$draw->rectangle(40, 30, 200, 260);

// Set the stroke opacity
$draw->setStrokeOpacity(0.5);

// Display the StrokeOpacity 
echo $draw->getStrokeOpacity();
?>
```

**输出：**

```
0.49999237048905
```

**参考：**[http://php.net/manual/en/imagickdraw.getstrokeopacity.php](http://php.net/manual/en/imagickdraw.getstrokeopacity.php)