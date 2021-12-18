# PHP|imagegd2()函数

> Original: [https://www.geeksforgeeks.org/php-imagegd2-function/](https://www.geeksforgeeks.org/php-imagegd2-function/)

函数**imagegd2()**是 PHP 中的一个内置函数，用于将 GD2 图像输出到浏览器或文件。 这对于将任何其他图像类型转换为 GD2 非常有用。 函数**imagecreatefrom mgd2()**可用于进一步读取 GD2 图像。

**语法：**

```
*bool* imagegd2( *resource* $image, *float* $to, 
             *int* $chunk_size, *int* $type )
```

**参数：**此函数接受四个参数，如上所述，如下所述：

*   **$image:** it specifies the image to be processed.
*   **$to (optional):** it specifies the path where the file is saved.
*   **$CHUNK_SIZE (optional):** it specifies the size of the block.
*   **$type (optional):** it specifies the type of compression to use, which can be one of *IMG_GD2_RAW* or *IMG_GD2_COMPRESSED* .

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**异常：**此函数在出错时抛出异常。

下面的示例说明了 PHP 中的**imagegd2()函数**：

**示例 1：**查看 GD2 文件。

```
<?php

// Create a blank image and add text
$im = imagecreatetruecolor(200, 200);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 0, 30, 30,  "GeeksforGeeks", $text_color);

// Output the image as string
imagegd2($im);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**将图像转换为 GD2。

```
<?php

// Create a image from png
$im = imagecreatefrompng(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Convert into GD2 and save to the same folder
imagegd2($im, 'geeksforgeeks.gd2');
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.imagegd2.php](https://www.php.net/manual/en/function.imagegd2.php)