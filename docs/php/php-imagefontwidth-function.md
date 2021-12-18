# PHP|imagefontwidth()函数

> Original: [https://www.geeksforgeeks.org/php-imagefontwidth-function/](https://www.geeksforgeeks.org/php-imagefontwidth-function/)

函数的作用是：**imagefontwidth()函数**是 PHP 中的一个内置函数，用于获取指定字体中字符的像素宽度。

**语法：**

```
*int* imagefontwidth( *int* $font )
```

**参数：**此函数接受保存字体的单个参数**$font**。 对于内置字体，它可以是 1、2、3、4、5；对于自定义字体，它可以与*imageloadfont()*一起使用。

**返回值：**此函数返回包含字体宽度的整数值。

以下程序说明了 PHP 中的**imagefontwidth()函数**：

**程序 1：**

```
<?php

// Get the font width
echo 'Font width for font value 1 is '
        . imagefontwidth(1) . '<br>';

echo 'Font width for font value 2 is '
        . imagefontwidth(2) . '<br>';

echo 'Font width for font value 3 is '
        . imagefontwidth(3) . '<br>';

echo 'Font width for font value 4 is '
        . imagefontwidth(4) . '<br>';

echo 'Font width for font value 5 is '
        . imagefontwidth(5) . '<br>';
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Get the font from local folder
$font = imageloadfont('Pacifico.ttf');

// Show the output
echo 'Font width for Pacifico is '
         . imagefontwidth($font);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.imagefontwidth.php](https://www.php.net/manual/en/function.imagefontwidth.php)