# PHP|readdir()函数

> Original: [https://www.geeksforgeeks.org/php-readdir-function/](https://www.geeksforgeeks.org/php-readdir-function/)

PHP 中的 readdir()函数是一个内置函数，用于返回目录中下一个条目的名称。 该方法按文件名存储在文件名系统中的顺序返回文件名。

目录句柄作为参数发送给 readdir()函数，如果成功则返回条目名称/filename，如果失败则返回 False。

**语法：**

```php
readdir(dir_handle)
```

**使用的参数：**PHP 中的 readdir()函数接受一个参数。

*   **DIR_HANDLE** : this is a mandatory parameter that specifies the handle resource that was previously opened by the opendir () function.

**返回值：**成功时返回条目名/文件名，失败时返回 False。

**错误和异常**：

1.  If the user does not specify a directory handle parameter, the readdir () function assumes the last link opened by opendir ().
2.  In addition to returning a Boolean value of FALSE, the readdir () function may sometimes return a non-Boolean value that evaluates to FALSE.

以下程序说明了 readdir()函数：

**程序 1：**

```php
<?php

// opening a directory
$dir_handle = opendir("user/gfg/");

// reading the contents of the directory
while(($file_name = readdir($dir_handle)) !== false) 
{ 
echo("File Name: " . $file_name);
echo "<br>" ; 
}

// closing the directory
closedir($dir_handle);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// opening a directory
$dir_handle = opendir("user/gfg/");

if(is_resource($dir_handle)) 
{ 

// reading the contents of the directory
while(($file_name = readdir($dir_handle)) !== false) 
{ 
echo("File Name: " . $file_name);
echo "<br>" ; 
} 

// closing the directory
closedir($dir_handle);
} 
else
{
echo("Failed to Open.");
} 
} 
else 
{
echo("Invalid Directory.");
} 
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.readdir.php](http://php.net/manual/en/function.readdir.php)