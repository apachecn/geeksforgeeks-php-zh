# PHP|imagegd()函数

> Original: [https://www.geeksforgeeks.org/php-imagegd-function/](https://www.geeksforgeeks.org/php-imagegd-function/)

函数**imagegd()**是 PHP 中的一个内置函数，用于将 GD 图像输出到浏览器或文件。 这对于将任何其他图像类型转换为 gd 非常有用。 *imagecreatefrom mgd()*函数可用于进一步读取 gd 图像。

**语法：**

```
*bool* imagegd( *resource* $image, *float* $to)
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$image：**它指定要处理的图像。
*   **$to(可选)：**它指定保存文件的路径。

**返回值：**此函数成功时返回 TRUE，失败时返回 FALSE。

**异常：**此函数在出错时抛出异常。

下面给出的程序说明了 PHP 中的**imagegd()函数**：
**程序 1(查看 GD 文件)：**

```
<?php
// Create a blank image and add text
$im = imagecreatetruecolor(100, 100);
$text_color = imagecolorallocate($im, 10, 10, 51);
imagestring($im, 0, 20, 20,  "GeeksforGeeks", $text_color);

// Output the image as string
imagegd($im);
?>
```

发帖主题：Re：Колибри0.7.0

```
This will output the image in the form of string as gd isn't supported in browser.
```

**程序 2(将图像转换为 gd)：**

```
<?php
// Create a image from png
$image = imagecreatefrompng('https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

// Convert into GD and save to the same folder
imagegd($image, 'geeksforgeeks.gd');
?>
```

发帖主题：Re：Колибри0.7.0

```
This will save a image with name geeksforgeeks.gd in the same folder.
```

**引用：**[https://www.php.net/manual/en/function.imagegd.php](https://www.php.net/manual/en/function.imagegd.php)