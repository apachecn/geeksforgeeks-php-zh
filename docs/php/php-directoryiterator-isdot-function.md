# PHP|DirectoryIterator isDot()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-isdot-function/](https://www.geeksforgeeks.org/php-directoryiterator-isdot-function/)

**DirectoryIterator：：isDot()函数**是 PHP 中的内置函数，用于检查当前 DirectoryIterator 项是否为‘’。 或“..”

**语法：**

```
*bool* DirectoryIterator::isDot( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果条目为，则此函数返回 TRUE。 或者..，否则就是假的。

以下程序说明了 PHP 中的 DirectoryIterator：：isDot()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs for each element of directory
foreach($directory as $dir) {

    // Check if not a dot directory
    if (!$dir->isDot()) {

        // Display directory element and its permission
        $perms = substr(sprintf('%o', $dir->getPerms()), -4);
        echo $dir->getFilename() . " " 
        . " | Permission: " . $perms . "<br>";
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

    // Check if not a dot directory
    if (!$directory->isDot()) {
        echo $directory->getFilename() . "<br>";
    }
    $directory->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.isdot.php](https://www.php.net/manual/en/directoryiterator.isdot.php)