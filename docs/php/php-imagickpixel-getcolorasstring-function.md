# PHP|ImagickPixel getColorAsString()函数

> Original: [https://www.geeksforgeeks.org/php-imagickpixel-getcolorasstring-function/](https://www.geeksforgeeks.org/php-imagickpixel-getcolorasstring-function/)

**ImagickPixel：：getColorAsString()函数**是 PHP 中的一个内置函数，用于以字符串形式获取 ImagickPixel 对象的颜色。

**语法：**

```
*string* ImagickPixel::getColorAsString( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**ImagickPixel：：getColorAsString()函数**：

**程序 1：**

```
<?php

// Create a new imagickPixel object
$imagickPixel = new ImagickPixel();

// Get the color as string
$color = $imagickPixel->getColorAsString();
echo $color;
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new imagick object
$imagickPixel = new ImagickPixel();

// Set the color
$imagickPixel->setColor('#5b7db3');

// Get the color
$color = $imagickPixel->getColorAsString();
echo $color;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagickpixel.getcolorasstring.php](https://www.php.net/manual/en/imagickpixel.getcolorasstring.php)