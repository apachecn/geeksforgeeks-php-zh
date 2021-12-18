# PHP|fSeek()函数

> Original: [https://www.geeksforgeeks.org/php-fseek-function/](https://www.geeksforgeeks.org/php-fseek-function/)

PHP 中的*fSeek()*函数是一个内置函数，用于在打开的文件中查找。 它将文件指针从其当前位置向前或向后移动到由字节数指定的新位置。 文件和偏移量作为参数发送给*fSeek()*函数，如果成功则返回 0，如果失败则返回-1。

**语法：**

```php
int fseek ( $file, $offset, $whence)
```

**参数：**PHP 中的*fSeek()*函数接受三个参数，如下所述。

*   ***$FILE* :** specifies the required parameters for the file.
*   ***$Offset* :** specifies the mandatory parameter for the new position of the pointer. It is measured in bytes from the beginning of the file.
*   ***$where* :** it is an optional parameter and can have the following possible values-
    *   Seek_Set: it sets the position equal to the offset.
    *   Seek_Cur: sets the position to the current position plus the offset.
    *   SEEK_END: set the position to EOF plus offset. To move to the position before EOF, the offset must be negative.

**返回值：**成功返回 0，失败返回-1。

**例外：**

*   查找过去的 EOF(文件结尾)会生成错误。
*   如果文件是在追加(a 或+)模式下打开的，则无论文件位置如何，写入该文件的任何数据都将被追加，并且调用*fSeek()*的结果将是未定义的。
*   并不是所有的流都支持查找。 对于那些不支持搜索的人，从当前位置向前搜索是通过读取和丢弃数据来完成的；其他形式的搜索将失败。

下面的程序说明了 PHP 中的*fSeek()*函数：

**程序 1：**在以下程序中，名为 gfg.txt 的文件包含以下内容：

> Geeksforgeek 是极客的门户！

```php
<?php
// Opening a file
$myfile = fopen("gfg.txt", "w");

// reading first line
fgets($myfile);

// moving back to the beginning of the file
echo fseek($myfile, 0);

// closing the file
fclose($myfile);
?>
```

帖子主题：Re：Колибри

**程序 2：**在下面程序中，名为 gfg.txt 的文件包含以下内容：

> Geeksforgeek 是极客的门户！

```php
<?php
// Opening a file
$myfile = fopen("gfg.txt", "w");

// reading first line
fgets($myfile);

// fseek() pointing to the end of the file
fseek(fp, 0, SEEK_END);

// closing the file
fclose($myfile);
?>
```

帖子主题：Re：Колибри

**引用：**[http://php.net/manual/en/function.fseek.php](http://php.net/manual/en/function.fseek.php)