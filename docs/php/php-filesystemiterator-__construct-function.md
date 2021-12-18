# PHP|FilesystemIterator__Construct()函数

> Original: [https://www.geeksforgeeks.org/php-filesystemiterator-__construct-function/](https://www.geeksforgeeks.org/php-filesystemiterator-__construct-function/)

**FilesystemIterator：：__Construct()函数**是 PHP 中的内置函数，用于构造新的文件系统迭代器。

**语法：**

```
*public* FilesystemIterator::__construct( *string* $path, *int* $flags )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$path:** this parameter saves the path of the file system entry.
*   **$FLAGS:** this parameter holds flags that provide the influence and behavior of certain methods.

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 FilesystemIterator：：__Construct()函数：

**程序 1：**

```
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(dirname(__FILE__));

// Loop runs for each element of filesystem
foreach ($fileItr as $file) {

    // Display the filename
    echo $file->getFilename() . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(dirname(__FILE__));

// Loop runs while file iterator is valid
while ($fileItr->valid()) {

    // Check for directory files
    if ($fileItr->isDir()) {

        // Display the file name
        echo $fileItr->getFilename() . "<br>";
    }

    // Move to the next element
    $fileItr->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/filesystemiterator.construct.php](https://www.php.net/manual/en/filesystemiterator.construct.php)