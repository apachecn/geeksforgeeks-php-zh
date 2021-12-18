# PHP|gmp_export()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_export-function/](https://www.geeksforgeeks.org/php-gmp_export-function/)

Gmp_export()函数是 PHP 中的一个内置函数，用于将 GMP 编号([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：对于大数)导出为二进制字符串。

**语法：**

```php
string gmp_export ( GMP $gmpnumber, int $word_size, int $options )

```

**参数：**gmp_export()函数接受三个参数，如下所示：

*   **$gmpnumber：**这是 gmp_export()函数的必需参数，它是该函数要导出的数字。
*   **$WORD_SIZE：**此参数包含每个二进制数据块中的字节数。 该参数主要与 OPTIONS 参数同时使用。 此参数的默认值为 1。
*   **$Options：**此参数的默认值为 GMP_MSW_FIRST|GMP_Native_Indian。

**返回值：**函数成功时返回字符串，失败时返回 False。

下面的程序演示了 PHP 中的 gmp_export()函数：

## PHP

```php
<?php
// PHP code implementing the gmp_export function

// The gmp_init() function creates a gmp number
// form a string or number
$number = gmp_init(16705);

echo gmp_export($number) . "\n";

?>
```

发帖主题：Re：Колибри0.7.0

```php
 AA

```

**相关文章：**

*   [PHP|gmp_add()加法大数](https://www.geeksforgeeks.org/php-gmp_add-for-adding-large-numbers/)
*   [PHP|模逆](https://www.geeksforgeeks.org/php-gmp_invert-inverse-modulo/)的 gmp_invert()
*   [PHP|gmp_rootrem()函数](https://www.geeksforgeeks.org/php-gmp_rootrem-function/)

**引用：**[http://php.net/manual/en/function.gmp-export.php](http://php.net/manual/en/function.gmp-export.php)