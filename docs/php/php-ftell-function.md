# PHP|ftell()函数

> Original: [https://www.geeksforgeeks.org/php-ftell-function/](https://www.geeksforgeeks.org/php-ftell-function/)

PHP 中的 ftell()函数是一个内置函数，用于返回打开文件中的当前位置。 该文件作为参数发送给 ftell()函数，如果成功则返回当前文件指针位置，如果失败则返回 False。

**语法：**

```
ftell( $file )
```

**使用的参数：**PHP 中的 ftell()函数只接受一个参数*$file*。 它是指定文件的必选参数。

**返回值：**成功时返回当前文件指针位置，失败时返回 False。

**例外**：

1.  某些文件系统函数可能会为大于 2 GB 的文件返回意外结果，因为 PHP 的整数类型是 SIGNED 的，并且许多平台使用 32 位整数。
2.  当通过 fopen(‘file’，‘a+’)打开要读写的文件时，文件指针应该在文件的末尾。

示例：

```
Input : $myfile = fopen("gfg.txt", "r");
        echo ftell($myfile);
Output : 0

Input : $myfile = fopen("gfg.txt", "r");
        echo ftell($myfile);
        fseek($myfile, "36");
        echo ftell($myfile);
Output : 0
         36

```

以下程序说明了 ftell()函数：

**程序 1**：在下面的程序中，名为 gfg.txt 的文件包含以下内容。

> 极客是极客的门户！

```
<?php
// Opening a file in read. mode
$myfile = fopen("gfg.txt", "r");

// displaying the current position of the pointer in the opened file
echo ftell($myfile);

// closing the file
fclose($myfile);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2**：在下面的程序中，名为 gfg.txt 的文件包含以下内容。

> 极客是极客的门户！

```
<?php
// Opening a file in read. mode
$myfile = fopen("gfg.txt", "r");

// displaying the current position of the pointer in the opened file
echo ftell($myfile);

// chnaging current position
fseek($myfile, "36");

//displaying current position
echo "<br />" . ftell($myfile);

// closing the file
fclose($myfile);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.ftell.php](http://php.net/manual/en/function.ftell.php)