# PHP|Imagick getFont()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-getfont-function/](https://www.geeksforgeeks.org/php-imagick-getfont-function/)

**Imagick：：getFont()函数**是 PHP 中的一个内置函数，用于获取字体。

**语法：**

```
*int* Imagick::getFont( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**成功时返回包含字体文件地址的字符串。

下面的程序演示了 PHP 中的**Imagick：：getFont()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Set the Font - make sure that the
// respective .ttf file is available in
// the same folder.
$imagick->setFont('Windsong.ttf');

// Get the Font
$font = $imagick->getFont();

echo $font();
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick();

// Set the Font - make sure that the
// respective .ttf file is available in
// the same folder.
$imagick->setFont('FFF_Tusj.ttf');

// Get the Font
$font = $imagick->getFont();

echo $font();
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.getfont.php](https://www.php.net/manual/en/imagick.getfont.php)