# PHP|imageistrucecolor()函数

> Original: [https://www.geeksforgeeks.org/php-imageistruecolor-function/](https://www.geeksforgeeks.org/php-imageistruecolor-function/)

函数的作用是：**imageistrucecolor()函数**是 PHP 中的一个内置函数，用于判断图像是否为真彩色图像。 真彩色图像是其中每个像素由三个值(即 RGB)指定的图像。

**语法：**

```php
*bool* imageistruecolor( *resource* $image )
```

**参数：**此函数接受保存图像的单个参数**$image**。

**返回值：**如果图像为真彩色，则此函数返回 TRUE，否则返回 FALSE。

下面给出的程序演示了 PHP 中的**imageistrucecolor()函数**：

**程序 1：**

```php
<?php
// Create an image instance with a truecolor image
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Check if image is truecolor
$istruecolor = imageistruecolor($im);

// Show the output to browser
if($istruecolor) {
    echo "The image is true color";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php
// Create an image instance with a grayscale image
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/20200124094548/grayscaleimage.png');

// Check if image is truecolor
$istruecolor = imageistruecolor($im);

// Show the output to browser
if(!$istruecolor) {
    echo "The image is not true color";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.imageistruecolor.php](https://www.php.net/manual/en/function.imageistruecolor.php)