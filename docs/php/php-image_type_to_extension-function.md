# PHP|IMAGE_TYPE_TO_EXTENSION()函数

> Original: [https://www.geeksforgeeks.org/php-image_type_to_extension-function/](https://www.geeksforgeeks.org/php-image_type_to_extension-function/)

**image_type_to_tension()函数**是 PHP 中的一个内置函数，用于获取图像类型的文件扩展名。 此函数可在任何 PHP 版本 Silimar 或高于 5.2.0 的版本中找到。

**语法：**

```
*string* image_type_to_extension( *int* $imagetype, *bool* $include_dot )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$imageType:** it takes an integer value as the first parameter, which is one of the imageType_XXX constants. For example: imageType_gif, imageType_JPEG, etc.
*   **$include_dot:** the second parameter takes a Boolean value to determine whether to precede the extension with a dot. In this function, the default value is set to TRUE.

**返回值：**此函数返回与给定图像类型对应的扩展名关联的字符串值。

下面的程序演示了 PHP 中的 image_type_to_tension()函数：

**程序 1：**

```
<?php 

// Extension with dot
echo image_type_to_extension(IMAGETYPE_PNG, TRUE) . "\n";

// Extension without dot
echo image_type_to_extension(IMAGETYPE_PNG, FALSE);

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create image instance
$image = imagecreatetruecolor(100, 100);

// Creates an image with .png extension
imagepng($image, './test' . 
        image_type_to_extension(IMAGETYPE_PNG));

// Free any memory associated with image
imagedestroy($image);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.image-type-to-extension.php](https://www.php.net/manual/en/function.image-type-to-extension.php)