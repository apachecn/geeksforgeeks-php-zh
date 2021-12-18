# PHP|fileperms()函数

> Original: [https://www.geeksforgeeks.org/php-fileperms-function/](https://www.geeksforgeeks.org/php-fileperms-function/)

PHP 中的 fileperms()函数是一个内置函数，用于返回授予文件或目录的权限。 必须检查其权限的文件的文件名作为参数发送给该函数，如果成功，它将以数字的形式返回授予该文件的权限，如果失败，则返回 False 的形式。

将缓存 fileperms()函数的结果，并使用名为 clearstatcache()的函数清除缓存。

**语法：**

```
fileperms($filename)
```

**参数：**PHP 中的 fileperms()函数接受一个参数*$filename*。 它指定要检查其权限的文件的文件名。

**返回值：**成功时返回文件的权限，失败时返回 False。

**错误和异常**：

1.  如果在 fileperms()函数之前使用了 mkdir()或 chmod()函数，则每次调用 fileperms()函数之前都需要调用 clearstatcache()函数。
2.  如果多次使用 fileperms()函数，则必须清除缓冲区。
3.  函数的作用是：在出现故障时发出 E_WARNING。

**示例：**

```
Input : fileperms("gfg.txt");
Output : 33206

Input : substr(sprintf("%o", fileperms("gfg.txt")), -4);
Output : 0644

```

下面的程序说明了 fileperms()函数。

**程序 1**：

```
<?php

// file permissions are displayed
// using fileperms() function
echo fileperms("gfg.txt");

?>
```

产出：

```
33206
```

**程序 2**：

```
<?php

// file permissions are displayed in
// octal format using fileperms() function
echo substr(sprintf("%o", fileperms("gfg.txt")), -4);

?>
```

产出：

```
0644
```

**引用：**
[http://php.net/manual/en/function.fileperms.php](http://php.net/manual/en/function.fileperms.php)