# PHP|DISK_TOTAL_SPACE()函数

> Original: [https://www.geeksforgeeks.org/php-disk_total_space-function/](https://www.geeksforgeeks.org/php-disk_total_space-function/)

PHP 中的 DISK_TOTAL_SPACE()函数是一个内置函数，用于返回指定目录的总空间。 函数的作用是：以字节为单位表示总空间。 它返回文件系统或磁盘分区上的总空间。

函数的作用是：返回指定目录的相应文件系统或磁盘分区上的总字节数，以字符串形式输入。

**语法：**

```
*float* disk_total_space ( string $directory )
```

**参数：**PHP 中的 DISK_TOTAL_SPACE()函数只接受一个参数*$DIRECTORY*，即 DIRECTORY。

**返回值：**它返回文件系统或磁盘分区上的总空间。

**错误和异常**：

1.  如果文件名作为参数而不是目录给出，PHP 中的 disk_total_space()函数可能会给出不正确的结果。
2.  PHP 中的 DISK_TOTAL_SPACE()函数不适用于远程文件，它只适用于服务器文件系统可以访问的文件。

**示例：**

```
Input : disk_total_space("D:");
Output : 10969328844798729

Input : disk_total_space("C:");
Output : 104379834795739795 

```

以下程序说明了 DISK_TOTAL_SPACE()函数：

**程序 1**：

```
<?php

// specifying directory to check for total space
echo disk_total_space("D:");

?>
```

产出：

```
10969328844798729
```

**程序 2**：

```
<?php

// specifying directory to
// check for total space
$space = disk_total_space("C:");

echo "C: drive has a total capacity
                    of $space bytes.";

?>
```

产出：

```
C: drive has a total capacity of 104379834795739795 bytes.

```

**引用：**
[http://php.net/manual/en/function.disk-total-space.php](http://php.net/manual/en/function.disk-total-space.php)