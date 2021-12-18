# PHP|DirectoryIterator isDir()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-isdir-function/](https://www.geeksforgeeks.org/php-directoryiterator-isdir-function/)

**DirectoryIterator：：isDir()函数**是 PHP 中的内置函数，用于检查当前 DirectoryIterator 项是否为目录。

**语法：**

```
*bool* DirectoryIterator::isDir( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果目录存在，此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 DirectoryIterator：：isDir()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check for directory element
    if ($directory->isDir()) {
        $file = $directory->current();

        // Display the filename and its size
        echo $file->getFilename() . " | Size: "
                . $directory->getSize() . "<br>";
    }

    // Move to the next element
    $directory->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check for directory element
    if ($directory->isDir()) {
        $file = $directory->current();

        // Display file name and last modified time
        echo $file->getFilename() . " | MTime: "
                . $directory->getMTime() . "<br>";
    }

    // Move to the next element
    $directory->next();
}
?> 
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.isdir.php](https://www.php.net/manual/en/directoryiterator.isdir.php)