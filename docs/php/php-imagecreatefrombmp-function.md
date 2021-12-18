# PHP|imagecreatefrom mbmp()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefrombmp-function/](https://www.geeksforgeeks.org/php-imagecreatefrombmp-function/)

函数的作用是：**imagecreatefrombmp()函数**是 PHP 中的一个内置函数，用于从文件或 URL 创建新的图像。

**语法：**

```
*resource* imagecreatefrombmp( *string* $filename )
```

**参数：**此函数接受单个参数**$fileName**，该参数保存文件的名称或 URL。

**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面给出的程序演示了 PHP 中的**imagecreatefrom mbmp()函数**：

**程序 1：**在浏览器中查看 BMP 文件。

```
<?php

// Load the BMP image
$im = imagecreatefrombmp(
'https://media.geeksforgeeks.org/wp-content/uploads/20200122193540/g4gbmp.bmp');

// Output the image to browser
header('Content-type: image/bmp');  
imagebmp($im);
imagedestroy($im);
?>
```

**输出：**
![](img/1a76f8648946c7943b0c932253e95bb9.png)

**程序 2：**此程序将位图转换为 PNG。

```
<?php

// Load the BMP image
$im = imagecreatefrombmp(
'https://media.geeksforgeeks.org/wp-content/uploads/20200122193540/g4gbmp.bmp');

// Convert it to a PNG file, press Ctrl + S to save the new png image
header('Content-type: image/png');  
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**引用：**[https://www.php.net/manual/en/function.imagecreatefrombmp.php](https://www.php.net/manual/en/function.imagecreatefrombmp.php)