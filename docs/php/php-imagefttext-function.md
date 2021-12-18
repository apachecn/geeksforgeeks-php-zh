# PHP|imagefttext()函数

> Original: [https://www.geeksforgeeks.org/php-imagefttext-function/](https://www.geeksforgeeks.org/php-imagefttext-function/)

**imagefttext()函数**是 PHP 中的一个内置函数，用于使用 FreeType2 的字体将文本写入图像。

**语法：**

```
*array* imagefttext( *resource* $image, *float* $size, *float* $angle,
              *int* $x, *int* $y, *int* $color, *string* $fontfile,
              *string* $text, *array* $extrainfo )
```

**参数：**此函数接受上述 9 个参数，如下所述：

*   **$image：**它指定要处理的图像。
*   **$size：**它指定要使用的字体大小(以磅为单位)。
*   **$angle：**它以度为单位指定角度。
*   **$x：**它指定 x 坐标。
*   **$y：**它指定 y 坐标。
*   **$color：**它指定文本所需颜色的索引。
*   **$fontfile：**它指定要使用的字体。
*   **$text：**它指定要写入的文本。
*   **$ExtraInfo(可选)：**它指定额外的信息。

**返回值：**此函数成功时返回数组。

下面的示例说明了 PHP 中的**imagefttext()函数**。

**示例 1：**

```
<?php

// Create an empty image
$im = imagecreatetruecolor(800, 250);

// Add text using a font from local file
$dataArr = imagefttext($im, 0, 0, 10, 10, 
                       imagecolorallocate($im, 0, 150, 0), 
                       './Pacifico.ttf', 'GeeksforGeeks');

// Output to browser
print("<pre>".print_r($dataArr, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```
Array
(
    [0] => 8
    [1] => 12
    [2] => 18
    [3] => 12
    [4] => 18
    [5] => 7
    [6] => 8
    [7] => 7
)
```

**程序 2：**

```
<?php

// Create an empty image
$im = imagecreatetruecolor(800, 250);

// Add text using a font from local file
imagefttext($im, 50, 0, 100, 100, 
            imagecolorallocate($im, 0, 150, 0), 
            './Pacifico.ttf', 'GeeksforGeeks');

// Output to browser
header('Content-Type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/4d41c5a3fefffabbba92dd97c202c402.png)

**引用：**[https://www.php.net/manual/en/function.imagefttext.php](https://www.php.net/manual/en/function.imagefttext.php)