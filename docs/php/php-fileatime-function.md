# PHP|fileatime()函数

> Original: [https://www.geeksforgeeks.org/php-fileatime-function/](https://www.geeksforgeeks.org/php-fileatime-function/)

PHP 中的 fileatime()函数是一个内置函数，用于返回指定文件的上次访问时间。 函数的作用是：如果成功，则以 Unix 时间戳的形式返回文件的最后访问时间；如果失败，则返回 False。

文件名作为参数传递给 fileatime()函数。 缓存 fileatime()函数的结果，并使用名为 clearstatcache()的函数清除缓存。

**语法：**

```
fileatime($filename)
```

**参数：**PHP 中的 fileatime()函数只接受一个参数*$filename*。 它指定要检查其上次访问时间的文件。

**返回值：**成功时以 Unix 时间戳形式返回文件的最后访问时间，失败时以 False 形式返回。

**错误和异常**：

1.  时间分辨率可能因文件系统不同而不同。
2.  此功能在某些 Unix 系统上不起作用，这些系统禁用了访问时间更新以提高性能。

**示例：**

```
Input : echo fileatime("gfg.txt");
Output : 1525159574

Input : echo "Last accessed: ".date("F d Y H:i:s.", 
                              fileatime("gfg.txt"));
Output : Last accessed: May 1 2018 07:26:14.

```

下面的程序演示了 fileatime()函数。

**程序 1**：

```
<?php

// checking last accessed time of a file 
echo fileatime("gfg.txt");

?>
```

产出：

```
1525159574
```

**程序 2**：

```
<?php

// checking last accessed time of a file 
echo fileatime("gfg.txt");

//checking last accessed time of a file
// and formatting the output of the date 
echo "Last accessed: ".date("F d Y H:i:s.", 
                     fileatime("gfg.txt"));
?>
```

产出：

```
1525159574
Last accessed: May 1 2018 07:26:14.

```

**引用：**
[http://php.net/manual/en/function.fileatime.php](http://php.net/manual/en/function.fileatime.php)