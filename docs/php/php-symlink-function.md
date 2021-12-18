# PHP|symlink()函数

> Original: [https://www.geeksforgeeks.org/php-symlink-function/](https://www.geeksforgeeks.org/php-symlink-function/)

PHP 中的 symlink()函数是一个内置函数，用于为已经存在的目标创建符号链接。 它有助于为目标创建特定的名称链接。-
目标名称和链接名称作为参数发送给 symlink()函数，成功时返回 True，失败时返回 False。*
symlink()函数不提供 HTML 链接，而是文件系统中的链接。
**语法：**

```
symlink(target, link)
```

**使用的参数：**和
PHP 中的 symlink()函数接受两个参数。

1.  目标：这是一个必选参数，用于指定必须创建其链接的目标。
2.  链接：必选参数，指定链接名称。

**返回值：**和
成功时返回 True，失败时返回 False。
**错误和异常：**

1.  如果运行 PHP 的系统早于 Windows Vista/Windows Server 2008，symlink()函数将不起作用。
2.  函数的作用是：在 Windows 上只接受绝对路径。 符号链接不支持 Windows 上的相对路径。
3.  Symlink()函数返回布尔值 FALSE，但很多时候它返回的是非布尔值，计算结果为 FALSE。

例如：

```
Input : $target_pointer = 'gfg.txt';
        $link_name = 'geeksforgeeks';
        symlink($target_pointer, $link_name);
Output : 1

Input : $target_pointer = "/home/user1/gfg.txt";
        $link_name = 'mylink';
        $test = symlink($target_pointer, $link_name);
        if ($result) 
        {
          echo ("Symlink has been created!");
        }
        else 
        {
          echo ("Symlink cannot be created!");
        }
Output : Symlink has been created!
```

下面的程序演示了 symlink()函数。
假设有一个名为‘gfg.txt’
**Program 1**的文件

## PHP

```
<?php
// specifying target
$target_pointer = 'gfg.txt';

// specifying link  name
$link_name = 'geeksforgeeks';

// creating alink using symlink() function
symlink($target_pointer, $link_name);
?>
```

**输出：**

```
1
```

**程序 2**

## PHP

```
<?php
// specifying target
$target_pointer = "/home/user1/gfg.txt";

// specifying link  name
$link_name = 'mylink';

// creating alink using symlink() function
$test = symlink($target_pointer, $link_name);
if ($result)
{
   echo ("Symlink has been created!");
}
else
{
   echo ("Symlink cannot be created!");
}

?>
```

**输出：**

```
Symlink has been created!
```

**引用：**和
[http://php.net/manual/en/function.symlink.php](http://php.net/manual/en/function.symlink.php)