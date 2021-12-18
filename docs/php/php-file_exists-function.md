# PHP|FILE_EXISTS()函数

> Original: [https://www.geeksforgeeks.org/php-file_exists-function/](https://www.geeksforgeeks.org/php-file_exists-function/)

PHP 中的 FILE_EXISTS()函数是一个内置函数，用于检查文件或目录是否存在。

您想要检查的文件或目录的路径将作为参数传递给 FILE_EXISTS()函数，该函数在成功时返回 True，在失败时返回 False。

**语法：**

```
file_exists($path)
```

**参数：**PHP 中的 FILE_EXISTS()函数只接受一个参数*$path*。 它指定要检查的文件或目录的路径。

**返回值：**成功返回 True，失败返回 False。

**错误和异常：**

1.  如果指定的路径指向不存在的文件，则函数的作用是：返回 FALSE。
2.  对于大于 2 GB 的文件，某些文件系统函数可能会产生意想不到的结果，因为 PHP 的整数类型是有符号的，并且许多平台使用 32 位整数。

**示例：**

```
Input : echo file_exists('/user01/work/gfg.txt');
Output : 1

Input : $file_pointer = '/user01/work/gfg.txt';
        if (file_exists($file_pointer)) {
            echo "The file $file_pointer exists";
        }else {
            echo "The file $file_pointer does 
                                   not exists";
        }
Output : 1

```

下面的程序举例说明了 FILE_EXISTS()函数。

**程序 1**：

```
<?php

// checking whether file exists or not
echo file_exists('/user01/work/gfg.txt');

?>
```

产出：

```
1
```

**程序 2**：

```
<?php

// checking whether file exists or not
$file_pointer = '/user01/work/gfg.txt';

if (file_exists($file_pointer)) 
{
    echo "The file $file_pointer exists";
}
else 
{
    echo "The file $file_pointer does
                             not exists";
}

?>
```

产出：

```
1
```

**引用：**
[http://php.net/manual/en/function.file-exists.php](http://php.net/manual/en/function.file-exists.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。