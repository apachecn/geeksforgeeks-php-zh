# PHP|DirectoryIterator Valid()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-valid-function/](https://www.geeksforgeeks.org/php-directoryiterator-valid-function/)

**DirectoryIterator：：Valid()函数**是 PHP 中的内置函数，用于检查当前 DirectoryIterator 位置是否为有效文件。

**语法：**

```
*bool* DirectoryIterator::valid( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果位置有效，此函数返回 TRUE，否则返回 FALSE。

下面的程序演示了 PHP 中的 DirectoryIterator：：Valid()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Move to the third element
$directory->seek(2);

// Check the validity of directory element 
if($directory->valid()) {

    // Display the filename
    echo $directory->getFilename();
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
    if($directory->isDir()) {

        // Display the key and filename
        echo $directory->key() . " => " . 
        $directory->getFilename() . "<br>";
    }

    // Move to the next element
    $directory->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.valid.php](https://www.php.net/manual/en/directoryiterator.valid.php)