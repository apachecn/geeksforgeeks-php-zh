# PHP|DirectoryIterator Current()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-current-function/](https://www.geeksforgeeks.org/php-directoryiterator-current-function/)

**DirectoryIterator：：Current()函数**是 PHP 中的内置函数，用于返回当前 DirectoryIterator 项。

**语法：**

```
*DirectoryIterator* DirectoryIterator::current( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回当前的 DirectoryIterator 项。

下面的程序说明了 PHP 中的 DirectoryIterator：：Current()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check for directory element
    if ($directory->isDir()) {

        // Store the current element
        $file = $directory->current();

        // Display the filename
        echo $file->getFilename() . "<br>";
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

// Loop runs for each element of directory
foreach($directory as $dir) {

    // Store the current element
    $file = $directory->current();

    // Display the key and filename
    echo $dir->key() . " => " . 
        $file->getFilename() . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.current.php](https://www.php.net/manual/en/directoryiterator.current.php)