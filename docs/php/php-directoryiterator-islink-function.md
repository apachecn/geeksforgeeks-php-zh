# PHP|DirectoryIterator isLink()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-islink-function/](https://www.geeksforgeeks.org/php-directoryiterator-islink-function/)

**DirectoryIterator：：isLink()函数**是 PHP 中的内置函数，用于检查当前 DirectoryIterator 项是否为符号链接。

**语法：**

```
*bool* DirectoryIterator::isLink( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**如果项目是符号链接，则此函数返回 TRUE，否则返回 FALSE。

以下程序说明了 PHP 中的 DirectoryIterator：：isLink()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs for each element of directory
foreach($directory as $dir) {

    // Use isLink() function to store the result
    $link = $dir->isLink();

    // Display result
    var_dump($link);
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

    // Use isLink() function to store the result
    $link = $directory->isLink();

    // Display result
    var_dump($link);

    $directory->next();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.islink.php](https://www.php.net/manual/en/directoryiterator.islink.php)