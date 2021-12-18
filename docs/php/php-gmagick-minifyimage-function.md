# PHP|Gmagick minifyimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-minifyimage-function/](https://www.geeksforgeeks.org/php-gmagick-minifyimage-function/)

**Gmagick：：minifyimage()**函数是 PHP 中的一个内置函数，用于按比例将图像缩放到原始大小的一半。 此函数用于将图像大小调整为原始大小的一半。
**语法：**和

```
*Gmagick* Gmagick::minifyimage( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数成功时返回 Gmagick 对象。
**错误/异常：**此函数在出错时引发 GmagickException。
下面的程序说明了 PHP：
**程序 1：**和
**输入图像：**和
中的**Gmagick：：minifyimage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Use minifyimage function
$gmagick->minifyimage();

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```