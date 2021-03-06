# PHP|DirectoryIterator key()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-key-function/](https://www.geeksforgeeks.org/php-directoryiterator-key-function/)

**DirectoryIterator：：key()函数**是 PHP 中的内置函数，用于返回当前 DirectoryIterator 项的键。

**语法：**

```php
*string* DirectoryIterator::key( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回当前 DirectoryIterator 项的键。

下面的程序说明了 PHP 中的 DirectoryIterator：：Key()函数：

**程序 1：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs for each element of directory
foreach($directory as $dir) {

    // Display the key and filename
    echo $dir->key() . " => " . 
    $dir->getFilename() . "<br>";
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

**引用：**[https://www.php.net/manual/en/directoryiterator.key.php](https://www.php.net/manual/en/directoryiterator.key.php)