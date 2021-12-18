# PHP|filemtime()函数

> Original: [https://www.geeksforgeeks.org/php-filemtime-function/](https://www.geeksforgeeks.org/php-filemtime-function/)

PHP 中的 filemtime()函数是一个内置函数，用于返回指定文件内容被修改的最后时间。 函数的作用是：成功时以 Unix 时间戳的形式返回上次更改文件的时间，失败时以 False 的形式返回。

文件名作为参数传递给 filemtime()函数。 将缓存 filemtime()函数的结果，并使用名为 clearstatcache()的函数清除缓存。

**语法：**

```php
filemtime($filename)
```

**参数：**PHP 中的 filemtime()函数只接受一个参数*$filename*。 它指定要检查的文件。

**返回值：**成功时返回文件内容的最后修改时间，失败时返回 False。

**错误和异常**：

1.  时间分辨率可能因文件系统不同而不同。
2.  此功能在某些 Unix 系统上不起作用，这些系统禁用了访问时间更新以提高性能。

**示例：**

```php
Input : echo filemtime("gfg.txt");
Output : 1525159574

Input : echo "Last modified: ".date("F d Y H:i:s.", 
                              filemtime("gfg.txt"));
Output : Last modified: May 1 2018 07:26:14.

```

下面的程序演示了 filemtime()函数。

**程序 1**：

```php
<?php

// checking last time the contents
// of a file were changed
echo filemtime("gfg.txt");

?>
```

产出：

```php
1525159574
```

**程序 2**：

```php
<?php

// checking last time the contents
// of a file were changed
echo filemtime("gfg.txt");

// checking last time the contents of
// a file were changed and formatting
// the output of the date 
echo "Last modified: ".date("F d Y H:i:s.", 
                      filemtime("gfg.txt"));
?>
```

产出：

```php
1525159574
Last modified: May 1 2018 07:26:14.

```

**引用：**
[http://php.net/manual/en/function.filemtime.php](http://php.net/manual/en/function.filemtime.php)