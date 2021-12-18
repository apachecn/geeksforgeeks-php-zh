# PHP|SplFileInfo getOwner()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getowner-function/](https://www.geeksforgeeks.org/php-splfileinfo-getowner-function/)

SplFileInfo：：getOwner()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件的所有者。 所有者 ID 以数字格式返回。

**语法：**

```
*int* SplFileInfo::getOwner( void )
```

**参数：**该函数不接受任何参数。

**返回值：**此函数以数字形式返回所有者 ID。

下面的程序演示了 PHP 中的 SplFileInfo：：getOwner()函数：

**程序 1：**

```
<?php

// PHP Program to illustrate 
// Splfileinfo::getOwner() function

// Create new SPlFileInfo Object
$file = new SplFileInfo('gfg.txt');

// Print result
print_r(posix_getpwuid($file->getOwner()));

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// PHP Program to illustrate 
// Splfileinfo::getOwner() function

// Create new SPlFileInfo Object
$file = new SplFileInfo(__FILE__);

// Print result
print_r(posix_getpwuid($file->getOwner()));

?>
```

**输出：**

```
Array
(
    [name] => www-data
    [passwd] => x
    [uid] => 33
    [gid] => 33
    [gecos] => www-data
    [dir] => /var/www
     => /usr/sbin/nologin
)

```

**引用：**[http://php.net/manual/en/splfileinfo.getowner.php](http://php.net/manual/en/splfileinfo.getowner.php)