# PHP|DirectoryIterator isExecutable()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-isexecutable-function/](https://www.geeksforgeeks.org/php-directoryiterator-isexecutable-function/)

**DirectoryIterator：：isExecutable()函数**是 PHP 中的内置函数，用于检查当前 DirectoryIterator 项是否可执行。

**语法：**

```
*bool* DirectoryIterator::isExecutable( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果条目是可执行的，则此函数返回 TRUE，否则返回 FALSE。

下面的程序说明了 PHP 中的 DirectoryIterator：：isExecutable()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check file is exeutable
    if($directory->isExecutable()) {

        // Display the filename
        echo $directory->getFilename() . "<br>";
    }

    // Move to the next element
    $directory->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs for each element of directory
foreach($directory as $dir) {

    // Check file is exeutable
    if($directory->isExecutable()) {

        // Display the filename
        echo $directory->getFilename() . "<br>";
    }
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.isexecutable.php](https://www.php.net/manual/en/directoryiterator.isexecutable.php)