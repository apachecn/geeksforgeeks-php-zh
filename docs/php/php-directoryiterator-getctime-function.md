# PHP|DirectoryIterator getCTime()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-getctime-function/](https://www.geeksforgeeks.org/php-directoryiterator-getctime-function/)

**DirectoryIterator：：getCTime()函数**是 PHP 中的一个内置函数，用于获取当前 DirectoryIterator 项的 inode 更改时间。

**语法：**

```php
*int* DirectoryIterator::getCTime( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数以 Unix 时间戳格式返回文件的最后更改时间。

下面的程序演示了 PHP 中的 DirectoryIterator：：getCTime()函数：

**程序 1：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check if the element is directory
    if ($directory->isDir()) {

        // Store the current element
        $file = $directory->current();

        // Display the file name and 
        // inode change time
        echo $file->getFilename() . " | CTime: "
                . $directory->getCTime() . "<br>";
    }

    // Move to the next element
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

    // Display the key, filename and 
    // its inode change time
    echo $dir->key() . " => " . 
        $file->getFilename() . " | CTime: " .
        $dir->getCTime() . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.getctime.php](https://www.php.net/manual/en/directoryiterator.getctime.php)