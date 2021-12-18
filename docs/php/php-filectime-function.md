# PHP|filectime()函数

> Original: [https://www.geeksforgeeks.org/php-filectime-function/](https://www.geeksforgeeks.org/php-filectime-function/)

PHP 中的 filectime()函数是一个内置函数，用于返回上次更改指定文件的时间。 函数的作用是：成功时以 Unix 时间戳的形式返回上次更改文件的时间，失败时以 False 的形式返回。 函数的作用是：检查 inode 更改，即权限、所有者、组或其他元数据的更新以及常规更改。

文件名作为参数传递给 filectime()函数。 将缓存 filectime()函数的结果，并使用名为 clearstatcache()的函数清除缓存。

**语法：**

```
filectime($filename)
```

**参数：**PHP 中的 filectime()函数只接受一个参数*$filename*。 它指定要检查其上次更改时间的文件。

**返回值：**如果成功，则以 Unix 时间戳的形式返回文件的最后更改时间；如果失败，则返回 False。

**错误和异常**：

1.  时间分辨率可能因文件系统不同而不同。
2.  此功能在某些 Unix 系统上不起作用，这些系统禁用了访问时间更新以提高性能。

**示例：**

```
Input : echo filectime("gfg.txt");
Output : 1525159574

Input : echo "Last changed: ".date("F d Y H:i:s.", 
                            filectime("gfg.txt"));
Output : Last changed: May 1 2018 07:26:14.

```

下面的程序演示了 filectime()函数。

**程序 1**：

```
<?php

// checking last time a file was changed
echo filectime("gfg.txt");

?>
```

产出：

```
1525159574
```

**程序 2**：

```
<?php

// checking last time a file was changed
echo filectime("gfg.txt");

// checking last time a file was changed
// and formatting the output of the date 
echo "Last changed: ".date("F d Y H:i:s.", 
                    filectime("gfg.txt"));
?>
```

产出：

```
1525159574
Last changed: May 1 2018 07:26:14.

```

**引用：**
[http://php.net/manual/en/function.filectime.php](http://php.net/manual/en/function.filectime.php)