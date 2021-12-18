# PHP|imagetypes()函数

> Original: [https://www.geeksforgeeks.org/php-imagetypes-function/](https://www.geeksforgeeks.org/php-imagetypes-function/)

Imagetypes()函数是 PHP 中的内置函数，用于返回 PHP 内置安装库支持的图像类型。

**语法：**

```
int imagetypes( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回 PHP 链接的 GD 版本支持的图片格式对应的位域。 此函数返回以下位：img_bmp、img_gif、img_jpg、img_png、img_wbmp、img_xPM、img_webp。

下面的程序演示了 PHP 中的 imagetypes()函数：

**程序 1：**

```
<?php
if (imagetypes() & IMG_PNG) {
    echo "PNG Support is enabled";
}
else {
    echo "Not supported image type.";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php
if (imagetypes() & IMG_JPEG) {
    echo "JPEG Support is enabled";
}
else {
    echo "Not supported image type.";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**相关文章：**

*   [PHP|imagegif()11-13](https://www.geeksforgeeks.org/php-imagegif-function/)
*   [php|Imagecolorexact()函数](https://www.geeksforgeeks.org/php-imagecolorexact-function/)

**引用：**[http://php.net/manual/en/function.imagetypes.php](http://php.net/manual/en/function.imagetypes.php)