# PHP|DirectoryIterator getSize()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-getsize-function/](https://www.geeksforgeeks.org/php-directoryiterator-getsize-function/)

**DirectoryIterator：：getSize()函数**是 PHP 中的内置函数，用于返回当前 DirectoryIterator 项的大小。

**语法：**

```
*int* DirectoryIterator::getSize( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回文件的大小(以字节为单位)。

下面的程序演示了 PHP 中的 DirectoryIterator：：getSize()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check it is directory or not
    if ($directory->isDir()) {
        $file = $directory->current();
        echo $file->getFilename() . " | Size: "
                . $directory->getSize() . "<br>";
    }

    // Move to next element of directory
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

    $file = $directory->current();

    echo $dir->key() . " => " . 
        $file->getFilename() . " | Size: " .
        $dir->getSize() . "<br>";
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.getsize.php](https://www.php.net/manual/en/directoryiterator.getsize.php)