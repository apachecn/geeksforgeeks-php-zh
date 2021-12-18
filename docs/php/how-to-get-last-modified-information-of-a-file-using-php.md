# 如何用 PHP 获取文件最后修改的信息？

> 原文:[https://www . geesforgeks . org/如何使用 php 获取文件的最后修改信息/](https://www.geeksforgeeks.org/how-to-get-last-modified-information-of-a-file-using-php/)

**[filemtime()](https://www.geeksforgeeks.org/php-filemtime-function/)** 函数是一个内置函数，返回文件内容的最后一次修改。它以文件上次修改时间的 UNIX 时间戳的形式返回，并在失败时返回 false。文件名由 filemtime()作为参数传递。此功能的输出被缓存。要清除缓存，请使用 clearstatcache()命令。

**语法**

```php
filemtime( filepath );
```

**参数:**该功能接受如上所述的单个参数，描述如下:

**文件路径:**指定要检查的文件的路径。它是必需的参数。

**返回值:**返回文件最后一次修改的时间，失败时返回 false。时间将作为适用于 date()函数的 Unix 时间戳返回。

**例 1:**

## PHP

```php
<?php

// Checking the contents of a
// file last time changed
echo filemtime("gfg.txt");

?>
```

```php
Output: 1540211782
```

**例二:**

## PHP

```php
<?php

// A file's last modification time as a
// date that is in human-readable form
echo "Last time of file change: " . 
  date("F d Y H:i:s.", filemtime("gfg.txt"));

?>
```

```php
Output: Last time of file change: September 11 2020 09:55:51
```