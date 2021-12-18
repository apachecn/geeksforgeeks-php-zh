# PHP|zip_entry_open()函数

> Original: [https://www.geeksforgeeks.org/php-zip_entry_open-function/](https://www.geeksforgeeks.org/php-zip_entry_open-function/)

函数的作用是：在 PHP 中内置函数，用于打开要读取的 zip 条目存档。 使用 ZIP_ENTRY_OPEN 函数打开 Zip 存档中的文件或目录会创建一个新流，并在该流与 Zip 存档中的文件或目录之间建立连接。 要打开并作为参数发送给 zip_entry_open()函数的 zip 资源和 zip 条目资源，成功时返回 True，失败时返回 False。

**语法：**

```
bool zip_entry_open( $zip, $zip_entry, $mode )
```

**参数：**此函数接受上述三个参数，如下所述：

*   **$zip：**这是一个强制参数，指定要读取的 zip 资源。
*   **$zip_entry：**它是指定 zip 条目资源的强制参数。
*   **$mode：**为可选参数，压缩档案的访问类型为必填项。

**返回值：**成功返回 True，失败返回 False。

**错误和异常：**

*   函数的作用是：如果压缩档案无效，则返回 ER_OPEN 错误。
*   函数的作用是：如果压缩存档为空，则返回 ER_NOZIP 错误。

下面的程序演示了 PHP 中的 zip_entry_open()函数：

**程序 1：**

> 假设压缩文件 articles.zip 包含以下文件：
> **geeks.txt**

```
<?php

// Opening a zip file
$zip_handle = zip_open("C:/xampp/htdocs/articles.zip");
$zip_entry = zip_read($zip_handle);

// Opening a zip entry archive 
zip_entry_open($zip_handle, $zip_entry, "rb");
$file = zip_entry_name($zip_entry);

if($file == true)
    echo("Zip file: " . $file . " open successfully <br>");
// Closing a zip entry archive 
$flag = zip_entry_close($zip_entry);
if ($flag == true) 
    echo("Zip file: " . $file . " closed successfully");
else
    echo("Zip file: " . $file . " cannot be closed");

// Closeing zip file
zip_close($zip_handle);
?>
```

发帖主题：Re：Колибри0.7.0

```
Zip file: articles/geeks open successfully 
Zip file: articles/geeks closed successfully

```

**程序 2：**

> 假设一个压缩文件 articles.zip 包含以下文件：
> **geeks.txt
> geeks1.txt**

```
<?php

// Opening a zip file
$zip_handle = zip_open("C:/xampp/htdocs/articles.zip");

if(is_resource($zip_handle)) 
{ 
    while($zip_entry = zip_read($zip_handle)) 
    { 

        // Opening a zip archive entry
        $file = zip_entry_open($zip_handle, $zip_entry, "rb");
        $file_name = zip_entry_name($zip_entry);

        if ($file == true) 
        { 
            echo("Zip file: " . $file_name . " open successfully");
            echo "<br>" ; 

            // Closing a zip archive entry
            $flag = zip_entry_close($zip_entry);

            if ($flag == true) 
                  echo("Zip file: " . $file_name .
                      " closed successfully <br><br>");
            else
                echo("Zip file: " . $file_name . 
                         " cannot be closed <br><br>");
        } 
        else
            echo("Zip Entry Cannot be opened.<br>");
    } 

    // Closing a zip archive
    zip_close($zip_handle);
}
else
    echo("Failed to Open" . $zip_handle );
?>
```

发帖主题：Re：Колибри0.7.0

```
Zip file: articles/geeks open successfully
Zip file: articles/geeks closed successfully 

Zip file: articles/geeks1 open successfully
Zip file: articles/geeks1 closed successfully

```

**相关文章：**

*   [PHP|zip_entry_close()函数](https://www.geeksforgeeks.org/php-zip_entry_close-function/)
*   [PHP|ZIP_ENTRY_COMPRESEDSIZE()函数](https://www.geeksforgeeks.org/php-zip_entry_compressedsize-function/)
*   [PHP|zip_entry_name()函数](https://www.geeksforgeeks.org/php-zip_entry_name-function/)
*   [PHP|zip_entry_filesize()函数](https://www.geeksforgeeks.org/php-zip_entry_filesize-function/)

**引用：**[http://php.net/manual/en/function.zip-entry-open.php](http://php.net/manual/en/function.zip-entry-open.php)