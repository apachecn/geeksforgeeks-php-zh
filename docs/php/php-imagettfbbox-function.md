# PHP|imagettfbbox()函数

> Original: [https://www.geeksforgeeks.org/php-imagettfbbox-function/](https://www.geeksforgeeks.org/php-imagettfbbox-function/)

**imagettfbbox()函数**是 PHP 中的一个内置函数，用于计算 TrueType 文本的边界框(以像素为单位)。
**语法：**和

```
*array* imagettfbbox( *float* $size, *float* $angle, 
                 *string* $fontfile, *string* $text)
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$size：**它以磅为单位指定字体大小。
*   **$angle：**它指定将测量文本的角度(以度为单位)。
*   **$fontfile：**它指定字体文件名。
*   **$text：**它指定要测量的字符串。

**返回值：**此函数成功时返回数组。
以下示例说明 PHP 中的**imagettfbbox()函数**：
**示例 1：**和

## PHP

```
<?php

// Create bounding box with local font file
$bbox = imagettfbbox(100, 100,
       './Pacifico.ttf', 'GeeksforGeeks');

// Print the boundbox data
print("<pre>".print_r($bbox, true)."</pre>");
?>
```

发帖主题：Re：Колибри0.7.8.0

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

**示例 2：**和

## PHP

```
<?php

// Create a image
$im = imagecreatetruecolor(800, 250);

// Set the background to be light blue
imagefilledrectangle($im, 0, 0, 800, 299,
            imagecolorallocate($im, 255, 0, 100));

// Create bounding box with local font file
$bbox = imagettfbbox(10, 0,
            './Pacifico.ttf', 'GeeksforGeeks');

// Calculate coordinates using bounding box
$x = $bbox[0] + 130;
$y = $bbox[1] + 130;

// Add text
imagettftext($im, 50, 0, $x, $y,
        imagecolorallocate($im, 0, 150, 0),
        './Pacifico.ttf', 'GeeksforGeeks');

// Output to browser
header('Content-Type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

发帖主题：Re：Колибри0.7.8.0

![](img/10b69b3bbb1bff2be1c96b8338666d18.png)

**引用：**[https://www.php.net/manual/en/function.imagettfbbox.php](https://www.php.net/manual/en/function.imagettfbbox.php)