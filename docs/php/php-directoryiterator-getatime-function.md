# PHP|DirectoryIterator getATime()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-getatime-function/](https://www.geeksforgeeks.org/php-directoryiterator-getatime-function/)

**DirectoryIterator：：getATime()函数**是 PHP 中的内置函数，用于获取当前 DirectoryIterator 项的最后访问时间。

**语法：**

```php
*int* DirectoryIterator::getATime( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数以 Unix 时间戳的形式返回上次访问文件的时间。

下面的程序演示了 PHP 中的 DirectoryIterator：：getATime()函数：

**程序 1：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check for directory element
    if ($directory->isDir()) {
        $file = $directory->current();

        // Display the filename and last accessed time
        echo $file->getFilename() . " | ATime: "
                . $directory->getATime() . "<br>";
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

    $file = $directory->current();

    // Display the key, filename and its
    // last accessed time
    echo $dir->key() . " => " . 
        $file->getFilename() . " | ATime: " .
        $dir->getATime() . "<br>";
}
?> 
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.getatime.php](https://www.php.net/manual/en/directoryiterator.getatime.php)