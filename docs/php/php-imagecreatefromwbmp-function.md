# PHP|imagecreatefrom mwbmp()函数

> Original: [https://www.geeksforgeeks.org/php-imagecreatefromwbmp-function/](https://www.geeksforgeeks.org/php-imagecreatefromwbmp-function/)

**imagecreatefrom mwbmp()函数**是 PHP 中的一个内置函数，用于从 WBMP 文件或 URL 创建新图像。 WBMP(无线应用协议位图格式)是一种针对移动计算设备优化的单色图形文件格式。 这个加载的图像可以在程序中进一步处理。 当您想要在从 WBMP 文件加载图像后对其进行编辑时，通常使用此函数。 可以使用**imagewbmp()**函数将图像转换为 WBMP。

**语法：**

```php
*resource* imagecreatefromwbmp( *string* $filename )
```

**参数：**此函数接受保存图像名称的单个参数**$fileName**。

**返回值：**此函数成功时返回图像资源标识符，出错时返回 False。

下面的示例说明了 PHP 中的**imagecreatefrom mwbmp()函数**：

**示例 1：**

```php
<?php

// Load an WBMP image from local folder
// You can convert any image to WBMP using
// imagewbmp() function or online convertors
$im = imagecreatefromwbmp('./geeksforgeeks.wbmp');

// View the loaded image in browser
imagewbmp($im);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.0

```php
This will load the content into browser in the form 
of unsupported text as browsers don't support WBMP.
```

**示例 2：**

```php
<?php

// Load an WBMP image from local folder
// You can convert any image to WBMP using
// imagewbmp() function or online convertors
$im = imagecreatefromwbmp('./geeksforgeeks.wbmp');

// Output the image by converting it into PNG
header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/07c99ec29e7a50fc3ea91a9d4a8d2f31.png)

**引用：**[https://www.php.net/manual/en/function.imagecreatefromwbmp.php](https://www.php.net/manual/en/function.imagecreatefromwbmp.php)