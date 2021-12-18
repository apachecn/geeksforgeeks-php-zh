# PHP|fgetc()函数

> Original: [https://www.geeksforgeeks.org/php-fgetc-function/](https://www.geeksforgeeks.org/php-fgetc-function/)

PHP 中的 fgetc()函数是一个内置函数，用于从打开的文件返回单个字符。 它用于从给定的文件指针获取字符。

要检查的文件用作 fgetc()函数的参数，它返回一个字符串，其中包含文件中用作参数的单个字符。

**语法：**

```
fgetc($file)
```

**参数：**PHP 中的 fgetc()函数只接受一个参数*$file*。 它指定需要从中提取字符的文件。

**返回值：**它返回一个字符串，该字符串包含文件中用作参数的单个字符。

**错误和异常**：

1.  该函数没有针对大文件进行优化，因为它一次读取一个字符，并且可能需要很长时间才能完全读取一个长文件。
2.  如果多次使用 fgetc()函数，则必须清除缓冲区。
3.  Fgetc()函数返回布尔值 False，但很多时候它返回的是非布尔值，计算结果为 False。

下面的程序演示了 fgetc()函数。

**程序 1**：在下面的程序中，名为*gfg.txt*的文件包含以下文本。

> 这是第一行。
> 这是第二行。
> 这是第三行。

```
<?php

// file is opened using fopen() function
$my_file = fopen("gfg.txt", "rw");

// Prints a single character from the
// opened file pointer
echo fgetc($my_file);

// file is closed using fclose() function
fclose($my_file);

?>
```

产出：

```
T
```

**程序 2**：在下面的程序中，名为*gfg.txt*的文件包含以下文本。

> 这是第一行。
> 这是第二行。
> 这是第三行。

```
<?php

// file is opened using fopen() function
$my_file = fopen("gfg.txt", "rw");

// prints single character at a time
// until end of file is reached
while (! feof ($my_file))
  {
  echo fgetc($my_file);
  }

// file is closed using fclose() function
fclose($my_file);
?>
```

产出：

```
This is the first line.
This is the second line.
This is the third line.

```

**引用：**
[http://php.net/manual/en/function.fgetc.php](http://php.net/manual/en/function.fgetc.php)