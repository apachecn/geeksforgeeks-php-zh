# PHP|DirectoryIterator Seek()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-seek-function/](https://www.geeksforgeeks.org/php-directoryiterator-seek-function/)

**DirectoryIterator：：Seek()函数**是 PHP 中的一个内置函数，用于将 DirectoryIterator 项查找到给定位置。

**语法：**

```php
*void* DirectoryIterator::seek( *int* $position )
```

**参数：**此函数接受单个参数**$position**，该参数保存从零开始的数字位置以查找元素。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP 中的 DirectoryIterator：：Seek()函数：

**程序 1：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Move to the third element (0 based indexing)
$directory->seek(2);

// Check for validity of element
if($directory->valid()) {

    // Display the filename
    echo $directory->getFilename();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**程序 2：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Move to the third element (0 based indexing)
$directory->seek(2);

// Check for validity of element
if($directory->valid()) {

    // Display the key and filename
    echo $directory->key() . " => " .
    $directory->getFilename();
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.seek.php](https://www.php.net/manual/en/directoryiterator.seek.php)