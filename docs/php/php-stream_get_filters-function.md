# PHP|STREAM_GET_FILTERS()函数

> Original: [https://www.geeksforgeeks.org/php-stream_get_filters-function/](https://www.geeksforgeeks.org/php-stream_get_filters-function/)

函数的作用是：获取已注册的流过滤器列表。

**语法：**

```
*array* stream_get_filters( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含所有可用流过滤器名称的数组。

下面的程序演示了 PHP 中的 stream_get_filter()函数：

**程序 1：**

```
<?php

// PHP program to illustrate
// stream_get_filter function

$streamlist = stream_get_filters();
print_r($streamlist);
?>
```

**输出：**

```
Array
(
    [0] => zlib.*
    [1] => string.rot13
    [2] => string.toupper
    [3] => string.tolower
    [4] => string.strip_tags
    [5] => convert.*
    [6] => consumed
    [7] => dechunk
    [8] => convert.iconv.*
)

```

**程序 2：**打印按函数返回的过滤器数量的程序。

```
<?php

// PHP program to illustrate
// stream_get_filter function

$res = stream_get_filters();

$count = sizeof($res);

// Print result
echo "Total Available Filters = " . $count;
?>
```

**输出：**

```
Total Available Filters = 9

```

**引用：**[http://php.net/manual/en/function.stream-get-filters.php](http://php.net/manual/en/function.stream-get-filters.php)