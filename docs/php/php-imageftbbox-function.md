# PHP|imageftbbox()函数

> Original: [https://www.geeksforgeeks.org/php-imageftbbox-function/](https://www.geeksforgeeks.org/php-imageftbbox-function/)

**imageftbbox()函数**是 PHP 中的一个内置函数，用于通过 freetype2 使用字体计算文本的边框。

**语法：**

```
*array* imageftbbox( *float* $size, *array* $angle,
          *string* $fontfile, *string* $text, *array* $extrainfo )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$size：**它以磅为单位指定字体大小。
*   **$angle：**它指定将测量文本的角度(以度为单位)。
*   **$fontfile：**它指定字体文件名。
*   **$text：**它指定要测量的字符串。
*   **$ExtraInfo(可选)：**它指定额外的信息。

**返回值：**此函数成功时返回数组。

下面给出的程序演示了 PHP 中的**imageftbbox()函数**：

**程序 1：**

```
<?php

// Create bounding box with local font file
$bbox = imageftbbox(100, 100, './Pacifico.ttf', 'GeeksforGeeks');

// Print the boundbox data
print("<pre>".print_r($bbox, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.0

```
Array
(
    [0] => 47
    [1] => -13
    [2] => -91
    [3] => -806
    [4] => -264
    [5] => -776
    [6] => -124
    [7] => 17
)
```

**程序 2：**

```
<?php

// Create an image
$im = imagecreatetruecolor(800, 250);

// Set the background to be light blue
imagefilledrectangle($im, 0, 0, 299, 299,
       imagecolorallocate($im, 0, 0, 100));

// Create bounding box with local font file
$bbox = imageftbbox(10, 0, './Pacifico.ttf',
            'GeeksforGeeks');

// Calculate coordinates using bounding box
$x = $bbox[0] + 130;
$y = $bbox[1] + 130;

// Add text
imagefttext($im, 50, 0, $x, $y, imagecolorallocate($im,
         0, 150, 0), './Pacifico.ttf', 'GeeksforGeeks');

// Output to browser
header('Content-Type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/93e89dc06fcafe8abb0419890d38c828.png)

**引用：**[https://www.php.net/manual/en/function.imageftbbox.php](https://www.php.net/manual/en/function.imageftbbox.php)