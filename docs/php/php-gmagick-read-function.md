# PHP|Gmagick read()函数

> Original: [https://www.geeksforgeeks.org/php-gmagick-read-function/](https://www.geeksforgeeks.org/php-gmagick-read-function/)

**Gmagick：：Read()函数**是 PHP 中的一个内置函数，用于从本地文件夹读取图像并将其添加到 Gmagick 对象。

**语法：**

```php
*Gmagick* Gmagick::read( *string* $filename )
```

**参数：**此函数接受保存文件名的单个参数**$fileName**。

**返回值：**此函数返回包含图像的 Gmagick 对象。

**异常：**此函数在出错时引发 GmagickException。

下面给出的程序演示了 PHP 中的**Gmagick：：Read()函数**：

**已用图像：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 1(从文件夹读取图像)：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick();

// Read an image
$gmagick->read('geeksforgeeks.png');

// Output the image  
header('Content-type: image/png');  
echo $gmagick;  
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2(读后编辑图像)：**

```php
<?php

// Create a new Gmagick object
$gmagick = new Gmagick();

// Read an image
$gmagick->read('geeksforgeeks.png');

// Here you can further work with your loaded image

// Add frame to image
$gmagick->frameimage('green', 15, 15, 5, 5);

// Output the image
header('Content-type: image/png');
echo $gmagick;
?>
```

**输出：**
![](img/24050cb0834faf6f92f8f9251bedd0a3.png)

**引用：**[https://www.php.net/manual/en/gmagick.read.php](https://www.php.net/manual/en/gmagick.read.php)