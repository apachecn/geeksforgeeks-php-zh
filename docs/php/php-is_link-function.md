# PHP|is_link()函数

> Original: [https://www.geeksforgeeks.org/php-is_link-function/](https://www.geeksforgeeks.org/php-is_link-function/)

PHP 中的 is_link()函数用于检查指定的文件是否为[符号链接](https://www.geeksforgeeks.org/soft-hard-links-unixlinux/)。 文件的路径作为参数发送给 is_link()函数，如果文件名存在并且是符号链接，则返回 TRUE，否则返回 FALSE。

**语法：**

```
is_link(file)
```

**使用的参数：**
PHP 中的 is_link()函数只接受一个参数。

*   **文件：**指定文件路径的必选参数。

**返回值：**
如果文件名存在并且是符号链接，则返回 TRUE，否则返回 FALSE。

**例外：**

1.  失败时会发出 E_WARNING。
2.  此函数的结果被缓存，因此使用 clearstatcache()函数清除缓存。

**示例：**

```
Input : $mylink = "gfg";
        if(is_link($mylink))
        {
         echo ("$mylink is a symbolic link!");
        }
        else
        {
         echo ("$mylink is not a symbolic link!");
        }

Output : gfg is a symbolic link!

Input : $mylink = "gfg";
        if (is_link($mylink)) 
        {
         echo ("$mylink is a symbolic link!");
         echo "Reading the link :\n";
         echo(readlink($mylink));
        }
        else 
        {
         symlink("gfg", $mylink);
        }
Output : gfg is a symbolic link!
         Reading the link :
         A portal for geeks!

```

下面的程序演示了 is_link()函数。

**程序 1**

```
<?php

$myfile = "gfg";

// checking whether the file is a symbolic link or not
if (is_link($mylink)) {
    echo ("$mylink is a symbolic link!");
} else {
    echo ("$mylink is not a symbolic link!");
}

?>
```

发帖主题：Re：Колибри0.7.0

```
gfg is a symbolic link!

```

**程序 2**

```
<?php

$myfile = "gfg";

// checking whether the file
// is a symbolic link or not
if (is_link($mylink)) {
    echo ("$mylink is a symbolic link!");

    // Reading the link
    echo "Reading the link :\n";
    echo (readlink($mylink));
}

// creating a symbolic link of the
// file if it doesn't exist
else {
    symlink("gfg", $mylink);
}

?>
```

发帖主题：Re：Колибри0.7.0

```
gfg is a symbolic link!
Reading the link :
A portal for geeks!

```

**引用：**
[http://php.net/manual/en/function.is-link.php](http://php.net/manual/en/function.is-link.php)