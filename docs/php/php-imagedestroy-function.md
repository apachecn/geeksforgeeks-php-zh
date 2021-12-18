# PHP|ImageDestroy()函数

> Original: [https://www.geeksforgeeks.org/php-imagedestroy-function/](https://www.geeksforgeeks.org/php-imagedestroy-function/)

函数**的作用是：**是 PHP 中的一个内置函数，用于销毁图像并释放与该图像相关的任何内存。

**语法：**

```php
*bool* imagedestroy( *resource* $image )
```

**参数：**此函数接受保存图像名称的单个参数**$image**。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**ImageDestroy()函数**：

**示例 1：**使用后销毁图像。

```php
<?php

// Load the png image
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123135210/geeksforgeeksinverted.png');

// Crop the image
$cropped = imagecropauto($im, IMG_CROP_BLACK);

// Convert it to a png file
header('Content-type: image/png');  
imagepng($cropped);

// Destroy the cropped image to deallocate the memory
imagedestroy($cropped);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**检查变量是否已销毁。

```php
<?php

// Load the png image
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123135210/geeksforgeeksinverted.png');

header('Content-type: image/png');

// Destroy the image to deallocate the memory
imagedestroy($im);

// Try to access the destroyed variable
imagepng($im);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.imagedestroy.php](https://www.php.net/manual/en/function.imagedestroy.php)