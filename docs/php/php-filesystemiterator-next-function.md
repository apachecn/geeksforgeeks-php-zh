# PHP|FilesystemIterator Next()函数

> Original: [https://www.geeksforgeeks.org/php-filesystemiterator-next-function/](https://www.geeksforgeeks.org/php-filesystemiterator-next-function/)

**FilesystemIterator：：Next()函数**是 PHP 中的一个内置函数，用于移动到下一个文件元素。

**语法：**

```
*void* FilesystemIterator::next( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 FilesystemIterator：：Next()函数：

**程序 1：**

```
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(dirname(__FILE__));

// Check for validity of file iterator
while ($fileItr->valid()) {

    // Check for directory
    if ($fileItr->isDir()) {

        // Display the filename
        echo $fileItr->getFilename() . "<br>";
    }

    // Move to the next element
    $fileItr->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(dirname(__FILE__), 
        FilesystemIterator::KEY_AS_FILENAME);

// Loop runs while file iterator is valid
while ($fileItr->valid()) {

    // Check if file iterator is not directory
    if (!$fileItr->isDir()) {

        // Display the key element
        echo $fileItr->key() . "<br>"; 
    }

    // Move to the next element
    $fileItr->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/filesystemiterator.next.php](https://www.php.net/manual/en/filesystemiterator.next.php)