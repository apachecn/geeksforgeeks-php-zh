# PHP|Gmagick getimageinterlacesCheme()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-getimageinterlacescheme-function/](https://www.geeksforgeeks.org/php-gmagick-getimageinterlacescheme-function/)

**gmagick：：getimageinterlacesCheme()函数**是 PHP 中的一个内置函数，用于获取图像的隔行扫描方案。

**语法：**

```
*int* Gmagick::getimageinterlacescheme( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回与下列交错常量之一对应的整数值：

*   Gmagick：：interlace_unfined(0)
*   Gmagick：：interlace_no(1)
*   Gmagick：：interlace_line(2)
*   Gmagick：：interlace_plan(3)

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：getimageinterlacesCheme()函数**：

**程序 1：**

```
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Get the interlace scheme
$interlaceScheme = $gmagick->getimageinterlacescheme();
echo $interlaceScheme; 
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a new Gmagick object
// https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the interlace scheme
$gmagick->setimageinterlacescheme(gmagick::INTERLACE_LINE);

// Get the interlace scheme
$interlaceScheme = $gmagick->getimageinterlacescheme();
echo $interlaceScheme;
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/gmagick.getimageinterlacescheme.php](https://www.php.net/manual/en/gmagick.getimageinterlacescheme.php)