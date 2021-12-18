# PHP|DirectoryIterator getPerms()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-getperms-function/](https://www.geeksforgeeks.org/php-directoryiterator-getperms-function/)

**DirectoryIterator：：getPerms()函数**是 PHP 中的内置函数，用于获取当前 DirectoryIterator 项的权限。

**语法：**

```php
*int* DirectoryIterator::getPerms( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数将文件权限还原为十进制整数。

下面的程序演示了 PHP 中的 DirectoryIterator：：getPerms()函数：

**程序 1：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // If not a dot folder
    if (!$directory->isDot()) {
        $perms = substr(sprintf('%o', $directory->getPerms()), -4);

        // Display the filename with permission
        echo $directory->getFilename() . " " 
            . " | Permission: " . $perms . "<br>";
    }
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

    // If not a dot folder
    if (!$dir->isDot()) {
        $perms = substr(sprintf('%o', $dir->getPerms()), -4);

        // Display the filename with permission
        echo $dir->getFilename() . " " 
                . " | Permission: " . $perms . "<br>";
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.getperms.php](https://www.php.net/manual/en/directoryiterator.getperms.php)