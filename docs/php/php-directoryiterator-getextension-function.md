# PHP|DirectoryIterator getExtension()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-getextension-function/](https://www.geeksforgeeks.org/php-directoryiterator-getextension-function/)

**DirectoryIterator：：getExtension()函数**是 PHP 中的内置函数，用于获取文件扩展名。

**语法：**

```
*string* DirectoryIterator::getExtension( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回包含文件扩展名的字符串，如果文件不包含扩展名，则返回空字符串。

下面的程序演示了 PHP 中的 DirectoryIterator：：getExtension()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs for each element of directory
foreach($directory as $dir) {

    // Display the file extension
    echo $dir->getExtension() . "<br>";
}
?> 
```

发帖主题：Re：Колибри0.7.8.0

**注意：**空行表示不包含文件扩展名的文件夹。

**程序 2：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check if element is not directory
    if (!$directory->isDir()) {

        // Display the extension
        echo $directory->getExtension() . "<br>";
    }

    // Move to the next element
    $directory->next();
}
?> 
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.getextension.php](https://www.php.net/manual/en/directoryiterator.getextension.php)