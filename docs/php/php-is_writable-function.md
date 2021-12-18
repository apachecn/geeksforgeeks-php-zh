# PHP|is_Writable()函数

> Original: [https://www.geeksforgeeks.org/php-is_writable-function/](https://www.geeksforgeeks.org/php-is_writable-function/)

PHP 中的 is_Writable()函数用于检查指定的文件是否可写。 文件名作为参数发送给 is_Writable()函数，如果文件名存在且可写，则返回 True。
目录名也可以是 is_Writable()函数的参数，该函数允许检查目录是否可写。

**语法：**

```
is_writable(file)
```

**使用的参数：**
PHP 中的 is_Writable()函数接受一个参数。

*   **文件：**指定文件的必选参数。

**返回值：**
如果文件名存在且可写，则返回 True。

**例外：**

1.  失败时会发出 E_WARNING。
2.  此函数的结果被缓存，因此使用 clearstatcache()函数清除缓存。
3.  对于不存在的文件，is_Writable()函数返回 False。

**示例：**

```
Input : $myfile = "gfg.txt";
        if(is_writable($myfile)) 
        {
           echo ("$myfile file is writable!");
        } 
        else 
        {
           echo ("$myfile file is not writable!");
        }
Output : gfg.txt file is writable!

Input : $permissions = fileperms("gfg.txt");
        $perm_value = sprintf("%o", $permissions);
        $myfile = "gfg.txt";

        if (is_writable($myfile)) 
        {
          echo ("$myfile file is writable and
          it has the following file permissions : $perm_value");
        } 
        else 
        {
          echo ("$myfile file is not writable and
          it has the following file permissions : $perm_value");
        }

Output : gfg.txt file is writable and it has the following file permissions : 0664

```

下面的程序演示了 is_Writable()函数。

**程序 1**

```
<?php 
$myfile = "gfg.txt";

// checking whether the file is writable or not
if(is_writable($myfile)) 
{
 echo ("$myfile file is writable!");
} 
else 
{
 echo ("$myfile file is not writable!");
}
?>
```

发帖主题：Re：Колибри0.7.0

```
 gfg.txt file is writable!

```

**程序 2**

```
<?php 
// checking permissions of the file
$permissions = fileperms("gfg.txt");
$perm_value = sprintf("%o", $permissions);

// Clearing the File Status Cache 
clearstatcache();

$myfile = "gfg.txt";

// checking whether the file is writable or not
if(is_writable($myfile)) 
{
 echo ("$myfile file is writable and 
   it has the following file permissions : $perm_value");
} 
else 
{
 echo ("$myfile file is not writable and
   it has the following file permissions : $perm_value");
}

// Clearing the File Status Cache 
clearstatcache();
?>
```

发帖主题：Re：Колибри0.7.0

```
gfg.txt file is writable and it has the following file permissions : 0664

```

**引用：**
[http://php.net/manual/en/function.is-writable.php](http://php.net/manual/en/function.is-writable.php)