# PHP|DirectoryIterator isFile()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-isfile-function/](https://www.geeksforgeeks.org/php-directoryiterator-isfile-function/)

**DirectoryIterator：：isFile()函数**是 PHP 中的内置函数，用于检查当前 DirectoryIterator 项是否为常规文件。

**语法：**

```php
*bool* DirectoryIterator::isFile( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果文件存在并且是常规文件(不是链接或目录)，则此函数返回 TRUE，否则返回 FALSE。

下面的程序说明了 PHP 中的 DirectoryIterator：：isFile()函数：

**程序 1：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs for each element of directory
foreach($directory as $dir) {

    // Check the directory element is file
    if($dir->isFile()) {

        // Display the filename
        echo $dir->getFilename() . "<br>";
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check the directory element is file
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

**引用：**[https://www.php.net/manual/en/directoryiterator.isfile.php](https://www.php.net/manual/en/directoryiterator.isfile.php)