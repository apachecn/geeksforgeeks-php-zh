# PHP|imageaffine()函数

> Original: [https://www.geeksforgeeks.org/php-imageaffine-function/](https://www.geeksforgeeks.org/php-imageaffine-function/)

**imageaffine()函数**是 PHP 中的一个内置函数，用于使用可选的剪贴区获取包含仿射变换的 src 图像的图像。 仿射是涉及矩阵的几何变换运算。

**语法：**

```php
*resource* imageaffine( *resource* $image, *array* $affine, *array* $clip )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$image：**它指定图像资源。
*   **$affine：**它使用键 0 到 5 指定数组。
*   **$Clip：**它指定要剪裁的区域。

**返回值：**此函数成功时返回仿射图像资源，失败时返回 False。

**异常：**此函数在出错时抛出异常。

下面给出的程序演示了 PHP 中的**imageaffine()函数**：

**程序 1：**

```php
<?php

// Create a image from url
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Affine the image
$newimage = imageaffine($im, [ -1.3, 0, 0, -0.7, 0, 0 ]);

// Output the image
header('Content-Type: image/png');
imagepng($newimage);
?>
```

**输出：**
![](img/0f5078f48667441c8986d4e74f8f6c89.png)

**程序 2：**

```php
<?php

// Create a image from url
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

$clipped = [
    'x' => 0,
    'y' => 0,
    'width' => 200,
    'height' => 200,
];

// Affine the image
$newimage = imageaffine($im, [-1, 0, 0, sin(4), 0, 0], $clipped);

// Output the image
header('Content-Type: image/png');
imagepng($newimage);
?>
```

**输出：**
![](img/f3d873ef09800ca93f223a2a07e3d8e6.png)

**引用：**[https://www.php.net/manual/en/function.imageaffine.php](https://www.php.net/manual/en/function.imageaffine.php)