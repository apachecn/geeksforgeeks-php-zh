# PHP|stream_is_local()函数

> Original: [https://www.geeksforgeeks.org/php-stream_is_local-function/](https://www.geeksforgeeks.org/php-stream_is_local-function/)

STREAM_IS_LOCAL()函数是 PHP 中的一个内置函数，用于检查流是本地流还是 URL。

**语法：**

```php
*bool* stream_is_local( $stream )
```

**参数：**此函数接受单个参数*$stream*，用于指定要检查的流。

**返回值：**此函数成功时返回 True，失败时返回 False。

下面的程序演示了 PHP 中的 stream_is_local()函数：

**程序 1：**

```php
<?php

// PHP program to illustrate
// stream_is_local function
$strm = "https://www.geeksforgeeks.org";

$res = stream_is_local($strm);

// Print result
var_dump($res);
?>
```

**输出：**

```php
bool(false)

```

**程序 2：**打印函数返回的数组长度的程序。

```php
<?php

// PHP program to illustrate 
// stream_is_local function
$stream1 = '/geeks.jpg'; // local
$stream2 = 'file://geeks.jpg'; // local
$stream3 = 'http://geeksforgeeks.org'; // non local stream

// Checking all strings and print result
$local = stream_is_local($stream1);
var_dump($local);

$shouldbelocal = stream_is_local($stream2);
var_dump($shouldbelocal);

$remote = stream_is_local($stream3);
var_dump($remote);
?>
```

**输出：**

```php
bool(true)
bool(false)
bool(false)

```

**引用：**[http://php.net/manual/en/function.stream-is-local.php](http://php.net/manual/en/function.stream-is-local.php)