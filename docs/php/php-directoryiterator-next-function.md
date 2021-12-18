# PHP|DirectoryIterator Next()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-next-function/](https://www.geeksforgeeks.org/php-directoryiterator-next-function/)

**DirectoryIterator：：Next()函数**是 PHP 中的一个内置函数，用于前进到下一个 DirectoryIterator 项。

**语法：**

```
*void* DirectoryIterator::next( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 DirectoryIterator：：Next()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check for directory
    if($directory->isDir()) {

        // Display key and file name
        echo $directory->key() . " => " . 
        $directory->getFilename() . "<br>";
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

    // Check for file element
    if($directory->isFile()) {

        // Display the filename
        echo $directory->getFilename() . "<br>";
    }

    // Move to the next element
    $directory->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.next.php](https://www.php.net/manual/en/directoryiterator.next.php)