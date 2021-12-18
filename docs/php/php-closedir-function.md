# PHP | closedir()函数

> 原文:[https://www.geeksforgeeks.org/php-closedir-function/](https://www.geeksforgeeks.org/php-closedir-function/)

PHP 中的 closedir()函数是一个内置函数，用于关闭目录句柄。要关闭的目录句柄作为参数发送给 closedir()函数，closedir()关闭目录句柄。目录句柄必须事先由 opendir()函数打开。

**语法:**

```php
closedir($dir_handle)

```

**使用的参数:**PHP 中的 closedir()函数只接受一个参数，如下所述。

*   **$ dir _ handle** : it is an optional parameter that specifies the directory handle resource that was previously opened with opendir (). If this parameter is not specified, the last link opened by opendir () will be assumed and closedir () will be closed.

**返回值:**不返回值。

**错误和异常**:

1.  作为参数发送给 closedir()函数的目录句柄必须事先由 opendir()函数打开。
2.  如果没有指定 dir_handle 参数，opendir()打开的最后一个链接将被 closedir()函数假定并关闭。

下面的程序说明了 closedir()函数:

**节目 1:**

```php
<?php

// Opening a directory
$dir_handle = opendir("/user/gfg/docs/");

if(is_resource($dir_handle))
{ 
    echo("Directory Opened Successfully.");

    // closing the directory
    closedir($dir_handle);
}
else
{
    echo("Directory Cannot Be Opened.");
} 

?>
```

**输出:**

```php
Directory Opened Successfully.

```

**节目 2** :

```php
<?php

// opening a directory and reading its contents
$dir_handle = opendir("user/gfg/sample.docx");

if(is_resource($dir_handle)) 
{ 
    while(($file_name = readdir($dir_handle)) == true) 
    { 
        echo("File Name: " . $file_Name);
        echo "<br>" ; 
    } 

    // closing the directory
    closedir($dir_handle);
}
else
{
    echo("Directory Cannot Be Opened.");
}

?>
```

**输出:**

```php
File Name: sample.docx

```

**参考:**T2】http://php.net/manual/en/function.closedir.php