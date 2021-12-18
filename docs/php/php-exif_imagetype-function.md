# PHP|exif_imageType()函数

> Original: [https://www.geeksforgeeks.org/php-exif_imagetype-function/](https://www.geeksforgeeks.org/php-exif_imagetype-function/)

**exif_imageType()函数**是 PHP 中的一个内置函数，用于确定图像的类型。
**语法：**和

```
*int* exif_imagetype( *string* $filename )
```

**参数：**此函数接受单个参数**$filename**，该参数保存图像的名称或 URL。
**返回值：**此函数返回一个整数，对应于下面给出的 ImageType 常量之一：

*   ImageType_GIF(1)
*   ImageType_JPEG(2)
*   ImageType_png(3)
*   ImageType_SWF(4)
*   ImageType_PSD(5)
*   ImageType_BMP(6)
*   ImageType_TIFF_II(7)
*   ImageType_TIFF_mm(8)
*   ImageType_JPC(9)
*   ImageType_JP2(10)
*   ImageType_JPX(11)
*   ImageType_JB2(12)
*   ImageType_SWC(13)
*   ImageType_IFF(14)
*   ImageType_WBMP(15)
*   ImageType_xbm(16)
*   ImageType_ICO(17)
*   ImageType_WebP(18)

下面给出的程序说明 PHP 中的**EXIF_ImageType()函数**：
**程序 1：**在此示例中，我们将检查图像文件的格式。

## PHP

```
<?php
// Load an image from PNG URL
$type = exif_imagetype(
'https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-13.png');

echo $type;
?>
```

发帖主题：Re：Колибри0.7.8.0

```
3 // which corresponds to IMAGETYPE_PNG
```

**程序 2：**在本例中，我们将检查图像文件是否受支持。

## PHP

```
<?php
// Load an image from JPEG URL
$type = exif_imagetype(
'https://media.geeksforgeeks.org/wp-content/uploads/20200123100652/geeksforgeeks12.jpg');

if($type > 0 || $type < 19)
{
    echo 'This is a supported image format.';
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```
This is a supported image format.
```

**引用：**[https://www.php.net/manual/en/function.exif-imagetype.php](https://www.php.net/manual/en/function.exif-imagetype.php)