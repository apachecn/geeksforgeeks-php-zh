# PHP|disk_free_space()函数

> Original: [https://www.geeksforgeeks.org/php-disk_free_space-function/](https://www.geeksforgeeks.org/php-disk_free_space-function/)

PHP 中的 disk_free_space()函数是一个内置函数，用于返回指定目录中的空闲空间量。 函数的作用是：以字节为单位表示可用空间。

它返回文件系统或磁盘分区上的可用空间。 函数的作用是：返回以字符串形式输入的指定目录在相应文件系统或磁盘分区上的可用字节数。

**语法：**

```
float disk_free_space ( $directory )
```

**参数：**PHP 中的 disk_free_space()函数接受一个参数，即*$directory*。 此参数指定必须检查的目录。

**返回值：**它返回文件系统或磁盘分区上的可用空间。

**错误和异常**：

1.  如果文件名作为参数而不是目录给出，PHP 中的 disk_free_space()函数可能会给出不正确的结果。
2.  PHP 中的 disk_free_space()函数不适用于远程文件，它只适用于服务器文件系统可以访问的文件。

**示例：**

```
Input : disk_free_space("D:");
Output : 10969328844

Input : disk_free_space("C:");
Output : 10969327231

```

下面的程序演示了 disk_free_space()函数：

**程序 1**：

```
<?php

// specifying directory to check for free space
echo disk_free_space("D:");

?>
```

产出：

```
10969328844
```

**程序 2**：

```
<?php

// specifying directory to check for free space
echo disk_free_space("C:");

?>
```

产出：

```
10969327231
```

**引用：**
[http://php.net/manual/en/function.disk-free-space.php](http://php.net/manual/en/function.disk-free-space.php)