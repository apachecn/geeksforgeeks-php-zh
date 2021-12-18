# PHP|REWIND()函数

> Original: [https://www.geeksforgeeks.org/php-rewind-function/](https://www.geeksforgeeks.org/php-rewind-function/)

PHP 中的 rewind()函数是一个内置函数，用于设置文件指针指向文件开头的位置。
如果文件是以追加(“a”或“a+”)模式打开的，则无论文件指针位置如何，写入文件的任何数据都将被追加。
必须在其上编辑指针的文件作为参数发送给 rewind()函数，如果成功则返回 True，如果失败则返回 False。

**语法：**

```php
rewind(file)
```

**使用的参数：**
PHP 中的 rewind()函数接受一个参数。

*   **file**：必选参数，指定要编辑的文件。

**返回值：**
成功时返回 True，失败时返回 False。

**错误和异常：**

1.  函数的作用是：在失败时生成 E_WARNING 级别的错误。
2.  要使用 rewind()函数，流必须是“可查找的”。
3.  如果文件是在追加模式下打开的，则无论指针的位置如何，写入的数据都会被追加。

例如：

```php
Input: $myfile = fopen("gfg.txt", "r");
        fseek($myfile, "10");
        rewind($myfile);
        fclose($file);

Output: 1

Input : $myfile = fopen("gfg.txt", "r+");
        fwrite($myfile, 'geeksforgeeks');
        rewind($myfile);
        fwrite($myfile, 'portal');
        rewind($myfile);
        echo fread($myfile, filesize("gfg.txt"));
        fclose($myfile);

Output : portalforgeeks
Here all characters of the file as it is after rewind "portal"

```

下面是演示 rewind()函数的程序。

**程序 1**

```php
<?php

$myfile = fopen("gfg.txt", "r");

// Changing the position of the file pointer
fseek($myfile, "10");

// Setting the file pointer to 0th 
// position using rewind() function
rewind($myfile);

// closing the file
fclose($file);

?>
```

发帖主题：Re：Колибри0.7.0

```php
1
```

**程序 2**

```php
<?php

$myfile = fopen("gfg.txt", "r+");

// writing to file
fwrite($myfile, 'geeksforgeeks a computer science portal');

// Setting the file pointer to 0th
// position using rewind() function
rewind($myfile);

// writing to file on 0th position
fwrite($myfile, 'geeksportal');
rewind($myfile);

// displaying the contents of the file
echo fread($myfile, filesize("gfg.txt"));

fclose($myfile);

?>
```

发帖主题：Re：Колибри0.7.0

```php
geeksportalks a computer science portal
```

**引用：**
[http://php.net/manual/en/function.rewind.php](http://php.net/manual/en/function.rewind.php)