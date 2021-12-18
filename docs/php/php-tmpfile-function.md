# PHP|tmpfile()函数

> Original: [https://www.geeksforgeeks.org/php-tmpfile-function/](https://www.geeksforgeeks.org/php-tmpfile-function/)

PHP 中的 tmpfile()函数是一个内置函数，用于在**读写(w+)**模式下创建具有唯一名称的临时文件。
使用 flose()关闭或没有剩余的文件句柄引用时，使用 tmpfile()函数创建的文件会被自动删除。-
脚本的末尾还会删除使用 tmpfile()函数创建的临时文件。
tmpfile()函数会自动删除使用 tmpfile()函数创建的临时文件。
tmpfile()函数会自动删除使用 tmpfile()函数创建的临时文件。
tmpfile()函数会自动删除使用 tmpfile()函数创建的临时文件。 对于新文件，则返回 FALSE，如果失败，则返回 FALSE。

**语法：**

```php
tmpfile()
```

**返回值：**或
成功时返回新文件的文件句柄，失败时返回 False。

**错误和异常：**

1.  使用 flose()关闭临时文件或脚本结束时，会自动删除该临时文件。
2.  Tmpfile()函数返回布尔值 False，但很多时候它返回的是非布尔值，计算结果为 False。

**示例：**

```php
Input :  $temp_pointer = tmpfile();
         fwrite($temp_pointer, 'temporary data');
         fclose(temp_pointer);
Output : 1

Input : $temp_pointer = tmpfile();
        fwrite($temp_pointer, "GeeksforGeeks");
        echo fread($temp_pointer, 2048);
        fclose($temp);

Output : Geeksforgeeks
```

下面的程序演示了 tmpfile()函数。

**程序 1**

## PHP

```php
<?php
// PHP program to illustrate tmpfile( ) Function

$temp_pointer = tmpfile();

// Write on temporary file
fwrite($temp_pointer, 'temporary data');

// This removes the file
fclose(temp_pointer);

?>
```

**输出：**

```php
1
```

**程序 2**

## PHP

```php
<?php
// PHP program to illustrate tmpfile( ) Function

$temp_pointer = tmpfile();

// Write on temporary file
fwrite($temp_pointer, "GeeksforGeeks");

// Read 2k from file
echo fread($temp_pointer, 2048);

// This removes the file
fclose($temp_pointer);

?>
```

**输出：**

```php
GeeksforGeeks
```

**引用：**和
[http://php.net/manual/en/function.tmpfile.php](http://php.net/manual/en/function.tmpfile.php)