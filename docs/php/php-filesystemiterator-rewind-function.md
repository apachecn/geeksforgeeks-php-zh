# PHP|FilesystemIterator 倒带()函数

> Original: [https://www.geeksforgeeks.org/php-filesystemiterator-rewind-function/](https://www.geeksforgeeks.org/php-filesystemiterator-rewind-function/)

**FilesystemIterator：：Rewind()函数**是 PHP 中的一个内置函数，用于倒带到文件的开头。

**语法：**

```
*void* FilesystemIterator::rewind( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 FilesystemIterator：：Rewind()函数：

**程序 1：**

```
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(dirname(__FILE__), 
        FilesystemIterator::KEY_AS_FILENAME);

// Loop runs while file iterator is valid
while ($fileItr->valid()) {

    // Check for non-directory element
    if (!$fileItr->isDir()) {

        // Display the key
        echo $fileItr->key() . "<br>"; 
    }

    // Move to the next element
    $fileItr->next();
}

// Rewind back to start position
$fileItr->rewind();

// Display the key
echo "<br>After using rewind() function <br>";

echo $fileItr->key();

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(__DIR__, 
    FilesystemIterator::CURRENT_AS_PATHNAME);

// Loop runs for each element
foreach($fileItr as $it) {

    // Display the current element
    echo $fileItr->current() . "<br>";
}

// Rewind back to start position
$fileItr->rewind();

// Display the key
echo "<br>After using rewind() function <br>";

echo $fileItr->key();

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/filesystemiterator.rewind.php](https://www.php.net/manual/en/filesystemiterator.rewind.php)