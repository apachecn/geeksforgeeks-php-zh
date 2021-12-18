# PHP|imagecolorest()函数

> Original: [https://www.geeksforgeeks.org/php-imagecolorclosest-function/](https://www.geeksforgeeks.org/php-imagecolorclosest-function/)

**imagecolorest()**函数是 PHP 中的一个内置函数，用于获取给定图像中最接近颜色的索引。 此函数用于返回图像调色板中最接近指定 RGB 值的颜色索引。

**语法：**

```
*int* imagecolorclosest( $image, $red, $green, $blue )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$image:** it is returned by one of the image creation functions, such as imagecreatetruecolor (). It is used to create the size of the image.
*   **$red:** this parameter is used to set the value of the red component.
*   **$green:** this parameter is used to set the value of the green component.
*   **$BLUE:** this parameter is used to set the value of the blue component.

**返回值：**此函数返回图像调色板中最接近颜色的索引。

下面的程序演示了 PHP 中的**imagecolorest()**函数。

**程序 1：**

```
<?php

// Start with an image and convert it to a palette-based image
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png');

imagetruecolortopalette($image, false, 255);

//  Search closest color
$result = imagecolorclosest($image, 7, 150, 10);

$result = imagecolorsforindex($image, $result);

$result = "({$result['red']}, {$result['green']}, {$result['blue']})";

echo "Closest color: " . $result;

imagedestroy($image);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Start with an image and convert it to a palette-based image
$image = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeks-21.png');

imagetruecolortopalette($image, false, 255);

// Search RGB colors
$color = array(
    array(7, 150, 0),
    array(53, 190, 255),
    array(255, 165, 54)
);

// Loop to find the closest color to the given RGB color
foreach($color as $id => $rgb)
{
    $result = imagecolorclosest($image, $rgb[0], $rgb[1], $rgb[2]);
    $result = imagecolorsforindex($image, $result);
    $result = "({$result['red']}, {$result['green']}, {$result['blue']})";

    echo "Given color: ($rgb[0], $rgb[1], $rgb[2]) => Closest match: $result<br>";
}

imagedestroy($image);

?>
```

发帖主题：Re：Колибри0.7.8.0

**返回值：**

*   [php|getimageSize()函数](https://www.geeksforgeeks.org/php-getimagesize-function/)
*   [PHP|imageflip()11-13](https://www.geeksforgeeks.org/php-imageflip-function/)
*   [php|Imagesx()函数](https://www.geeksforgeeks.org/php-imagesx-function/)

**引用：**[http://php.net/manual/en/function.imagecolorclosest.php](http://php.net/manual/en/function.imagecolorclosest.php)