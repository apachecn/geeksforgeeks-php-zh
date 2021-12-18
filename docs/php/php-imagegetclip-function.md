# PHP|ImagegetClip()函数

> Original: [https://www.geeksforgeeks.org/php-imagegetclip-function/](https://www.geeksforgeeks.org/php-imagegetclip-function/)

**ImagickDraw：：ImagegetClip()函数**是 PHP 中的一个内置函数，用于获取当前的裁剪矩形，即将绘制超出像素数的区域。 默认裁剪区域是整个图像，可以使用**imagesetClip()**函数进行自定义。

**语法：**

```
*array* ImagickDraw::imagegetclip( *resource* $image )
```

**参数：**此函数接受保存图像的单个参数**$image**。

**返回值：**此函数返回包含裁剪区域的数组。

以下示例说明 PHP 中的**ImagickDraw：：ImagegetClip()函数**：

**示例 1：**

```
<?php

// Create an image
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Get the clipping area
print("<pre>".print_r(imagegetclip($im),
                         true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create an image
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Set the clip area
imagesetclip($im,100, 100, 200, 300);

// Get the clipping area
print("<pre>".print_r(imagegetclip($im),
                         true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.imagegetclip.php](https://www.php.net/manual/en/function.imagegetclip.php)