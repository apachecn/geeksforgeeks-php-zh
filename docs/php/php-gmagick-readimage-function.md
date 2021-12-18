# PHP|Gmagick readimage()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-readimage-function/](https://www.geeksforgeeks.org/php-gmagick-readimage-function/)

**gmagick：：readimage()函数**是 PHP 中的一个内置函数，用于从本地文件夹读取图像并将其添加到 Gmagick 对象。 这是*read()*函数的替代方法。

**语法：**

```
*Gmagick* Gmagick::readimage( *string* $filename )
```

**参数：**此函数接受保存文件名的单个参数**$fileName**。

**返回值：**此函数返回包含图像的 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：readimage()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1(从文件夹读取图像)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick();

// Read an image
$gmagick->readimage('geeksforgeeks.png');

// Output the image  
header('Content-type: image/png');  
echo $gmagick;  
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2(读后编辑图像)：**

```
<?php

// Create a new Gmagick object
$gmagick = new Gmagick();

// Read an image
$gmagick->readimage('geeksforgeeks.png');

// Here you can further work with your loaded image

// Simulate a charcoal drawing
$gmagick->charcoalimage(0.1, 10);

// Output the image
header('Content-type: image/png');
echo $gmagick;
?>
```

**输出：**
![](img/19800452099f6d877644bd6cf704f92e.png)

**引用：**[https://www.php.net/manual/en/gmagick.readimage.php](https://www.php.net/manual/en/gmagick.readimage.php)