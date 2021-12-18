# PHP|Imagick exportImagePixels()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-exportimagepixels-function/](https://www.geeksforgeeks.org/php-imagick-exportimagepixels-function/)

Imagick：：exportImagePixels()函数是 PHP 中的内置函数，用于以数组形式导出原始图像像素。 该贴图定义了导出像素的顺序。 返回的数组大小为 Width*Height*strlen(Map)。

**语法：**

```
*array* Imagick::exportImagePixels( $x, $y, $width, $height, $map, $STORAGE )
```

**参数：**此函数接受上述六个参数，如下所述：

*   **$x:** it holds the x coordinates of the exported area.
*   **$y:** it holds the y coordinates of the exported area.
*   **$Width:** it saves the width of the exported area.
*   **$Height:** it maintains the height of the exported area.
*   **$map:** it saves the order in which pixels are exported. For example, "RGB". The valid characters mapped are: r, G, B, A, O, C, Y, M, K, I and P.
*   **$STORAGE:** it holds pixel type constants.

**返回值：**此函数返回包含像素值的数组。

**程序：**

```
<?php

// Create new Imagick object
$image = new Imagick();

// Use newPseudoImage() function
// to create new image
$image->newPseudoImage(0, 0, "magick:rose");

// Use exportImagePixels() function
// to export the image pixels
$pixels = $image->exportImagePixels(5, 5, 3, 3, "RGB", Imagick::PIXEL_CHAR);

// Display the output array
var_dump($pixels);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/imagick.exportimagepixels.php](https://www.php.net/manual/en/imagick.exportimagepixels.php)