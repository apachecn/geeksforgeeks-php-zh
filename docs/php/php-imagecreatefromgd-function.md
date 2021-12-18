# PHP|imagecreatefrom mgd()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefromgd-function/](https://www.geeksforgeeks.org/php-imagecreatefromgd-function/)

函数的作用是：**imagecreatefrom mgd()函数**是 PHP 中的一个内置函数，用于从 GD 文件或 URL 创建新的图像。 此外，这个图像可以在程序中处理。 可以使用*imagegd()*函数将图像转换为 GD 格式。

**语法：**

```
*resource* imagecreatefromgd( *string* $filename )
```

**参数：**此函数接受单个参数**$fileName**，该参数保存文件的名称或 URL。

**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面给出的程序说明了 PHP 中的**imagecreatefrom mgd()函数**：
**程序 1(在浏览器中查看 gd 文件)：**

```
<?php
// Load the GD image from localfile
$im = imagecreatefromgd('geeksforgeeks.gd');

// Output the image to browser
imagegd($im);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```
This will load gd image in text form as it is not supported by browser.
```

**节目 2(将 GD 转换为 PNG 并在浏览器中查看)：**

```
<?php
// As GD isn't supported in browser, it can be
// converted into PNG to be viewed in browser
// Load the GD image
$im = imagecreatefromgd('geeksforgeeks.gd');

// Output the image to browser
header("Content-Type: image/png");
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**程序 3(将 gd 转换为 jpg)：**

```
<?php
// Load the GD image
$im = imagecreatefromgd('geeksforgeeks.gd');

// Convert the image and save in local folder
imagejpeg($im, 'geeksforgeeks.jpg');
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```
This will convert GD image into JPEG and save in local folder.
```

**引用：**[https://www.php.net/manual/en/function.imagecreatefromgd.php](https://www.php.net/manual/en/function.imagecreatefromgd.php)