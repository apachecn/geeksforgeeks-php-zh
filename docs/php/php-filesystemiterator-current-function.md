# PHP|FilesystemIterator Current()函数

> Original: [https://www.geeksforgeeks.org/php-filesystemiterator-current-function/](https://www.geeksforgeeks.org/php-filesystemiterator-current-function/)

**FilesystemIterator：：Current()函数**是 PHP 中的内置函数，用于返回当前元素的文件信息。

**语法：**

```php
*mixed* FilesystemIterator::current( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数根据设置的标志返回文件名、文件信息或$this。

下面的程序演示了 PHP 中的 FilesystemIterator：：Current()函数：

**程序 1：**

```php
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(__DIR__, 
    FilesystemIterator::CURRENT_AS_PATHNAME);

// Loop runs for each element
foreach($fileItr as $it) {

    // Display the current element
    echo $fileItr->current() . "<br>";
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(__DIR__, 
    FilesystemIterator::CURRENT_AS_PATHNAME);

// Loop runs file iterator is valid
while ($fileItr->valid()) {

    // Check for directory file iterator
    if ($fileItr->isDir()) {

        // Display the current element
        echo $fileItr->current() . "<br>";
    }

    // Move to the next file iterator
    $fileItr->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/filesystemiterator.current.php](https://www.php.net/manual/en/filesystemiterator.current.php)