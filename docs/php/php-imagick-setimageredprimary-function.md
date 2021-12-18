# PHP|Imagick setImageRedPrimary()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageredprimary-function/](https://www.geeksforgeeks.org/php-imagick-setimageredprimary-function/)

**Imagick：：setImageRedPrimary()函数**是 PHP 中的一个内置函数，用于设置图像的色度红色基准点。

**语法：**

```
*bool* Imagick::setImageRedPrimary( *float* $x, *float* $y )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x：**它指定红色主 x 点。
*   **$y：**它指定红色主 y 点。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面给定的程序说明了 PHP：
**程序 1：**中的**Imagick：：setImageRedPrimary()函数**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Use setImageRedPrimary() function
$imagick->setImageRedPrimary(5, 8);

// Use getImageRedPrimary() function
$result = $imagick->getImageRedPrimary();
print_r($result);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [x] => 5 [y] => 8 )
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Use setImageRedPrimary() function
$imagick->setImageRedPrimary(0.2, 0.8);

// Display the image
$imagick->setformat('png');
header("Content-Type: image/png");

echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/8a6bf34ded7fdfa47ead1d1c27e16fc5.png)

**引用：**[https://www.php.net/manual/en/imagick.setimageredprimary.php](https://www.php.net/manual/en/imagick.setimageredprimary.php)