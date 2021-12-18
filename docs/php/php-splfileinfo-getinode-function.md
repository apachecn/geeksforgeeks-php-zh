# PHP|SplFileInfo getInode()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-getinode-function/](https://www.geeksforgeeks.org/php-splfileinfo-getinode-function/)

SplFileInfo：：getInode()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件系统对象的 inode 编号。

**语法：**

```php
*int* SplFileInfo::getInode( void)
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回文件系统对象的 inode 编号。

下面的程序演示了 PHP 中的 SplFileInfo：：getInode()函数：

**程序 1：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo::getInode() function

// Create new SPlFileInfo Object
$file = new SplFileInfo("gfg.txt");

// Print result
print_r($file->getInode());

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo::getInode() function

// Create new SPlFileInfo Object
$file = new SplFileInfo(__FILE__);

// print result
print_r($file->getInode());

?>
```

**输出：**

```php
4365503

```

**引用：**[http://php.net/manual/en/splfileinfo.getinode.php](http://php.net/manual/en/splfileinfo.getinode.php)