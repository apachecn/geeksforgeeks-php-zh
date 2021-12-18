# PHP|plose()函数

> Original: [https://www.geeksforgeeks.org/php-pclose-function/](https://www.geeksforgeeks.org/php-pclose-function/)

函数的作用是：关闭由 popen()函数打开的管道。 由 popen()函数启动的文件指针必须用 plose()关闭。
popen()函数指定的管道作为参数发送给 plose()函数，它返回正在运行的进程的终止状态，如果出现错误，则返回-1。

**语法：**

```php
pclose(pipe)
```

**使用的参数：**
PHP 中的 plose()函数只接受一个参数。

*   **管道：**这是一个强制参数，指定 popen()函数打开的管道。

**返回值：**
它返回正在运行的进程的终止状态，如果出现错误，则返回-1。

**错误和异常：**

1.  要获得实际的退出状态代码，应该使用**pcntl_wexitstatus()**函数。
2.  Plose()在每个平台上都返回 0，以防 popen()无法执行指定的命令。

**示例：**

```php
Input : $my_file = popen("/bin/ls", "r");
        pclose($my_file);
Output : 1

Input : $my_file = popen('/executable/gfg.exe', 'r');
        echo "'my_file'; " . get_class($my_file) . "\n";
        $file_read = fread($my_file, 4192);
        echo $file_read;
        pclose($my_file);

Output : 1

```

下面的程序演示了 plose()函数。

**程序 1**

```php
<?php
// opening a pipe 
$my_file = popen("/bin/ls", "r");

// closing the my_file
pclose($my_file);
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
$my_file = popen('/executable/gfg.exe', 'r');

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

**引用：**
[http://php.net/manual/en/function.pclose.php](http://php.net/manual/en/function.pclose.php)