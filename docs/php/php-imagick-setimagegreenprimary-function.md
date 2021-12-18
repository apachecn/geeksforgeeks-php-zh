# PHP|Imagick setImageGreenPrimary()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimagegreenprimary-function/](https://www.geeksforgeeks.org/php-imagick-setimagegreenprimary-function/)

**Imagick：：setImageGreenPrimary()函数**是 PHP 中的一个内置函数，用于设置图像的色度绿色基准点。

**语法：**

```
*bool* Imagick::setImageGreenPrimary( *float* $x, *float* $y )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x：**它指定绿色的主 x 点。
*   **$y：**它指定绿色主要 y 点。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageGreenPrimary()函数**：

**程序 1：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/20190823154611/geeksforgeeks24.png');

// Use setImageGreenPrimary() function
$imagick->setImageGreenPrimary(9, 11);

// Use getImageGreenPrimary() function
$result = $imagick->getImageGreenPrimary();
print_r($result);
?>
```

发帖主题：Re：Колибри0.7.0

```
Array ( [x] => 9 [y] => 11 )
```

**程序 2：**

```
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Use setImageGreenPrimary() function
$imagick->setImageGreenPrimary(0.2, 0.8);

// Display the image
$imagick->setformat('png');
header("Content-Type: image/png");

echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/c59fdbea4863829702798a80d9d8d464.png)

**引用：**[https://www.php.net/manual/en/imagick.setimagegreenprimary.php](https://www.php.net/manual/en/imagick.setimagegreenprimary.php)