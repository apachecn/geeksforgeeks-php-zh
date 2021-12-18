# PHP|readfile()函数

> Original: [https://www.geeksforgeeks.org/php-readfile-function/](https://www.geeksforgeeks.org/php-readfile-function/)

PHP 中的 readfile()函数是一个内置函数，用于读取文件并将其写入输出缓冲区。 文件名作为参数发送给 readfile()函数，它在成功时返回读取的字节数，在失败时返回 False 和错误。
通过在函数名前面添加**‘@’**，可以隐藏错误输出。

**语法：**

```
readfile(filename, include_path, context)
```

**使用的参数：**
PHP 中的 readfile()函数接受三个参数。

1.  **文件名：**指定文件名的必选参数。
2.  **include_path：**这是一个可选参数，如果要在 php 的 include_path 中搜索文件，可以将该参数设置为 1
3.  **上下文：**这是一个可选参数，指定流的行为。

**返回值：**
它返回成功时读取的字节数，失败时返回 False 和错误。

```
Note: URL can be used as a filename with this function if the fopen wrappers have been enabled.
```

**错误和异常**

*   在调用 Readfile()函数之前关闭输出缓冲可能有助于将更大的文件读入内存。

**示例：**

```
Input : echo readfile("gfg.txt");
Output : A computer portal for geeks!

Input : $myfile = @readfile("gfg.txt");
        if (!$myfile) 
        {
             print "File could not be opened";
        }
Output : A computer portal for geeks!

```

下面的程序演示了 readfile()函数。

假设有一个名为“gfg.txt”的文件

**程序 1**

```
<?php 

// writing file contents on the output
//  buffer using readfile() function
echo readfile("gfg.txt");

?>
```

发帖主题：Re：Колибри0.7.0

```
A computer portal for geeks!
```

**程序 2**

```
<?php 

// writing file contents on the output
//  buffer using readfile() function
$myfile = @readfile("gfg.txt");
if (!$myfile) 
{
   print "File could not be opened";
}
?>
```

发帖主题：Re：Колибри0.7.0

```
A computer portal for geeks!
```

**引用：**
[http://php.net/manual/en/function.readfile.php](http://php.net/manual/en/function.readfile.php)