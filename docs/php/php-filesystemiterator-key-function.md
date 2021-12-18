# PHP|FilesystemIterator key()函数

> Original: [https://www.geeksforgeeks.org/php-filesystemiterator-key-function/](https://www.geeksforgeeks.org/php-filesystemiterator-key-function/)

**FilesystemIterator：：key()函数**是 PHP 中的一个内置函数，用于检索当前文件的密钥。

**语法：**

```php
*string* FilesystemIterator::key( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数根据设置的标志返回路径名或文件名。

下面的程序演示了 PHP 中的 FilesystemIterator：：Key()函数：

**程序 1：**

```php
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(dirname(__FILE__), 
        FilesystemIterator::KEY_AS_FILENAME);

// Loop runs for each element of file iterator
foreach($fileItr as $it) {

    // Display the key
    echo $fileItr->key() . "<br>"; 
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(dirname(__FILE__), 
        FilesystemIterator::KEY_AS_FILENAME);

// Loop runs while file iterator is valid
while ($fileItr->valid()) {

    // Check for non directory files
    if (!$fileItr->isDir()) {

        // Display the key
        echo $fileItr->key() . "<br>"; 
    }

    // Move to the next element
    $fileItr->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/filesystemiterator.key.php](https://www.php.net/manual/en/filesystemiterator.key.php)