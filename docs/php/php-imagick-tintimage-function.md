# PHP|Imagick tintImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-tintimage-function/](https://www.geeksforgeeks.org/php-imagick-tintimage-function/)

**Imagick：：tintImage()函数**是 PHP 中的一个内置函数，用于将颜色向量应用到图像的每个像素。

**语法：**

```
*bool* Imagick::tintImage( *mixed* $tint, *mixed* $opacity, *bool* $legacy = FALSE )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$tint：**此参数保存 ImagickPixel 对象或包含向量颜色的字符串。
*   **$opacity：**此参数保存 ImagickPixel 对象或包含不透明度值的浮点。 1 表示完全不透明，0 表示完全透明。
*   **$Legacy：**此参数包含一个布尔值，用于告知是否需要遗留行为。 建议将其保持为 true 以使用字符串颜色。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的**Imagick：：tintImage()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Add the tint
$imagick->tintImage('red', 1, true);

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/1b07488feecc439d99c72e6059a3c278.png)

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-9.png');

// Add the tint
$imagick->tintImage(new ImagickPixel('white'), 0.5, true);

header("Content-Type: image/png");

// Display the output image
echo $imagick->getImageBlob();

?>
```

**输出：**
![](img/5505e0837752a7bde748c229eff4e93b.png)

**引用：**[https://www.php.net/manual/en/imagick.tintimage.php](https://www.php.net/manual/en/imagick.tintimage.php)