# PHP|feof()函数

> Original: [https://www.geeksforgeeks.org/php-feof-function/](https://www.geeksforgeeks.org/php-feof-function/)

PHP 中的 feof()函数是一个内置函数，用于测试文件指针上的文件结尾。 它检查是否已到达“文件末尾”。 如果事先不知道内容的大小，则使用 feof()函数遍历文件的内容。

如果已到达文件末尾或发生错误，则 feof()函数返回 True。 否则，它返回 FALSE。

**语法：**

```php
feof( $file )
```

**参数：**PHP 中的 feof()函数只接受一个参数，即$file。 此参数指定必须检查文件结尾的文件。

**返回值：**如果已到达文件末尾或发生错误，则返回 TRUE。 否则，它返回 FALSE。

**错误和异常**：

1.  如果传递的文件指针无效，它将进入无限循环，因为文件结尾无法返回 True。
2.  如果服务器没有关闭 fsockopen()打开的连接，feof()函数就会挂起。

以下程序说明了 feof()函数：

**程序 1**：在下面的程序中，名为“singleline.txt”的文件只包含一行文本，即“本文件只包含一行”。

```php
<?php

// a file is opened using fopen() function
$check = fopen("singleline.txt", "r");

$seq = fgets($check);

// Outputs a line of the file until
// the end-of-file is reached
while(! feof($check))
{
  echo $seq ;
  $seq = fgets($check);
}

// file is closed using fclose() function
fclose($check);

?>
```

产出：

```php
This file consists of only a single line.

```

**程序 2**：在下面的程序中，名为“gfg.txt”的文件包含以下文本。

> 这是第一行。
> 这是第二行。
> 这是第三行。

```php
<?php

// a file is opened using fopen() function
$check = fopen("gfg.txt", "r");
$seq = fgets($check);

// Outputs a line of the file until
// the end-of-file is reached
while(! feof($check))
{
  echo $seq ;
  $seq = fgets($check);
}

// file is closed using fclose() function
fclose($check);

?>
```

产出：

```php
This is the first line.
This is the second line.
This is the third line.
```

**引用：**
[http://php.net/manual/en/function.feof.php](http://php.net/manual/en/function.feof.php)