# PHP|IntlChar 枚举 CharTypes()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-enumchartypes-function/](https://www.geeksforgeeks.org/php-intlchar-enumchartypes-function/)

**IntlChar：：EumpCharTypes()**函数是 PHP 中的一个内置函数，用于给出所有代码点及其 Unicode 常规类别的目录。 在所有代码点中，所有的编目都非常高效。 对于枚举所有分配的代码点和构建数据结构等，这将非常有用。 对于具有给定一般类别和字符类型的连续范围的每个代码点，调用回调函数。 相邻的范围可以有不同的类型。 Unicode 标准保证类型的数值为 0 到 31。

**语法：**

```
*void* IntlChar::enumCharTypes( $callback )
```

**参数：**此函数接受单个参数**$callback**。 对于具有相同常规类别的每个连续的代码点范围，将调用该函数。 回调函数包含下面列出的三个参数：

*   **INTEGER$START:** it is the starting code point.
*   **Integer $end:** it is the end code point.
*   **Integer $name:** Category Type (one of the IntlChar::CHAR_CATEGORY_* constants)

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的**IntlChar：：EnumerCharTypes()**函数：

**程序：**

```
<?php

// PHP program to uses IntlChar::enumCharTypes()
// function
IntlChar::enumCharTypes(function($start, $end, $type) {
    printf("U+%04x through U+%04x are in category %d\n",
                                   $start, $end, $type);
});

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/intlchar.enumchartypes.php](https://www.php.net/manual/en/intlchar.enumchartypes.php)