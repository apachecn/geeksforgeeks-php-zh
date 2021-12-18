# PHP|image_type_to_mime_type()函数

> Original: [https://www.geeksforgeeks.org/php-image_type_to_mime_type-function/](https://www.geeksforgeeks.org/php-image_type_to_mime_type-function/)

Image_type_to_mime_type()函数是 PHP 中的内置函数，用于获取由其他不同函数返回的 imageType 的 MimeType，如 getimagesize()、EXIF_READ_DATA()、EXIF_TMBILE()、EXIF_ImageType()等。
**MIME**代表**多用途 Internet 邮件扩展**。 MIME 类型表单是对 Internet 上的文件类型进行分类的标准方式。 诸如 Web 服务器和浏览器之类的 Internet 程序都有 MIME 类型列表，因此它们可以以相同的方式传输相同类型的文件，无论它们运行的是哪种操作系统。

**语法：**

```php
*string* image_type_to_mime_type( *int* $imagetype )
```

**参数：**此函数接受单个参数**$imageType**，该参数保存 imageType_XXX 常量(如 imageType_gif、imageType_JPEG、imageType_png 等)的整数值。

**返回值：**此函数返回给定 imageType 常量的 Mime 类型字符串。

下面是所有返回值的详尽列表。

| 图像类型 | 返回值 |
| --- | --- |
| ImageType_GIF | 图像/gif |
| ImageType_JPEG | 图像/jpeg |
| ImageType_PNG | 图像/PNG |
| ImageType_SWF | 应用/x-冲击波-闪存 |
| ImageType_PSD | 图像/PSD |
| ImageType_BMP | 图像/BMP |
| 发帖主题：Re：Колибри0.7.8.0 | 图像/TIFF |
| ImageType_TIFF_mm(摩托罗拉字节顺序) | 图像/TIFF |
| ImageType_JPC | 应用程序/八位元-流 |
| ImageType_JP2 | 图像/JP2 |
| ImageType_JPX | 应用程序/八位元-流 |
| ImageType_JB2 | 应用程序/八位元-流 |
| ImageType_SWC | 应用/x-冲击波-闪存 |
| ImageType_IFF | IMAGE/IFF |
| ImageType_WBMP | Image/vnd.wap.wbmp |
| ImageType_xbm | Image/xbm |
| ImageType_ICO | Image/vnd.microsoft.icon |
| ImageType_WebP | 图像/WebP |

下面的程序演示了 PHP 中的 image_type_to_mime_type()函数：

**程序 1：**

```php
<?php
echo image_type_to_mime_type(IMAGETYPE_PNG);
?>
```

发帖主题：Re：Колибри0.7.0

```php
image/png
```

**程序 2：**

```php
<?php
echo image_type_to_mime_type(IMAGETYPE_JPEG);
?>
```

发帖主题：Re：Колибри0.7.0

```php
image/jpeg
```

**引用：**[https://www.php.net/manual/en/function.image-type-to-mime-type.php](https://www.php.net/manual/en/function.image-type-to-mime-type.php)