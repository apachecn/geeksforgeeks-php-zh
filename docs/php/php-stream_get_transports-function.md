# PHP|stream_get_transports()函数

> Original: [https://www.geeksforgeeks.org/php-stream_get_transports-function/](https://www.geeksforgeeks.org/php-stream_get_transports-function/)

Stream_get_transports()函数是 PHP 中的一个内置函数，用于获取已注册套接字传输的列表。 此函数返回包含所有可用套接字名称的索引数组。

**语法：**

```php
*array* stream_get_transports( void )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含所有可用套接字传输名称的数组。

下面的程序演示了 PHP 中的 stream_get_transports()函数：

**程序 1：**

```php
<?php

// PHP program to illustrate
// stream_get_transports function

print_r(stream_get_transports());
?>
```

**输出：**

```php
Array
(
    [0] => tcp
    [1] => udp
    [2] => unix
    [3] => udg
    [4] => ssl
    [5] => tls
    [6] => tlsv1.0
    [7] => tlsv1.1
    [8] => tlsv1.2
)

```

**程序 2：**检查运输工具是否可用的程序。

```php
<?php

// PHP program to illustrate
// stream_get_transports function

$wrapper = array (
    'tcp',
    'unix',
    'file',
    'ssl',
    'GFG'
);

// Checking socket transport enabled or not
foreach ($wrapper as &$gfg) {
    if (in_array($gfg, stream_get_transports())) {
        echo $gfg . ': Enabled' . "\n";
    } else {
        echo $gfg . ": Not Enabled" . "\n";
    }
}

?>
```

**输出：**

```php
tcp: Enabled
unix: Enabled
file: Not Enabled
ssl: Enabled
GFG: Not Enabled

```

**引用：**[http://php.net/manual/en/function.stream-get-transports.php](http://php.net/manual/en/function.stream-get-transports.php)