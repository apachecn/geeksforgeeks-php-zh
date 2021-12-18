# PHP|lstat()函数

> Original: [https://www.geeksforgeeks.org/php-lstat-function/](https://www.geeksforgeeks.org/php-lstat-function/)

PHP 中的 lstat()函数用于返回有关文件或符号链接的信息。 它收集作为参数发送给 lstat()函数的文件的统计信息。 此函数返回一个数组，其中包含有关以下元素的信息：

*   [0]或[dev]-设备号
*   [1]或[ino]-信息节点号
*   [2]或[模式]-信息节点保护模式
*   [3]或[nlink]-链接数
*   [4]或[uid]-所有者的用户 ID
*   [5]或[gid]-所有者的组 ID
*   [6]或[rdev]-信息节点设备类型
*   或以字节为单位发送给您
*   [8]或[atime]-上次访问(作为 Unix 时间戳)
*   [9]或[mtime]-上次修改时间(作为 Unix 时间戳)
*   [10]或[ctime]-上次更改信息节点(作为 Unix 时间戳)
*   [11]或[块大小]-文件系统 IO 的块大小(如果支持)
*   [12]或[块]-分配的块数

**注：**

> 此函数类似于[stat()](https://www.geeksforgeeks.org/php-stat-function/)，不同之处在于如果文件参数是符号链接，则符号链接的状态是返回而不是符号链接指向的文件的状态。

**语法：**↔

```
lstat(file)
```

**使用的参数：**和
PHP 中的 lstat()函数接受一个参数。

*   **文件：**指定文件的必选参数。

**返回值：**和
它返回一个包含上述元素的数组。
**例外：**

1.  Lstat()函数的结果因服务器而异。
2.  此函数的结果被缓存，因此使用 clearstatcache()函数清除缓存。
3.  失败时会发出 E_WARNING。

**示例：1**和

```
Input : print_r(lstat("gfg.txt"));

Output :
Array
(
[0] => 0
[1] => 0
[2] => 33206
[3] => 1
[4] => 0
[5] => 0
[6] => 0
[7] => 92
[8] => 1141633430
[9] => 1141298003
[10] => 1138609592
[11] => -1
[12] => -1
[dev] => 0
[ino] => 0
[mode] => 33206
[nlink] => 1
[uid] => 0
[gid] => 0
[rdev] => 0
[size] => 92
[atime] => 1141633430
[mtime] => 1141298003
[ctime] => 1138609592
[blksize] => -1
[blocks] => -1
)
```

**示例：2**和

```
Input : symlink('gfg.php', 'gfg');
        array_diff(stat('gfg'), lstat('gfg'));
Output :
Array
(
    [ino] => 97236376
    [mode] => 33188
    [size] => 34
    [atime] => 1223580003
    [mtime] => 1223581848
    [ctime] => 1223581848
    [blocks] => 8
)

Explanation: Difference of the results of stat() and lstat() function
```

下面的程序演示了 lstat()函数。
**程序 1**

## PHP

```
<?php
// displaying information using lstat() function
print_r(lstat("gfg.txt"));
?>
```

**输出：**

```
Array
(
[0] => 0
[1] => 0
[2] => 33206
[3] => 1
[4] => 0
[5] => 0
[6] => 0
[7] => 92
[8] => 1141633430
[9] => 1141298003
[10] => 1138609592
[11] => -1
[12] => -1
[dev] => 0
[ino] => 0
[mode] => 33206
[nlink] => 1
[uid] => 0
[gid] => 0
[rdev] => 0
[size] => 92
[atime] => 1141633430
[mtime] => 1141298003
[ctime] => 1138609592
[blksize] => -1
[blocks] => -1
)
```

**程序 2**

## PHP

```
<?php

// creating a symbolic link
symlink('gfg.php', 'gfg');

// comparing information returned
//  by stat() and lstat() function
array_diff(stat('gfg'), lstat('gfg'));
?>
```

**输出：**

```
Array
(
    [ino] => 97236376
    [mode] => 33188
    [size] => 34
    [atime] => 1223580003
    [mtime] => 1223581848
    [ctime] => 1223581848
    [blocks] => 8
)
```

**程序 3**

## PHP

```
<?php
// displaying information of
// zip file using lstat() function
$myfile = lstat("./gfg.zip");
echo($myfile);
?>
```

**输出：**

```
Array (
[0] => 2161 
[1] => 18351063 
[2] => 33188 
[3] => 1 
[4] => 1036 
[5] => 1036 
[6] => 0 
[7] => 270081 
[8] => 1382409024 
[9] => 1382409631 
[10] => 1382409631 
[11] => 4096 
[12] => 528
[dev] => 2161 
[ino] => 18351063 
[mode] => 33188 
[nlink] => 1 
[uid] => 1036 
[gid] => 1036 
[rdev] => 0 
[size] => 270081 
[atime] => 1382409024 
[mtime] => 1382409631 
[ctime] => 1382409631 
[blksize] => 4096 
[blocks] => 528 )
```

**相关文章：**[php|STAT()函数](https://www.geeksforgeeks.org/php-stat-function/)
**参考：**http://php.net/manual/en/function.lstat.php
[STAT](http://php.net/manual/en/function.lstat.php)