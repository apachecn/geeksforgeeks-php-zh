# PHP|is_readable()函数

> Original: [https://www.geeksforgeeks.org/php-is_readable-function/](https://www.geeksforgeeks.org/php-is_readable-function/)

PHP 中的 is_readable()函数用于检查指定的文件是否存在以及是否可读。 文件名作为参数发送给 is_readable()函数，如果文件存在且可读，则返回 True。
is_readable()函数对于流返回 False，例如 php：//stdin。
is_readable()函数还可以用于 PHP 5.0.0 中的一些 URL 包装，如 file：//、http：//、ftp：//、php：//。

**语法：**

```php
is_readable($file)
```

**使用的参数：**
PHP 中的 is_readable()函数只接受一个参数。

*   **文件：**指定文件的必选参数。

**返回值：**
如果指定的文件或目录存在且可读，则返回 True，否则返回 False。

**例外：**

1.  失败时会发出 E_WARNING。
2.  此函数的结果被缓存，因此使用 clearstatcache()函数清除缓存。

下面的程序演示了 is_readable()函数。

**程序 1**

```php
<?php 
$myfile = "gfg.txt";

// checking whether file is readable or not
if (is_readable($myfile)) 
{
    echo '$myfile is readable';
} 
else 
{
    echo '$myfile is not readable';
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
gfg.txt is readable

```

**程序 2**

```php
<?php 
$myfile = "gfg.txt";

// checking whether file is readable or not
if (is_readable($myfile)) 
{
    echo '$myfile is readable';

    // displaying contents of the uploaded file
    echo "Contents of the file are :\n";
    readfile($myfile);
} 
else 
{
    echo '$myfile is not readable';
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
gfg.txt is readable
Contents of the file are :
Portal for geeks!

```

**程序 3**

```php
<?php 

$permissions = fileperms("gfg.txt");
$permvalue = sprintf("%o", $permissions);

// Clearing the File Status Cache 
clearstatcache();

if(is_readable("gfg.txt")) 
{ 
   echo("File is Readable 
    and File Permissions are : $permvalue)");
} 
else
{
  echo("File is Not Readable 
     and File Permissions are : $permvalue)");
} 

// Clearing the File Status Cache
clearstatcache();
?>
```

发帖主题：Re：Колибри0.7.0

```php
File is Readable and File Permissions are : 0644

```

**相关文章：**[PHP|is_Writable()函数](https://www.geeksforgeeks.org/php-is_writable-function/)

**引用：**
[http://php.net/manual/en/function.is-readable.php](http://php.net/manual/en/function.is-readable.php)