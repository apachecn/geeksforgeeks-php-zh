# PHP|Imagick setImageBluePrimary()函数

> Original: [https://www.geeksforgeeks.org/php-imagick-setimageblueprimary-function/](https://www.geeksforgeeks.org/php-imagick-setimageblueprimary-function/)

**Imagick：：setImageBluePrimary()函数**是 PHP 中的一个内置函数，用于设置图像的色度蓝色基准点。

**语法：**

```php
*bool* Imagick::setImageBluePrimary( *float* $x, *float* $y )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$x：**它指定蓝色主 x 点。
*   **$y：**它指定蓝色主要 y 点。

**返回值：**如果成功，此函数返回 TRUE。

**异常：**此函数在出错时引发 ImagickException。

下面的程序说明了 PHP 中的**Imagick：：setImageBluePrimary()函数**：

**程序 1：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Use setImageBluePrimary() function
$imagick->setImageBluePrimary(10, 10);

// Use getImageBluePrimary() function
$result = $imagick->getImageBluePrimary();

print_r($result);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array ( [x] => 10 [y] => 10 )
```

**程序 2：**

```php
<?php

// Create a new imagick object
$imagick = new Imagick(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Use setImageBluePrimary() function
$imagick->setImageBluePrimary(0.2, 0.2);

// Display the image
$imagick->setformat('png');

header("Content-Type: image/png");
echo $imagick->getImageBlob();
?>
```

**输出：**
![](img/e8edb1819f0f052f33e7534331091e74.png)

**引用：**[https://www.php.net/manual/en/imagick.setimageblueprimary.php](https://www.php.net/manual/en/imagick.setimageblueprimary.php)