# PHP|imagegammacorrect()函数

> Original: [https://www.geeksforgeeks.org/php-imagegammacorrect-function/](https://www.geeksforgeeks.org/php-imagegammacorrect-function/)

**imagegammacorrect()函数**是 PHP 中的一个内置函数，用于在给定输入和输出 Gamma 的情况下对给定图像应用 Gamma 校正。

**语法：**

```
*bool* imagegammacorrect( *resource* $image, *float* $inputgamma, *float* $outputgamma )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$image：**它指定要处理的图像。
*   **$inputGamma：**它指定输入 Gamma。
*   **$outputGamma：**它指定输出 Gamma。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**异常：**此函数在出错时抛出异常。

下面给出的程序说明了 PHP 中的**imagegammacorrect()函数**：
**程序 1：**

```
<?php
// Create an image
$im = imagecreatefrompng('https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Change the image gamma
imagegammacorrect($im, 3, 1.3);

// Output to browser
header('Content-Type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/1a1e2910f12cb24c17315e50e26c0fbf.png)

**程序 2：**

```
<?php
// Create an empty image
$im = imagecreatetruecolor(800, 250);

// Set the background to be light blue
imagefilledrectangle($im, 0, 0, 800, 250, imagecolorallocate($im, 0, 0, 180));

// Add text using a font from local
imagefttext($im, 80, 0, 50, 130, imagecolorallocate($im, 0, 150, 0), './Pacifico.ttf', 'GeeksforGeeks');

// Change the image gamma
imagegammacorrect($im, 3, 1.3);

// Output to browser
header('Content-Type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

**输出：**
![](img/a6673935f935207e652dbae17eb69646.png)

**引用：**[https://www.php.net/manual/en/function.imagegammacorrect.php](https://www.php.net/manual/en/function.imagegammacorrect.php)