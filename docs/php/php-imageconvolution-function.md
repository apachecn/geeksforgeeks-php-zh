# PHP|imageconvolution()函数

> Original: [https://www.geeksforgeeks.org/php-imageconvolution-function/](https://www.geeksforgeeks.org/php-imageconvolution-function/)

**imagecvolution()**函数是 PHP 中的一个内置函数，用于修改图像内容。 它使用给定的系数和偏移量在图像中应用 3x3 卷积矩阵。 此函数成功时返回 TRUE，失败时返回 FALSE。

**语法：**

```
bool imageconvolution ( $image, $matrix, $div, $offset )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$image：**它由图像创建函数之一返回，如 imagecreatetruecolor()。 它用于创建图像的大小。
*   **$Matrix：**它包含一个由 3x3(3x3 矩阵)组成的浮点数组。
*   **$div：**它是卷积结果的除数，用于归一化。
*   **$Offset：**用于设置颜色偏移量。

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序说明了 PHP 中的**imagecvolution()**函数：

**程序 1：**

```
<?php

// Create a gif image 
$image = imagecreatefromgif(
'https://media.geeksforgeeks.org/wp-content/uploads/animateImages.gif');

// Declare a 3X3 matrix
$matrix = array(
        array(2, 0, 0), 
        array(0, -1, 0), 
        array(0, 0, -1)
);

// imageconvolution function to modify image elements
imageconvolution($image, $matrix, 1, 127);

// Output of image content
header('Content-Type: image/png');
imagepng($image, null, 9);
?>
```

**输出：**
![image](img/4fdce5008757563da12b84c46a6440da.png)

**程序 2：**

```
<?php

// Create a gif image 
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Declare a 3X3 matrix
$emboss = array(        
        array(0, -1, 2), 
        array(2, 0, 0),
        array(2, 0, -2)
);

// imageconvolution function to modify image elements
imageconvolution($image, $emboss, 1, 127);

// Output of image content
header('Content-Type: image/png');
imagepng($image, null, 9);
?>
```

**输出：**
![image](img/12cb226cfce7bbdab4d4d5644851e6a3.png)

**相关文章：**

*   [PHP|imagecolorset()函数](https://www.geeksforgeeks.org/php-imagecolorset-function/)
*   [PHP|imagecolorat()函数](https://www.geeksforgeeks.org/php-imagecolorat-function/)
*   [PHP|imagecolorsforindex()函数](https://www.geeksforgeeks.org/php-imagecolorsforindex-function/)

**引用：**[http://php.net/manual/en/function.imageconvolution.php](http://php.net/manual/en/function.imageconvolution.php)