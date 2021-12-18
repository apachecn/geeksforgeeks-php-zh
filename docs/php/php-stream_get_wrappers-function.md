# PHP|stream_get_wrappers()函数

> Original: [https://www.geeksforgeeks.org/php-stream_get_wrappers-function/](https://www.geeksforgeeks.org/php-stream_get_wrappers-function/)

Stream_get_wrappers()函数是 PHP 中的一个内置函数，用于获取正在运行的系统上可用的已注册流列表。

**语法：**

```php
*array* stream_get_wrappers( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含所有可用流名称的数组。

下面的程序演示了 PHP 中的 stream_get_wrappers()函数：

**程序 1：**

```php
<?php

// PHP program to illustrate
// stream_get_wrappers function

print_r(stream_get_wrappers());
?>
```

**输出：**

```php
Array
(
    [0] => https
    [1] => ftps
    [2] => compress.zlib
    [3] => php
    [4] => file
    [5] => glob
    [6] => data
    [7] => http
    [8] => ftp
    [9] => phar
)

```

**程序 2：**检查给定流是否可用的程序。

```php
<?php

// PHP program to illustrate
// stream_get_wrappers function

$wrapper = array (
    'https',
    'http',
    'file',
    'data',
    'GFG'
);

// Checking stream wrapper enabled or not
foreach ($wrapper as &$gfg) {
    if (in_array($gfg, stream_get_wrappers())) {
        echo $gfg . ': Enabled' . "\n";
    } else {
        echo $gfg . ": Not Enabled" . "\n";
    }
}

?>
```

**输出：**

```php
https: Enabled
http: Enabled
file: Enabled
data: Enabled
GFG: Not Enabled

```

**引用：**[http://php.net/manual/en/function.stream-get-wrappers.php](http://php.net/manual/en/function.stream-get-wrappers.php)