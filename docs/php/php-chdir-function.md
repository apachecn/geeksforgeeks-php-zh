# php | chdir()函数

> 原文:[https://www.geeksforgeeks.org/php-chdir-function/](https://www.geeksforgeeks.org/php-chdir-function/)

PHP 中的 chdir()函数用于将 PHP 的当前目录更改为新的目录路径。它只接受一个参数作为**新的目录路径。**

**语法:**

```php
bool chdir(string $new_directory_path)

```

> **使用的参数:**该函数只接受一个参数，并且必须通过。
> 
> *   **$new_directory_path :** 此参数表示新的目录路径(即目标路径)。
> 
> **返回值:**它返回一个布尔运算符作为返回值，但实际上根据需要更改了当前目录。

**示例:**

```php
Input : CWD: /home/
        chdir("gfg")
Output : CWD: /home/gfg
Explanation : Current working directory(CWD)
was changed from '/home/' to '/home/gfg'.

Input : CWD: /home/Documents/
        chdir("foldergfg/inside_folder_gfg")
Output : CWD: /home/Documents/foldergfg/inside_folder_gfg

Explanation : Current working directory (CWD)
was changed from '/home/Documents/' to '/home/
Documents/folder_gfg/inside_folder_gfg'.

```

**错误和异常:**
该函数成功时返回真，失败时返回假。因此，它在失败时给出一个**错误/ E_WARNING** 。通常，当目标目录路径无效时，会出现故障情况。

**适用版本:**
该功能适用于 PHP 4、PHP 5、PHP 7。

**程序 1:**

```php
<?php
// To get current working directory
echo getcwd() . "<br>";

// Change directory function
chdir("testing_gfg");

// To get current working directory
echo getcwd();
?> 
```

**输出:**

```php
/var/www/html
/var/www/html/testing_gfg

```

最初当前的工作目录是“/var/www/html”。应用 chdir()函数后，当前工作目录改为“/var/www/html/testing_gfg”目录。同样，chdir()函数可以用来改变目录。
**节目 2:**

```php
<?php
// To get current working directory
echo getcwd() . "<br>";

// Change directory function
chdir("GFG/Geeks");

// To get current working directory
echo getcwd();
?> 
```

**输出:**

```php
/home
/home/GFG/Geeks

```

**参考文献:**T2】http://php.net/manual/en/function.chdir.php