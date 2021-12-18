# PHP|imagecreatefrom mpng()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefrompng-function/](https://www.geeksforgeeks.org/php-imagecreatefrompng-function/)

**imagecreatefrom mpng()函数**是 PHP 中的一个内置函数，用于从 PNG 文件或 URL 创建新图像。 这个图像可以在程序中进一步处理。 此功能通常在您想要编辑 PNG 图像时使用。

**语法：**

```php
*resource* imagecreatefrompng( *string* $filename )
```

**参数：**此函数接受保存图像名称的单个参数**$fileName**。

**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面给出的程序演示了 PHP 中的**imagecreatefrom mpng()函数**：

**程序 1(查看加载的 PNG 图像)：**

```php
<?php

// Load an image from PNG URL
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// View the loaded image in browser
header('Content-type: image/png');  
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 2(处理加载的 PNG 图像)：**

```php
<?php

// Load an image from PNG URL
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Flip the image
imageflip($im, 2);

// View the loaded image in browser
header('Content-type: image/png');  
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/c95d7ce3f4fc35e6e66ad5ca678b9a32.png)

**引用：**[https://www.php.net/manual/en/function.imagecreatefrompng.php](https://www.php.net/manual/en/function.imagecreatefrompng.php)