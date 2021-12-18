# PHP|imagecolorclosestapha()函数

> Original: [https://www.geeksforgeeks.org/php-imagecolorclosestalpha-function/](https://www.geeksforgeeks.org/php-imagecolorclosestalpha-function/)

**imagecolorclosestapha()**函数是 PHP 中的一个内置函数，用于获取给定图像中与 Alpha 值最接近的颜色索引。 此函数用于返回图像调色板中最接近指定 RGB 值和 Alpha 级别的颜色的索引。 Alpha 值表示图像的透明度。

**语法：**

```
*int* imagecolorclosestalpha ( $image, $red, $green, $blue, $alpha )
```

**参数：**此函数接受上述五个参数，如下所述：

*   **$image：**它由图像创建函数之一返回，如 imagecreatetruecolor()。 它用于创建图像的大小。
*   **$red：**该参数用于设置红色分量的值。
*   **$green：**该参数用于设置绿色分量的值。
*   **$BLUE：**该参数用于设置蓝色分量的值。
*   **$alpha：**此参数用于设置图像的透明度。 $alpha 的值介于 0 到 127 之间，其中 0 表示完全不透明，127 表示完全透明。

**返回值：**此函数返回调色板中最接近颜色的索引。

下面的程序说明了 PHP 中的**imagecolorclosestapha()**函数：

**程序 1：**

## PHP

```
<?php

// Convert an image into a palette-based image
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/col1.png');

imagetruecolortopalette($image, false, 255);

// Find closest color in image
$output = imagecolorclosestalpha($image, 155, 40, 200, 50);
$output = imagecolorsforindex($image, $output);
$output = "({$output['red']}, {$output['green']},
          {$output['blue']}, {$output['alpha']})";

echo "Closest match: " . $output . "\n";

imagedestroy($image);
?>
```

发帖主题：Re：Колибри0.7.0

```
Closest match: (100, 58, 108, 0)
```

**程序 2：**

## PHP

```
<?php

// Convert an image into a palette-based image
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/col1.png');

imagetruecolortopalette($image, false, 255);

// Search the given rgb color.
$color = array(
    array(155, 40, 200, 50),
    array(235, 205, 188, 127),
    array(135, 00, 132, 0),
);

// Loop to return the closest color match.
foreach($color as $id => $rgb)
{
    $output = imagecolorclosestalpha($image, $rgb[0],
                          $rgb[1], $rgb[2], $rgb[3]);

    $output = imagecolorsforindex($image, $output);

    $output = "({$output['red']}, {$output['green']},
              {$output['blue']}, {$output['alpha']})";

    echo "Given color: ($rgb[0], $rgb[1], $rgb[2], $rgb[3])
                 => Closest match: $output <br>";
}

imagedestroy($image);
?>
```

发帖主题：Re：Колибри0.7.0

```
Given color: (155, 40, 200, 50) => Closest match: (100, 58, 108, 0) 
Given color: (235, 205, 188, 127) => Closest match: (100, 58, 108, 0) 
Given color: (135, 0, 132, 0) => Closest match: (100, 58, 108, 0) 
```

**相关文章：**

*   [PHP|imagecharup()函数](https://www.geeksforgeeks.org/php-imagecharup-function/)
*   [PHP|imagedashedline()函数](https://www.geeksforgeeks.org/php-imagedashedline-function/)

**引用：**[http://php.net/manual/en/function.imagecolorclosestalpha.php](http://php.net/manual/en/function.imagecolorclosestalpha.php)