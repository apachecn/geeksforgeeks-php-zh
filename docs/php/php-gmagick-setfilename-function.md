# PHP|Gmagick setfilename()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-setfilename-function/](https://www.geeksforgeeks.org/php-gmagick-setfilename-function/)

**Gmagick：：setfilename()函数**是 PHP 中的一个内置函数，用于在读取或写入图像之前设置文件名。

**语法：**

```
*Gmagick* Gmagick::setfilename( *string* $filename )
```

**参数：**此函数接受保存文件名的单个参数**$filename**。

**返回值：**此函数成功时返回 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：setfilename()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the filename
$gmagick->setfilename('Filename_1.png');

// Get the filename
$name = $gmagick->getfilename();
echo $name;
?>
```

发帖主题：Re：Колибри0.7.0

```
Filename_1.png
```

**程序 2：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick('geeksforgeeks.png');

// Set the filename
$gmagick->setfilename('Filename_1.png');

// Save the image in the local folder
// using the same filename
$gmagick->writeimage($gmagick->getfilename());
?>
```

发帖主题：Re：Колибри0.7.0

```
This will save the image geeksforgeeks.png as Filename_1.png on the same folder.
```

**引用：**[https://www.php.net/manual/en/gmagick.setfilename.php](https://www.php.net/manual/en/gmagick.setfilename.php)