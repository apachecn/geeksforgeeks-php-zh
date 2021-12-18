# PHP|DirectoryIterator getMTime()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-getmtime-function/](https://www.geeksforgeeks.org/php-directoryiterator-getmtime-function/)

**DirectoryIterator：：getMTime()函数**是 PHP 中的内置函数，用于返回当前 DirectoryIterator 项的最后修改时间。

**语法：**

```php
*int* DirectoryIterator::getMTime( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回文件的最后修改时间，格式为 Unix 时间戳。

下面的程序演示了 PHP 中的 DirectoryIterator：：getMTime()函数：

**程序 1：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check it is directory or not
    if ($directory->isDir()) {

        $file = $directory->current();

        // Displaty the filename and last modified time
        echo $file->getFilename() . " | MTime: "
                . $directory->getMTime() . "<br>";
    }

    // Move to the next element of directory
    $directory->next();
}
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

    // Store the current element of directory
    $file = $directory->current();

    // Display the key, filename and last modified time
    echo $dir->key() . " => " . 
        $file->getFilename() . " | MTime: " .
        $dir->getMTime() . "<br>";
}
?> 
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.getmtime.php](https://www.php.net/manual/en/directoryiterator.getmtime.php)