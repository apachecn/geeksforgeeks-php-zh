# PHP|dir()函数

> Original: [https://www.geeksforgeeks.org/php-dir-function/](https://www.geeksforgeeks.org/php-dir-function/)

PHP 中的 dir()函数是一个内置函数，用于返回 Directory 类的实例。 函数的作用是：读取一个目录，它包括以下内容：

1.  Open the given directory.
2.  Two properties of dir (), Handle and Path, are available.
3.  There are three methods for both the handle and path properties: Read (), Rewind (), and Close ().

目录的路径作为参数发送给 opendir()函数，如果成功则返回 Directory 类的实例，如果失败则返回 False。

**语法：**

```
dir($directory, $context)
```

**使用的参数：**PHP 中的 dir()函数接受两个参数，如下所述。

*   **$DIRECTORY** : this is a mandatory parameter for the specified directory path.
*   **$CONTEXT** : this is an optional parameter that specifies the behavior of the flow.

**返回值：**成功时返回 Directory 类的实例，失败时返回 False。

**错误和异常**：

1.  If you pass dir () with the wrong argument, a null value is returned.
2.  The order in which the Read method returns directory entries depends on the system.

以下程序说明了 dir()函数：

**程序 1：**

```
<?php

$dir_handle = dir("user/gfg");

while(($file_name = $dirhandle->read()) !== false) 
{ 
    echo("File Name : " . $file_name);
    echo "<br>" ; 
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

$dir_handle = dir("user/gfg");

echo("Directory Path: " . $dir_handle->path . "<br>");

echo("Directory Handler ID: " . $dir_handle->handle . "<br>");

while(($file_name = $dir_handle->read()) !== false) 
{ 
   echo("File Name: " . $file_name);
   echo "<br>" ; 
} 

$dir_handle->close();

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.dir.php](http://php.net/manual/en/function.dir.php)