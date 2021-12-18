# 使用 PHP 从 URL 下载文件

> 原文:[https://www . geesforgeks . org/download-file-from-URL-using-PHP/](https://www.geeksforgeeks.org/download-file-from-url-using-php/)

在本文中，我们将看到如何在 PHP 中从 URL 下载并保存文件，还将通过示例了解实现它的不同方法。从网址下载文件的方法有很多，下面讨论其中一些:

[**使用 file_get_contents()函数**](https://www.geeksforgeeks.org/php-file_get_contents-function/)**:**file _ get _ contents()函数用于将文件读入字符串。该函数使用服务器支持的内存映射技术，因此提高了性能，使其成为读取文件内容的首选方式。

**语法:**

```
file_get_contents($path, $include_path, $context, 
                  $start, $max_length)
```

**示例 1:** 本示例说明了使用 **file_get_contents()** 函数将文件读入字符串。

## PHP

```
<?php

    // Initialize a file URL to the variable
    $url = 
    'https://media.geeksforgeeks.org/wp-content/uploads/gfg-40.png';

    // Use basename() function to return the base name of file
    $file_name = basename($url);

    // Use file_get_contents() function to get the file
    // from url and use file_put_contents() function to
    // save the file by using base name
    if (file_put_contents($file_name, file_get_contents($url)))
    {
        echo "File downloaded successfully";
    }
    else
    {
        echo "File downloading failed.";
    }
?>
```