# PHP|imagesetstyle()函数

> Original: [https://www.geeksforgeeks.org/php-imagesetstyle-function/](https://www.geeksforgeeks.org/php-imagesetstyle-function/)

**imagesetstyle()函数**是 PHP 中的一个内置函数，用于设置所有线条绘制函数(如*imageline()*或*imagepolygon()*)使用的样式。

**语法：**

```php
*bool* imagesetstyle( *resource* $image, *array* $style )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$image：**它指定要处理的图像资源。
*   **$style：**它指定像素颜色的数组。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面给出的程序说明了 PHP 中的**imagesetstyle()函数**：
**程序 1(在图像上绘制)：**

```php
<?php
// Load the png image
$image = imagecreatefrompng(
    'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Prepare the colors
$red = imagecolorallocate($image, 255, 0, 0);
$green   = imagecolorallocate($image, 0, 255, 0);

// Draw a dashed line, 5 red pixels, 5 white pixels
$style = array($red, $red, $red, $red, $red, $green, $green, $green, $green, $green);
imagesetstyle($image, $style);
imageline($image, 0, 100, 800, 100, IMG_COLOR_STYLED);

// Output image to the browser
header('Content-type: image/png');
imagepng($image);
?>
```

**输出：**
![](img/7b9a52abd2cb981f8b2537c5e983283d.png)

**程序 2(在空白图纸上绘图)：**

```php
<?php
//Create a blank image
$image = imagecreatetruecolor(700, 200);

// Set the background color of image
$background_color = imagecolorallocate($image, 255, 255, 255);

// Fill background with above selected color
imagefill($image, 0, 0, $background_color);

// Prepare the colors
$red = imagecolorallocate($image, 255, 0, 0);
$green = imagecolorallocate($image, 0, 255, 0);

// Draw a dashed line, 7 red pixels, 3 white pixels
$style = array($red, $red, $red, $red, $red, $ren, $red, $green, $green, $green);
imagesetstyle($image, $style);

// Set the vertices of polygon
$values = array(
    150, 150,
    450, 150,
    150, 50,
);

// Draw the polygon
imagepolygon($image, $values, 3, IMG_COLOR_STYLED);

// Output image to the browser
header('Content-type: image/png');
imagepng($image);
?>
```

**输出：**
![](img/d36ebef4f2f9dff0c0a754d59376e5b9.png)

**引用：**[https://www.php.net/manual/en/function.imagesetstyle.php](https://www.php.net/manual/en/function.imagesetstyle.php)