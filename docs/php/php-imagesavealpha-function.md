# PHP|imagesavelpha()函数

> Original: [https://www.geeksforgeeks.org/php-imagesavealpha-function/](https://www.geeksforgeeks.org/php-imagesavealpha-function/)

**imagesavelpha()函数**是 PHP 中的一个内置函数，用于设置保存 PNG 图像时是否保留完整的 Alpha 通道信息。 Alpha 通道指示图像是完全透明的还是不透明的。 必须使用**imagelphablating($im，false)**禁用 Alpha 混合，才能首先保留 Alpha 通道。

**语法：**

```
*bool* imagesavealpha( *resource* $image, *bool* $save_flag )
```

**参数：**此函数接受两个参数，如上所述，如下所述：

*   **$image:** it specifies the image resources to be processed.
*   **$save_flag:** it specifies whether to save the Alpha channel.

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

下面的示例说明了 PHP 中的**imagesavelpha()函数**：

**示例 1：**在此示例中，我们将启用保存 Alpha 信息。

```
<?php

// Load the png image
$png = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Turn off alpha blending
imagealphablending($png, false);

// Add alpha as 100 to image
$transparent = imagecolorallocatealpha($png, 255, 255, 255, 100);
imagefill($png, 0, 0, $transparent);

// Set alpha flag to true so that
// alpha info is saved in the image
imagesavealpha($png, true);

// Save the image
imagepng($png, 'imagewithalphainfo.png');
imagedestroy($png);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**在此示例中，我们将禁用保存 Alpha 信息。

```
<?php

// Load the png image
$png = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Turn off alpha blending
imagealphablending($png, false);

// Add alpha as 100 to image
$transparent = imagecolorallocatealpha($png, 255, 255, 255, 100);
imagefill($png, 0, 0, $transparent);

// Set alpha flag to false so that
// alpha info is not saved in the image
imagesavealpha($png, false);

// Save the image
imagepng($png, 'imagewithoutalphainfo.png');
imagedestroy($png);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.imagesavealpha.php](https://www.php.net/manual/en/function.imagesavealpha.php)