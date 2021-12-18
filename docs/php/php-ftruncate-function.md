# PHP|ftruncate()函数

> Original: [https://www.geeksforgeeks.org/php-ftruncate-function/](https://www.geeksforgeeks.org/php-ftruncate-function/)

PHP 中的 ftruncate()函数是一个内置函数，用于将打开的文件截断(缩短)到指定长度。 文件和文件的新大小作为参数发送给 ftruncate()函数，成功时返回 True，失败时返回 False。 如果参数中指定的大小大于文件，则使用空字节扩展文件，如果指定的大小小于文件，则将文件截断为该大小。

**语法：**

```
ftruncate(file, size)
```

**参数：**PHP 中的 ftruncate()函数接受两个参数。

1.  **FILE** : specifies the required parameters for the file.
2.  **SIZE** : a required parameter that specifies the new size of the file.

**返回值：**成功返回 True，失败返回 False。

**例外**：

1.  要替换文件内容，必须在 ftruncate()函数之后使用 rewind()函数。
2.  Ftruncate()函数不会更改文件指针。
3.  如果参数中指定的大小大于文件，则使用空字节扩展文件；如果指定的大小小于文件，则将文件截断为该大小

以下程序说明了 ftruncate()函数：

**程序 1**：

```
<?php
// checking filesize before truncating
echo filesize("gfg.txt");

// Opening the file
$myfile = fopen("gfg.txt", "a+");

// truncating the file
ftruncate($myfile, 10);

// closing the file
fclose($file);

// Clearing cache and checking filesize again
clearstatcache();
echo filesize("gfg.txt");

// closing the file
fclose($myfile);
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2**：

```
<?php
$myfile = 'gfg.txt';

// opening file in read mode
$myhandle = fopen($myfile, 'r+');

// truncating the file
ftruncate($myhandle, rand(1, filesize($myfile)));

// using reiwnd() to replace file content
rewind($myhandle);
echo fread($myhandle, filesize($myfile));

// closing the file
fclose($handle);

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[http://php.net/manual/en/function.ftruncate.php](http://php.net/manual/en/function.ftruncate.php)