# PHP|Gmagick magifyimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-magnifyimage-function/](https://www.geeksforgeeks.org/php-gmagick-magnifyimage-function/)

**Gmagick：：MagagifyImage()**函数是 PHP 中的一个内置函数，用于将图像按比例缩放到 2 倍。 此函数用于将图像缩放为其原始大小的两倍。
**语法：**和

```php
*public* Gmagick::magnifyimage( void )
```

**参数：**此函数不接受任何参数。
**返回值：**此函数返回放大 Gmagick 对象。
**错误/异常：**此函数在出错时引发 GmagickException。
下面的程序说明了 PHP：
**程序 1：**和
**输入图像：**和
中的**Gmagick：：MagagifyImage()**函数

![](img/88e955c2701e97341d552eba1b5adceb.png)

## PHP

```php
<?php

// Create a Gmagick object
$gmagick = new Gmagick(
'https://media.geeksforgeeks.org/wp-content/uploads/tech.png');

// Use magnifyimage function
$gmagick->magnifyimage();

header('Content-type: image/png');

// Output the image
echo $gmagick;
?>
```