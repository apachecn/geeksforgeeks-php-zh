# PHP|rewindir()函数

> Original: [https://www.geeksforgeeks.org/php-rewinddir-function/](https://www.geeksforgeeks.org/php-rewinddir-function/)

Rewindir()函数是 PHP 中的一个内置函数，用于倒带目录句柄。 函数的作用是：打开一个目录并列出它的文件，重置目录句柄，再次列出它的文件，最后关闭目录句柄。
作为参数发送给 rewindir()函数的目录句柄，成功时返回 Null，失败时返回 False。

**语法：**

```php
rewinddir ( $dir_handle )
```

**参数：**rewindir()函数接受单个参数*$dir_handle*。 它是一个强制参数，用于指定以前由 opendir()函数打开的句柄资源。

**返回值：**成功时返回 Null，失败时返回 False。

**错误和异常**：

*   如果用户没有指定目录句柄参数，那么 rewindir()函数将假定 opendir()打开的最后一个链接。
*   Rewindir()等同于 clodir()、opendir()序列，但没有获得新的句柄。

以下程序说明了 PHP 中的 rewindir()函数：
**程序 1：**

```php
<?php

// Open a directory
$dir_handle = opendir("C:/xampp/htdocs/gfg");

// Read the contents of directory
while(($file_name = readdir($dir_handle)) !== false) 
{ 
    echo("File Name: " . $file_name . "<br>");
}

// Rewinding directory
rewinddir($dir_handle);

while(($file_Name = readdir($dir_handle)) !== false) 
{ 
    echo("File Name: " . $file_Name . "<br>");
} 

// Close directory
closedir($dir_handle);
?>
```

发帖主题：Re：Колибри0.7.0

```php
File Name: .
File Name: ..
File Name: content.xlsx
File Name: gfg.pdf
File Name: image.jpeg
File Name: .
File Name: ..
File Name: content.xlsx
File Name: gfg.pdf
File Name: image.jpeg

```

**程序 2：**

```php
<?php

// Directory path
$dir_name = "C:/xampp/htdocs/gfg";

// Open directory and read the content
// of directory
if (is_dir($dir_name)) {
  if ($dir_handle = opendir($dir_name)) {

    // List files in images directory
    while (($file_name = readdir($dir_handle)) !== false) {
      echo "File Name:" . $file_name . "<br>";
    }

    // Rewing the directory
    rewinddir();

    // List once again files in images directory
    while (($file_name = readdir($dir_handle)) !== false) {
      echo "File Name:" . $file_name . "<br>";
    }

    // Close the directory
    closedir($dir_handle);
  }
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
filename:.
filename:..
filename:content.xlsx
filename:gfg.pdf
filename:image.jpeg
filename:.
filename:..
filename:content.xlsx
filename:gfg.pdf
filename:image.jpeg

```

**引用：**[http://php.net/manual/en/function.rewinddir.php](http://php.net/manual/en/function.rewinddir.php)