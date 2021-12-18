# PHP|IntlChar getUnicodeVersion()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-getunicodeversion-function/](https://www.geeksforgeeks.org/php-intlchar-getunicodeversion-function/)

**IntlChar：：getUnicodeVersion()**函数是 PHP 中的内置函数，用于获取 Unicode 版本。 Unicode 标准版本信息被填充到一个数组中。 例如，Unicode 版本 2.2.1 表示为值为[2，2，1，0]的数组。

**语法：**

```php
*array* IntlChar::getUnicodeVersion ( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含 Unicode 版本号的数组。

下面的程序演示了 PHP 中的**IntlChar：：getUnicodeVersion()**函数：

**程序：**

```php
<?php
var_dump(IntlChar::getUnicodeVersion());
?>
```

**输出：**

```php
array(4) {
  [0]=>
  int(7)
  [1]=>
  int(0)
  [2]=>
  int(0)
  [3]=>
  int(0)
}

```

**相关文章：**

*   [php|IntlChar：：iscntrl()函数](https://www.geeksforgeeks.org/php-intlchariscntrl-function/)
*   [php|IntlChar charType()函数](https://www.geeksforgeeks.org/php-intlchar-chartype-function/)
*   [php|IntlChar：：Ord()函数](https://www.geeksforgeeks.org/php-intlcharord-function/)
*   [php|IntlChar Toupper()函数](https://www.geeksforgeeks.org/php-intlchar-toupper-function/)

**引用：**[http://php.net/manual/en/intlchar.getunicodeversion.php](http://php.net/manual/en/intlchar.getunicodeversion.php)