# PHP|Gmagick setimageformat()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setimageformat-function/](https://www.geeksforgeeks.org/php-gmagick-setimageformat-function/)

**Gmagick：：setimageformat()函数**是 PHP 中的一个内置函数，用于设置图像格式。

**语法：**

```
*Gmagick* Gmagick::setimageformat( *string* $imageFormat )
```

**参数：**此函数接受保存图像格式的单个参数**$imageFormat**。

**返回值：**此函数成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：setimageformat()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the format
$gmagick->setimageformat('jpeg');

// Get the format
$format = $gmagick->getimageformat();
echo $format;
?>
```

发帖主题：Re：Колибри0.7.0

```
jpeg
```

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the format
$gmagick->setimageformat('jpeg');

// Get the format
$gmagick->write('mynewimage.' . $gmagick->getimageformat());
echo 'Image saved in same folder successfully';
?>
```

发帖主题：Re：Колибри0.7.0

```
This will change the format to jpeg from png and save image in same folder.
```

**引用：**[https://www.php.net/manual/en/gmagick.setimageformat.php](https://www.php.net/manual/en/gmagick.setimageformat.php)