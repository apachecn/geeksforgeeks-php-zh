# PHP|stat()函数

> Original: [https://www.geeksforgeeks.org/php-stat-function/](https://www.geeksforgeeks.org/php-stat-function/)

PHP 中的 stat()函数是一个内置函数，用于返回文件信息。 函数的作用是：返回一个文件的统计信息，该文件是一个包含以下元素的数组：

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
*   [11]或[块大小]-文件系统 IO 的块大小
*   [12]或[块]-分配的块数

Stat()函数接受文件名作为参数，并在成功时返回包含上述元素的数组，在失败时返回 False。
如果 filename 是符号链接，则统计数据来自文件本身，而不是符号链接。

**语法：**

```
stat(filename)
```

**使用的参数：**
PHP 中的 stat()函数接受一个参数。

1.  FileName：指定您想要了解其统计数据的文件的文件名。

**返回值：**
成功时返回包含上述元素的数组，失败时返回 false。

**错误和异常**

1.  Stat()函数的结果因服务器而异。
2.  Stat()函数的结果被缓存，因此应使用 clearstatcache()函数清除缓存。
3.  函数的作用是：在失败时生成 E_WARNING。
4.  在 Windows 平台上，所有者的 Groupid、所有者的 UserID 和 inode 编号始终为 0。
5.  对于大于 2 GB 的文件，某些文件系统函数可能会返回意外结果，因为 PHP 的整数类型是有符号的，并且许多平台使用 32 位整数。

**示例：**

```
Input : $test = stat('gfg.txt');
        echo 'Access time: ' .$test['atime'];
        echo '
Modification time: ' .$test['mtime'];
        echo '
Device number: ' .$test['dev'];

Output :Access time: 1141666750
        Modification time: 1135897503
        Device number: 0

Input : $test = stat('gfg.txt');
        echo 'Access time: ' .$test[8];
        echo '
Modification time: ' .$test[9];
        echo '
Device number: ' .$test[0];

Output : Access time: 1141666750
         Modification time: 1135897503
         Device number: 0

Input : $test = stat('gfg.txt');
        $access_time = $stat['atime'] + 18000;
        if (touch($test, time(), $access_time)) 
        {
          echo 'Access time changed to 5 hours in the past!';
        } 
        else 
        {
          echo 'Access time could not be changed.';
        }

Output : Access time changed to 5 hours in the past!

```

下面的程序说明了 stat()函数。

假设有一个名为“gfg.txt”的文件

**程序 1**

```
<?php
$test = stat('gfg.txt');
//using stat() along with name index to display access time
echo 'Access time: ' .$test['atime'];

//using stat() along with name index  to display modification time
echo '<br />Modification time: ' .$test['mtime'];

//using stat() along with name index  to display device number
echo '<br />Device number: ' .$test['dev'];
?>
```

发帖主题：Re：Колибри0.7.0

```
Access time: 1141666750
Modification time: 1135897503
Device number: 0

```

**程序 2**

```
<?php
$test = stat('gfg.txt');

//using stat() along with number index to display access time
echo 'Access time: ' .$test[8];

//using stat() along with number index to display modification time
echo '<br />Modification time: ' .$test[9];

//using stat() along with number index to display device number
echo '<br />Device number: ' .$test[0];
?>
```

发帖主题：Re：Колибри0.7.0

```
Access time: 1141666750
Modification time: 1135897503
Device number: 0

```

**程序 3**

```
<?php
$test = stat('gfg.txt');

//changing access time to 5 hours in the past
$access_time = $stat['atime'] + 18000;

//using touch() function to change the access time
if (touch($test, time(), $access_time)) 
{
   echo 'Access time changed to 5 hours in the past!';
} 
else 
{
   echo 'Access time could not be changed.';
}

?>
```

发帖主题：Re：Колибри0.7.0

```
Access time changed to 5 hours in the past!

```

**引用：**
[http://php.net/manual/en/function.stat.php](http://php.net/manual/en/function.stat.php)