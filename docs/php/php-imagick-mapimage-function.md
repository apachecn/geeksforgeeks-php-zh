# PHP|Imagick mapImage()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-mapimage-function/](https://www.geeksforgeeks.org/php-imagick-mapimage-function/)

**Imagick：：mapImage()函数**是 PHP 中的一个内置函数，用于用与参考图像最接近的颜色替换图像的颜色。

**语法：**

```php
*bool* Imagick::mapImage( *Imagick* $map, *float* $dither )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$map：**此参数保存 Imagick 对象。
*   **$dither：**此参数包含决定是否添加噪波的布尔值。

**返回值：**如果成功，此函数返回 TRUE。

**错误/异常：**此函数在出错时引发 ImagickException。

下面的程序演示了 PHP 中的 Imagick：：mapImage()函数：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Create another imagick object
$imagick2 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190901195451/mattefloodfillimage.png');

// Mapping the image with noise
$imagick1->mapImage($imagick2, true);

header("Content-Type: image/jpg"); 

// Display the output image 
echo $imagick1->getImageBlob();

?>
```

**输出：**
![](img/cae6f5868ff35ee6f5fa8102c7dd9e0f.png)

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick1 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Create another imagick object
$imagick2 = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190901195451/mattefloodfillimage.png');

// Mapping the image without noise
$imagick1->mapImage($imagick2, false);

header("Content-Type: image/jpg"); 

// Display the output image 
echo $imagick1->getImageBlob();

?>
```

**输出：**
![](img/341c23823978a1d065ccbe6e1ba7d6b8.png)

**引用：**[https://www.php.net/manual/en/imagick.mapimage.php](https://www.php.net/manual/en/imagick.mapimage.php)