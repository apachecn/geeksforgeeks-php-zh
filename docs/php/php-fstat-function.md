# PHP|fstat()函数

> Original: [https://www.geeksforgeeks.org/php-fstat-function/](https://www.geeksforgeeks.org/php-fstat-function/)

PHP 中的*fstat()*函数是一个内置函数，用于返回有关打开的文件的信息。 文件名作为参数发送给*fstat()*函数，它返回一个包含以下元素的数组：。 ][T90。 。

| 数字的 / 用数字表示的 / 数值的 / 同 numeric | 联想的 / 结合的 / 联合的 / 组合的 | 描述 / 描写 / 形容 / 类别 |
| --- | --- | --- |
| 0 | 发展 | 设备号 |
| 1[。 T25] | Inode number * |
| 2 个 | Pattern | Inode protection mode |
| 3. | NLink | Number of links |
| 4. | UID | Number of links |
| 4. | UID |
| 5. | 脑包虫病 / 多头蚴病 / 蹒跚病 / 眩倒病 | Owner |
| 6. | Rdev | Device type, if the Inode device |
| 7. | Size | Byte size |
| 8 个 | 阿提姆 | Last access time (Unix timestamp) |
| 9. | 时光网 |
| 10 个 | Ctime | Time when the Inode was last changed (Unix timestamp) |
| 11. | Block size | File system IO block size * * |
| 12 个 | Block |

函数的作用是：收集文件指针句柄打开的文件的统计信息。 Fstat()函数类似于 stat()函数，不同之处在于它操作的是打开的文件指针，而不是文件名。

**语法：**

```
array fstat ( $file )
```

**参数：**PHP 中的*fstat()*函数只接受一个参数。

*   **$FILE:** specifies the required parameters for the file.

**返回值：**如果成功，则返回包含上述元素的数组。

**例外：**

*   The result of this function varies from server to server. The array can contain a numeric index and / or a name index.
*   The *fstat ()* function is similar to the *stat ()* function, except that it must open a file.
*   The atime element is not updated with simple file read access.

以下程序说明了*fstat()*函数：

**程序 1：**

```
<?php
// Opening a file
$myfile = fopen("gfg.txt", "r");

// printing the stats of the opened file
print_r(fstat($myfile));

// closing the file
fclose($myfile);
?>
```

帖子主题：Re：Колибри

**程序 2：**

```
<?php
// Opening a file
$myfile = fopen("gfg.txt", "r");

// printing the associative part of the output array
$mystat = fstat($myfile);
print_r(array_slice($mystat, 13));

// closing the file
fclose($myfile);
?>
```

帖子主题：Re：Колибри

**引用：**[http://php.net/manual/en/function.fstat.php](http://php.net/manual/en/function.fstat.php)