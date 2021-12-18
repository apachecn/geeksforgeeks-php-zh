# PHP|popen()函数

> Original: [https://www.geeksforgeeks.org/php-popen-function/](https://www.geeksforgeeks.org/php-popen-function/)

函数的作用是：打开通向用户使用命令参数指定的程序的管道。 它返回的文件指针与[fopen()](https://www.geeksforgeeks.org/php-basics-file-handling/)返回的文件指针相同，但本质上是单向的，即它只能用于读取或写入。 Popen()指针可以与[fgets()](https://www.geeksforgeeks.org/php-fgets-function/)、[fgetss()](https://www.geeksforgeeks.org/php-fgetss-function/)和[fwrite()](https://www.geeksforgeeks.org/php-basics-file-handling/)一起使用。 由 popen()函数启动的文件指针必须用[plose()](https://www.geeksforgeeks.org/php-pclose-function/)关闭。
命令和模式作为参数发送给 popen()函数，成功时返回单向文件指针，失败时返回 False。

**语法：**

```php
popen(command, mode)
```

**使用的参数：**
PHP 中的 popen()函数接受两个参数。

1.  **命令：**必选参数，指定要执行的命令。
2.  **模式：**必选参数，指定连接模式，如只读(R)或只写(W)。

**返回值：**
它返回的文件指针与 fopen()返回的文件指针相同，但本质上是单向的。

**错误和异常：**

1.  由 popen()函数启动的文件指针必须用 plose()关闭。
2.  如果找不到要执行的命令，则 popen()函数将返回有效资源。

**示例：**

```php
Input : $my_file= popen("/bin/ls", "r");
Output : 1

Input : $my_file= popen('/executable/gfg.exe', 'r');
        echo "'my_file'; " . get_class($my_handle) . "\n";
        $file_read = fread($my_file, 4192);
        echo $file_read;
        pclose($my_file);
Output : 1

```

下面的程序演示了 popen()函数。

**程序 1**

```php
<?php

// opening a pipe 
$my_file= popen("/bin/ls", "r");
?>
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**程序 2**

```php
<?php 
// opening a pipe
$my_file= popen('/executable/gfg.exe', 'r');

// returning name of class of an object using get_class()
  echo "'$my_file'; " . get_class($my_file) . "\n";

// reading file using fread()
$filereader = fread($my_file, 4192);
   echo $filereader;

// closing the pipe
pclose($my_file);
?>
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**相关文章：**[PHP|plose()函数](https://www.geeksforgeeks.org/php-pclose-function/)

**引用：**
[http://php.net/manual/en/function.popen.php](http://php.net/manual/en/function.popen.php)