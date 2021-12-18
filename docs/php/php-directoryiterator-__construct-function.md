# PHP|DirectoryIterator__Construction()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-__construct-function/](https://www.geeksforgeeks.org/php-directoryiterator-__construct-function/)

**DirectoryIterator：：__Construct()函数**是 PHP 中的内置函数，用于从路径构造新的目录迭代器。

**语法：**

```
*public* DirectoryIterator::__construct( *string* $path )
```

**参数：**此函数接受单个参数$PATH，该参数保存要遍历的目录的路径。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的 DirectoryIterator：：__Construct()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs for each element of directory
foreach ($directory as $dir) {

    // Check if directory element is valid
    if ($dir->valid()) {

        // Display the filename
        echo $dir->getFilename() . "<br>";
    }
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

    // Check or directory element
    if ($directory->isDir()) {

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

**引用：**[https://www.php.net/manual/en/directoryiterator.construct.php](https://www.php.net/manual/en/directoryiterator.construct.php)