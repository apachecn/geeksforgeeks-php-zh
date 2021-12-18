# PHP|fflush()函数

> Original: [https://www.geeksforgeeks.org/php-fflush-function/](https://www.geeksforgeeks.org/php-fflush-function/)

PHP 中的 fflush()函数是一个内置函数，用于将所有缓冲的输出写入打开的文件。 函数的作用是：强制将所有缓冲输出写入文件句柄指向的资源。 函数的作用是：成功时返回*true*，失败时返回*false*。

**语法：**

```
fflush($file)
```

**参数：**PHP 中的 fflush()函数只接受一个参数，即$file。 它指定打开的文件流。

**返回值：**成功返回 TRUE，失败返回 FALSE。

**错误和异常**：

1.  如果文件指针无效，则 fflush()函数会导致错误。
2.  指向的文件必须由 fopen()或 fsockopen()打开，并由 flose()关闭。

下面的程序演示了 fflush()函数。

**程序 1**：在下面的程序中，名为*singleline.txt*的文件包含一行信息，即“该文件由一行组成”。

```
<?php

// The file is opened using fopen() function
$check = fopen("singleline.txt", "r");
$seq = fgets($check);

// Writing buffered output to a file
// until the end-of-file is reached
while(! feof($check))
    fflush($check);

// The file is closed using fclose() function
fclose($check);

?>
```

产出：

```
This file consists of a single line.

```

**程序 2**：在下面的程序中，名为*gfg.txt*的文件包含以下文本。

> 这是第一行。
> 这是第二行。
> 这是第三行。

```
<?php

// The file is opened using fopen() function
$check = fopen("gfg.txt", "r");
$seq = fgets($check);

// Writing buffered output to a file
// until the end-of-file is reached
while(! feof($check))
    fflush($check);

// The file is closed using fclose() function
fclose($check);

?>
```

产出：

```
This is the first line.
This is the second line.
This is the third line.

```

**引用：**
[http://php.net/manual/en/function.fflush.php](http://php.net/manual/en/function.fflush.php)