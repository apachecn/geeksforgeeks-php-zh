# PHP|DirectoryIterator getPath()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-getpath-function/](https://www.geeksforgeeks.org/php-directoryiterator-getpath-function/)

**DirectoryIterator：：getPath()函数**是 PHP 中的一个内置函数，用于获取当前迭代器项的路径，不带文件名。

**语法：**

```php
*string* DirectoryIterator::getPath( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回文件路径，省略文件名和任何尾随斜杠。

下面的程序演示了 PHP 中的 DirectoryIterator：：getPath()函数：

**程序 1：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Display the path
echo $directory->getPath();
?> 
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs for each element of directory
foreach($directory as $dir) {

    $file = $directory->current();

    // Display key, filename and its path
    echo $dir->key() . " => " . 
        $file->getFilename() . " | Path: " .
        $directory->getPath() . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.getpath.php](https://www.php.net/manual/en/directoryiterator.getpath.php)