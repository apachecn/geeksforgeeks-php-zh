# PHP|SplFileInfo OpenFile()函数

> Original: [https://www.geeksforgeeks.org/php-splfileinfo-openfile-function/](https://www.geeksforgeeks.org/php-splfileinfo-openfile-function/)

SplFileInfo：：OpenFile()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取文件的 SplFileObject 对象。

**语法：**

```php
*bool* SplFileInfo::openFile( $mode, $path, $context)
```

**参数：**此函数接受上述三个参数，如下所述。

*   **$mode：**指定打开文件的模式。
*   **$path：**如果将其设置为 true，则在 PATH 中搜索文件名。
*   **$CONTEXT：**指定描述的手动路径。

**返回值：**此函数将打开的文件作为 SplFileObject 对象返回。

**注意：**确保文件可读或可写。

下面的程序演示了 PHP 中的 SplFileInfo：：OpenFile()函数：

**程序：**

```php
<?php

// PHP Program to illustrate 
// Splfileinfo::openFile function

// Make sure file is writable 
$file = new SplFileInfo("gfg.txt");

$obj = $file->openFile('a');

$obj->fwrite("Append...GeeksforGeeks to the file...");

?>
```

**追加文件前输出：**
**：**
![openfile](img/329aaa90c85f14c823e05dd0302a398a.png)

**追加文件后：**
![openfile](img/d4c43fc5f95802cdb7973843d4ef8448.png)

**引用：**[http://php.net/manual/en/splfileinfo.openfile.php](http://php.net/manual/en/splfileinfo.openfile.php)