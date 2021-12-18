# PHP|fput()函数

> Original: [https://www.geeksforgeeks.org/php-fputs-function/](https://www.geeksforgeeks.org/php-fputs-function/)

PHP 中的 fput()函数是一个内置函数，用于写入打开的文件。
fput()函数在文件末尾或达到作为参数传递的指定长度时(以先到者为准)停止。
必须写入的文件、字符串和长度作为参数发送给 fput()函数，它在成功时返回写入的字节数，在失败时返回 False。
fput()函数是 fwrite()函数的别名。

**语法：**

```php
fputs(file, string, length)
```

**使用的参数：**
PHP 中的 fput()函数接受三个参数。

1.  文件：必选参数，指定文件。
2.  字符串：必选参数，指定要写入的字符串。
3.  长度：可选参数，指定要写入的最大字节数。

**返回值：**
它返回成功时写入的字节数，失败时返回 False。

**例外**

1.  由于 fput()是二进制安全的，因此可以使用该函数写入二进制数据，如图像和字符数据。
2.  不带 LENGTH 参数的 fput()函数将所有数据写到末尾，但它不包括遇到的第一个第 0 个字节。

**示例：**

```php
Input : $myfile = fopen("gfg.txt", "w");
        echo fputs($myfile, "Geeksforgeeks is a portal of geeks!");
        fclose($myfile);
Output : 35

Input : $myfile = fopen("gfg.txt", "w");
        echo fputs($myfile, "Geeksforgeeks is a portal of geeks!", 13);
        fclose($myfile);
        fopen("gfg.txt", "r");
        echo fread($myfile, filesize("gfg.txt"));
        fclose($myfile);
Output : Geeksforgeeks

```

以下程序说明了 fput()函数：

**程序 1**

```php
<?php
// Opening a file
$myfile = fopen("gfg.txt", "w");

// writing content to a file using fputs
echo fputs($myfile, "Geeksforgeeks is a portal of geeks!");

// closing the file
fclose($myfile);
?>
```

发帖主题：Re：Колибри0.7.0

```php
35

```

**程序 2**

```php
<?php
// Opening a file
$myfile = fopen("gfg.txt", "w");

// writing content to a file with a specified string length using fputs
echo fputs($myfile, "Geeksforgeeks is a portal of geeks!", 13);

// closing the file
fclose($myfile);

//opening the same file to read its contents        
fopen("gfg.txt", "r");
echo fread($myfile, filesize("gfg.txt"));

// closing the file
fclose($myfile);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Geeksforgeeks

```

**引用：**
[http://php.net/manual/en/function.fputs.php](http://php.net/manual/en/function.fputs.php)