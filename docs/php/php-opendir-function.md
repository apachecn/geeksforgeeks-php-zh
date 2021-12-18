# PHP|opendir()函数

> Original: [https://www.geeksforgeeks.org/php-opendir-function/](https://www.geeksforgeeks.org/php-opendir-function/)

PHP 中的 opendir()函数是一个内置函数，用于打开目录句柄。 要打开的目录的路径作为参数发送给 opendir()函数，如果成功则返回目录句柄资源，如果失败则返回 False。

函数的作用是：打开一个目录句柄，以便在后续操作中与其他目录函数(如 clodir()、readdir()和 rewindir())一起使用。

**语法：**

```
opendir($path, $context)
```

**使用的参数：**PHP 中的 opendir()函数接受两个参数。

*   **$path**：必选参数，指定要打开的目录的路径。
*   **$CONTEXT**：它是一个可选参数，指定流的行为。

**返回值：**成功时返回目录句柄资源，失败时返回 False。

**错误和异常**：

1.  如果路径不是有效目录，或者由于权限限制或文件系统错误而无法打开该目录，则会生成 E_WARNING 级别的 PHP 错误，并且 opendir()返回 FALSE。
2.  可以通过在函数名前面加上‘@’来取消 opendir()的错误输出。

下面的程序说明了 opendir()函数：
**程序 1：**

```
<?php

// Opening a directory
$dir_handle = opendir("/user/gfg/docs/");

if(is_resource($dir_handle))
{ 
    echo("Directory Opened Successfully.");
} 

// closing the directory
closedir($dir_handle);

else
{
    echo("Directory Cannot Be Opened.");
} 

?>
```

发帖主题：Re：Колибри0.7.0

```
Directory Opened Successfully.

```

**程序 2：**

```
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

发帖主题：Re：Колибри0.7.0

```
File Name: sample.docx

```

**引用：**[http://php.net/manual/en/function.opendir.php](http://php.net/manual/en/function.opendir.php)