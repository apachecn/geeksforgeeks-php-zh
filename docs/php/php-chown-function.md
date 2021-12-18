# PHP | chown()函数

> 原文:[https://www.geeksforgeeks.org/php-chown-function/](https://www.geeksforgeeks.org/php-chown-function/)

PHP 中的 chown()函数是一个内置函数，用于更改指定文件的所有者。成功时返回真，失败时返回假。只有超级用户有权更改文件的所有者。

**语法:**

```php
bool chown ( $filename, $user )
```

**参数:**PHP 中的 chown()函数接受两个参数，即文件名和用户。

1.  **$filename** :指定要更改所有者的文件。
2.  **$user** :指定新的所有者。它可以是用户名或用户 id。

**返回值:**chown()函数成功时返回 true，失败时返回 false。

**错误和异常**:

1.  PHP 中的 chown()函数不适用于远程文件。它只对服务器文件系统可访问的文件起作用。
2.  当启用安全模式时，PHP 检查正在操作的文件或目录是否与正在执行的脚本拥有相同的所有者。

示例:

```php
Input : chown("gfg.txt", "shubrodeep")
Output : true

Input :  $path = "/user01/Desktop/geeksforgeeks/gfg.php";
         $user_name = "root";
         chown($path, $user_name); 
Output : true

```

下面的程序说明了 chown()函数。

**程序 1** :

```php
<?php

// Sets shubrodeep as owner
chown("gfg.txt", "shubrodeep");

?>
```

输出:

```php
true
```

**程序 2** :

```php
<?php

// Sets root as owner of the file "gfg.php"
$path = "/user01/Desktop/geeksforgeeks/gfg.php";
$user_name = "root";
chown($path, $user_name); 

?>
```

输出:

```php
true
```

**参考:**T2[http://php.net/manual/en/function.chown.php](http://php.net/manual/en/function.chown.php)