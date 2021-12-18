# PHP|imagefontheight()函数

> Original: [https://www.geeksforgeeks.org/php-imagefontheight-function/](https://www.geeksforgeeks.org/php-imagefontheight-function/)

**imagefontheight()函数**是 PHP 中的一个内置函数，用于获取指定字体中字符的像素高度。

**语法：**

```
*int* imagefontheight( *int* $font )
```

**参数：**此函数接受保存字体值的单个参数**$font**。 对于内置字体，它的值可以是 1、2、3、4、5；对于自定义字体，它可以与*imageloadfont()*一起使用。

**返回值：**此函数返回包含高度的整数值。

下面给出的程序演示了 PHP 中的**imagefontheight()函数**：

**程序 1：**

```
<?php

// Get the font height
echo 'Font height for font value 1 is '
        . imagefontheight(0) . '<br>';

echo 'Font height for font value 2 is '
        . imagefontheight(2) . '<br>';

echo 'Font height for font value 3 is '
        . imagefontheight(3) . '<br>';

echo 'Font height for font value 4 is '
        . imagefontheight(4) . '<br>';

echo 'Font height for font value 5 is '
        . imagefontheight(5) . '<br>';
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Get the font from local folder
$font = imageloadfont('Pacifico.ttf');

// Show the output
echo 'Font height for Pacifico is '
         . imagefontheight($font);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.imagefontheight.php](https://www.php.net/manual/en/function.imagefontheight.php)