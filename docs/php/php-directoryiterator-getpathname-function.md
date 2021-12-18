# PHP|DirectoryIterator getPathname()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-getpathname-function/](https://www.geeksforgeeks.org/php-directoryiterator-getpathname-function/)

**DirectoryIterator：：getPathname()函数**是 PHP 中的内置函数，用于返回当前 DirectoryIterator 项的路径和文件名。

**语法：**

```
*string* DirectoryIterator::getPathname( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回当前文件的路径和文件名。 目录不包含尾部斜杠。

下面的程序演示了 PHP 中的 DirectoryIterator：：getPathname()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs for each element of directory
foreach($directory as $dir) {

    // Display the path name
    echo $directory->getPathname() . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory element is valid
while ($directory->valid()) {

    // Check for directory element
    if ($directory->isDir()) {

        // Display the path name
        echo $directory->getPathname() . "<br>";
    }

    // Move to the next element
    $directory->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.getpathname.php](https://www.php.net/manual/en/directoryiterator.getpathname.php)