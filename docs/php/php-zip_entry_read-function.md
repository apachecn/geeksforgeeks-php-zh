# PHP|zip_entry_read()函数

> Original: [https://www.geeksforgeeks.org/php-zip_entry_read-function/](https://www.geeksforgeeks.org/php-zip_entry_read-function/)

函数的作用是：它是 PHP 中的一个内置函数，用于从打开的 zip 存档条目中读取内容。 正在读取压缩条目，返回的字节数可以作为参数发送给 zip_entry_read()函数，如果成功，它将返回指定压缩条目的内容，否则将返回 PHP 警告。

**语法：**

```
string zip_entry_read( $zip_entry, $length )
```

**参数：**此函数接受上述两个参数，如下所述。

*   **$zip_entry：**它是指定 zip 条目资源的强制参数。
*   **$length：**它是一个可选参数，指定要返回的字节数。

**返回值：**如果成功则返回指定 zip 条目的内容，否则返回 PHP 警告。

**错误和异常：**

*   如果 zip 存档无效，则函数的作用是：返回一个 ER_OPEN 错误。
*   函数的作用是：如果压缩存档为空，则返回 ER_NOZIP 错误。

下面的程序演示了 PHP 中的 zip_entry_read()函数：

**程序 1：**

> 假设一个 zip 文件 Tistrle.zip 包含以下文件：
> **geeks.txt**

```
<?php

// Opening a zip file
$zip_handle = zip_open("C:/xampp/htdocs/articles.zip");

// Reading a zip archive entry
while($zip_entry = zip_read($zip_handle)) 
{ 
    $resource = zip_entry_open($zip_handle, $zip_entry, "rb");
    $file_name = zip_entry_name($zip_entry);

    if ($resource == true) 
    { 

        // Reading contents of a zip archive entry
        $file_content = zip_entry_read($zip_entry);
        echo("File: " . $file_name . " successfully opened. <br>");
        echo("File content: " . $file_content);

        // Closing a zip archive entry
        zip_entry_close($zip_entry);
    } 
    else
        echo("Failed to Open.");
}

// Closin zip file.
zip_close($zip_handle);
?>
```

发帖主题：Re：Колибри0.7.0

```
File: articles/geeks successfully opened. 
File content: Welcome to GeeksforGeeks. It is a computer science portal
where you can learn programming.

```

**程序 2**：

> 假设一个压缩文件 Tistrle.zip 包含以下文件：
>  **geeks.txt
> geeks1.txt**

```
<?php

// Opening a zip file
$zip_handle = zip_open("C:/xampp/htdocs/articles.zip");

// Reading a zip archive entry
while($zip_entry = zip_read($zip_handle)) 
{ 
    $resource = zip_entry_open($zip_handle, $zip_entry, "rb");
    $file_name = zip_entry_name($zip_entry);
    if ($resource == true) 
    { 

        // Reading contents of a zip archive entry upto 150 bytes
        $file_content = zip_entry_read($zip_entry, 150);
        echo("File Name: " . $file_name . " is opened Successfully. <br>");
        echo($file_content);
        echo("<br><br>");

        // Closing a zip archive entry
        zip_entry_close($zip_entry);
    } 
    else
        echo("Failed to Open.");
} 

// Closing a zip archive
zip_close($zip_handle);
?>
```

发帖主题：Re：Колибри0.7.0

```
File Name: articles/geeks is opened Successfully. 
Welcome to GeeksforGeeks. It is a computer science portal where you
can learn programming.

File Name: articles/geeks1 is opened Successfully. 
A Computer Science portal for geeks. It contains well written, well
thought and well-explained computer science and programming articles,
quizzes and many more. 

```

**相关文章：**

*   [PHP|zip_entry_name()函数](https://www.geeksforgeeks.org/php-zip_entry_name-function/)
*   [PHP|zip_read()函数](https://www.geeksforgeeks.org/php-zip_read-function/)
*   [PHP|zip_entry_filesize()函数](https://www.geeksforgeeks.org/php-zip_entry_filesize-function/)

**引用：**[http://php.net/manual/en/function.zip-entry-read.php](http://php.net/manual/en/function.zip-entry-read.php)