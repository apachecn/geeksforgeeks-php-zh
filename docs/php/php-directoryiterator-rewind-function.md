# PHP|DirectoryIterator Rewind()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-rewind-function/](https://www.geeksforgeeks.org/php-directoryiterator-rewind-function/)

**DirectoryIterator：：Rewind()函数**是 PHP 中的一个内置函数，用于将 DirectoryIterator 倒回到开始位置。

**语法：**

```
*void* DirectoryIterator::rewind( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 DirectoryIterator：：Rewind()函数：

**程序 1：**

```
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory is valid
while ($directory->valid()) {

    // Check the element is directory
    if($directory->isDir()) {

        // Display the key and file name
        echo $directory->key() . " => " . 
        $directory->getFilename() . "<br>";
    }

    // Move to the next element
    $directory->next();
}

// Use rewind() function to move to
// the start position
$directory->rewind();

// Display the key and file name
echo $directory->key() . " => " . 
        $directory->getFilename();

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

    // Display key and file name
    echo $dir->key() . " => " . 
    $dir->getFilename() . "<br>";
}

// Use rewind() function to move to
// the start position
$directory->rewind();

// Display key and file name
echo $directory->key() . " => " . 
        $directory->getFilename();

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.rewind.php](https://www.php.net/manual/en/directoryiterator.rewind.php)