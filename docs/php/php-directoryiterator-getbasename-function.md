# PHP|DirectoryIterator getBasename()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-getbasename-function/](https://www.geeksforgeeks.org/php-directoryiterator-getbasename-function/)

**DirectoryIterator：：getBasename()函数**是 PHP 中的内置函数，用于获取当前 DirectoryIterator 项的基本名称。

**语法：**

```
*string* DirectoryIterator::getBasename( *string* $suffix )
```

**参数：**此函数接受单个参数$SUBFERFIX，该参数保存以后缀结尾的基本名称。

**返回值：**此函数返回当前 DirectoryIterator 项的基本名称。

下面的程序演示了 PHP 中的 DirectoryIterator：：getBasename()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Display the base name
    echo $directory->getBasename() . "<br>";

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

    // Display the key and basename
    echo $dir->key() . " => " . 
        $dir->getBasename() . "<br>";
}
?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.getbasename.php](https://www.php.net/manual/en/directoryiterator.getbasename.php)