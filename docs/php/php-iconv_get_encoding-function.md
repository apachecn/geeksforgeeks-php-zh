# PHP|iconv_get_coding()函数

> Original: [https://www.geeksforgeeks.org/php-iconv_get_encoding-function/](https://www.geeksforgeeks.org/php-iconv_get_encoding-function/)

函数是 PHP 中的内置函数，用于检索 iconv 扩展的内部配置变量。

**语法：**

```php
*mixed* iconv_get_encoding( $type = "all" )
```

**参数：**此函数接受单个参数**$type**。 $TYPE 参数值为：

*   比分相同 / 完全 / 全然地 / 越发
*   输入编码
*   输出编码
*   内部编码

**返回值：**此函数成功时返回内部配置变量的当前值，失败时返回 False。

下面的程序演示了 PHP 中的 iconv_get_coding()函数：

**程序：**

```php
<?php

// Use iconv_set_encoding() function
// with encoding parameter
iconv_set_encoding("input_encoding", "UTF-8");
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("output_encoding", "ISO-8859-1"); 

var_dump(iconv_get_encoding('all'));

?>
```

**输出：**

```php
array(3) {
  ["input_encoding"]=>
  string(5) "UTF-8"
  ["output_encoding"]=>
  string(10) "ISO-8859-1"
  ["internal_encoding"]=>
  string(5) "UTF-8"
}

```

**引用：**[https://www.php.net/manual/en/function.iconv-get-encoding.php](https://www.php.net/manual/en/function.iconv-get-encoding.php)