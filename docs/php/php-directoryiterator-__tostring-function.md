# PHP|DirectoryIterator__toString()函数

> Original: [https://www.geeksforgeeks.org/php-directoryiterator-__tostring-function/](https://www.geeksforgeeks.org/php-directoryiterator-__tostring-function/)

**DirectoryIterator：：__toString()函数**是 PHP 中的内置函数，用于返回当前 DirectoryIterator 项的文件名。

**语法：**

```php
*string* DirectoryIterator::__toString( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回当前 DirectoryIterator 项的文件名。

下面的程序演示了 PHP 中的 DirectoryIterator：：__toString()函数：

**程序 1：**

```php
<?php

// Create a directory Iterator
$directory = new DirectoryIterator(dirname(__FILE__));

// Loop runs while directory element is valid
while ($directory->valid()) {

    // Display the filename in string format
    echo $directory->__toString() . "<br>";

    // Move to the next element
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

    // Display the key and filename
    echo $directory->key() . " => " .
    $directory->__toString() . "<br>";
}

?>
```

发帖主题：Re：Колибри0.7.8.0

**注意：**此函数的输出取决于服务器文件夹的内容。

**引用：**[https://www.php.net/manual/en/directoryiterator.tostring.php](https://www.php.net/manual/en/directoryiterator.tostring.php)