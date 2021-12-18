# PHP|gd_info()函数

> Original: [https://www.geeksforgeeks.org/php-gd_info-function/](https://www.geeksforgeeks.org/php-gd_info-function/)

**gd_info()**函数是 PHP 中的内置函数，用于检索有关当前安装的 GD 库的信息。 此函数返回有关已安装的 GD 库的版本和功能的信息。

**语法：**

```php
*array* gd_info( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含已安装 GD 库信息的关联数组。
此函数返回的信息如下所示：

*   **GD 版本：**它是描述安装的 libgd 版本的字符串值。
*   **FreeType 支持：**它是一个布尔值。 如果安装了 FreeType 支持，则为 True。
*   **FreeType Linkage：**它是描述 FreeType 链接方式的字符串。 期望值为：使用 freetype、使用 TTF 库和使用未知库。 只有当 FreeType 支持评估为 true 时，才会定义此元素。
*   **T1Lib 支持：**它是布尔值。 如果包含 T1Lib 支持，则为 True。
*   **GIF 读取支持：**它是布尔值。 如果包含读取 GIF 图像支持，则返回 True。
*   **GIF 创建支持：**它是一个布尔值。 如果包含对创建 GIF 图像支持，则返回 True。
*   **JPEG 支持：**它是一个布尔值。 如果包含 JPEG 支持，则返回 True。
*   **PNG 支持：**它是一个布尔值。 如果包含 PNG 支持，则返回 True。
*   **WBMP 支持：**它是一个布尔值。 如果包含 WBMP 支持，则返回 True。
*   **XBM 支持：**它是一个布尔值。 如果包含 XBM 支持，则返回 True。
*   **WebP 支持：**它是一个布尔值。 如果包含 WebP 支持，则返回 True。

下面的程序演示了 PHP 中的**gd_info()**函数：

**程序：**

```php
<?php
var_dump(gd_info());
?>
```

发帖主题：Re：Колибри0.7.0

```php
array(12) { 
    ["GD Version"]=> string(26) "bundled (2.1.0 compatible)" 
    ["FreeType Support"]=> bool(true) 
    ["FreeType Linkage"]=> string(13) "with freetype" 
    ["GIF Read Support"]=> bool(true) 
    ["GIF Create Support"]=> bool(true) 
    ["JPEG Support"]=> bool(true) 
    ["PNG Support"]=> bool(true) 
    ["WBMP Support"]=> bool(true) 
    ["XPM Support"]=> bool(true) 
    ["XBM Support"]=> bool(true) 
    ["WebP Support"]=> bool(true) 
    ["JIS-mapped Japanese Font Support"]=> bool(false) 
} 

```

**相关文章：**

*   [PHP|getimagesize()函数](https://www.geeksforgeeks.org/php-getimagesize-function/)
*   [PHP|imagecolorat()函数](https://www.geeksforgeeks.org/php-imagecolorat-function/)

**引用：**[http://php.net/manual/en/function.gd-info.php](http://php.net/manual/en/function.gd-info.php)