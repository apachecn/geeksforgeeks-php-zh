# PHP|DirectoryIterator getType()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-gettype-function/](https://www.geeksforgeeks.org/php-directoryiterator-gettype-function/)

DirectoryIterator：：getType()函数是 PHP 中的内置函数，用于检查当前 DirectoryIterator 项的类型。

**语法：**

```
*string* DirectoryIterator::getType( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回表示文件类型的字符串。 类型可以是文件、链接或目录之一。

下面的程序演示了 PHP 中的 DirectoryIterator：：getType()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check it is directory or not
    if ($directory->isDir()) {
        $file = $directory->current();
        echo $file->getFilename() . " | Type: "
                . $directory->getType() . "<br>";
    }

    // Move to the next element of DirectoryIterator
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

    $file = $directory->current();

    echo $dir->key() . " => " . 
        $file->getFilename() . " | Type: " .
        $dir->getType() . "<br>";
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.gettype.php](https://www.php.net/manual/en/directoryiterator.gettype.php)