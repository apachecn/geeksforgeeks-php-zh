# PHP|unlink()函数

> Original: [https://www.geeksforgeeks.org/php-unlink-function/](https://www.geeksforgeeks.org/php-unlink-function/)

Unlink()函数是 PHP 中的一个内置函数，用于删除文件。 它类似于 UNIX unlink()函数。 $fileName 作为需要删除的参数发送，函数成功时返回 True，失败时返回 False。

**语法：**

```
unlink( $filename, $context )

```

**参数：**此函数接受上述两个参数，如下所述：

*   **$filename：**这是一个强制参数，用于指定必须删除的文件的文件名。
*   **$CONTEXT：**它是一个可选参数，用于指定可用于修改流性质的文件句柄的上下文。

**返回值：**成功返回 True，失败返回 False。

**错误和异常：**

*   函数的作用是：在失败时生成 E_WARNING 级别的错误。
*   Web 服务器用户必须对目录具有写入权限才能使用 unlink()函数。
*   Unlink()函数返回布尔值 False，但很多时候它返回的是非布尔值，计算结果为 False。

以下程序说明了 PHP 中的 unlink()函数：

假设有一个名为**“gfg.txt”**
**Program 1：**的文件

## PHP

```
<?php
// PHP program to delete a file named gfg.txt
// using unlink() function

$file_pointer = "gfg.txt";

// Use unlink() function to delete a file
if (!unlink($file_pointer)) {
    echo ("$file_pointer cannot be deleted due to an error");
}
else {
    echo ("$file_pointer has been deleted");
}

?>
```

**输出：**

```
gfg.txt has been deleted

```

**程序 2：**

## PHP

```
<?php
// PHP program to delete a file named gfg.txt
// using unlink() function

$file_pointer = fopen('gfg.txt', 'w+');

// writing on a file named gfg.txt
fwrite($file_pointer, 'A computer science portal for geeks!');
fclose($file_pointer);  

// Use unlink() function to delete a file
if (!unlink($file_pointer)) {
    echo ("$file_pointer cannot be deleted due to an error");
}
else {
    echo ("$file_pointer has been deleted");
}

?>
```

**输出：**

```
Warning: unlink() expects parameter 1 to be a valid path, resource
given in C:\xampp\htdocs\server.php on line 12
Resource id #3 cannot be deleted due to an error

```

**引用：**[http://php.net/manual/en/function.unlink.php](http://php.net/manual/en/function.unlink.php)