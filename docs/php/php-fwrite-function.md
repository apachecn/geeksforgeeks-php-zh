# PHP|fwrite()函数

> Original: [https://www.geeksforgeeks.org/php-fwrite-function/](https://www.geeksforgeeks.org/php-fwrite-function/)

PHP 中的 fwrite()函数是一个内置函数，用于写入打开的文件。 Fwrite()函数在文件末尾或达到作为参数传递的指定长度时停止(以先到者为准)。 必须写入的文件、字符串和长度作为参数发送给 fwrite()函数，它在成功时返回写入的字节数，在失败时返回 False。

**语法：**

```php
fwrite(file, string, length)
```

**参数：**PHP 中的 fwrite()函数接受三个参数。

1.  **FILE** : specifies the required parameters for the file.
2.  **String** : a required parameter that specifies the string to write.
3.  **Length** : optional parameter that specifies the maximum number of bytes to write.

**返回值：**成功时返回写入的字节数，失败时返回 False。

**例外**：

1.  因为 fwrite()是二进制安全的，所以像图像和字符数据这样的二进制数据都可以用这个函数写入。
2.  如果对文件指针执行两次写入操作，则数据将附加到文件内容的末尾。

**示例：**

```php
Input : $myfile = fopen("gfg.txt", "w");
        echo fwrite($myfile, "Geeksforgeeks is a portal for geeks!");
        fclose($myfile);
Output : 36

Input : $myfile = fopen("gfg.txt", "w");
        echo fwrite($myfile, "PhP is Simple to Learn!");
        echo fwrite($myfile, "Geeksforgeeks is a portal for geeks!");
        fclose($myfile);
Output : 23
         59

```

以下程序说明了 fwrite()函数：

**程序 1**：

```php
<?php
// Opening a file
$myfile = fopen("gfg.txt", "w");

// writing content to a file using fwrite()
echo fwrite($myfile, "Geeksforgeeks is a portal for geeks!");

// closing the file
fclose($myfile);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2**：

```php
<?php
// Opening a file
$myfile = fopen("gfg.txt", "w");

// writing content to a file using fwrite()
echo fwrite($myfile, "PhP is Simple to Learn!");
echo fwrite($myfile, "Geeksforgeeks is a portal for geeks!");

// closing the file
fclose($myfile);
?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.fwrite.php](http://php.net/manual/en/function.fwrite.php)