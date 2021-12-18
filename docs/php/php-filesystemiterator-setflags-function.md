# PHP|FilesystemIterator setFlags()函数

> Original: [https://www.geeksforgeeks.org/php-filesystemiterator-setflags-function/](https://www.geeksforgeeks.org/php-filesystemiterator-setflags-function/)

**FilesystemIterator：：setFlags()函数**是 PHP 中的内置函数，用于设置处理标志。

**语法：**

```php
*void* FilesystemIterator::setFlags( *int* $flags )
```

**参数：**此函数接受保存要设置的处理标志的单个参数**$flag**。

**返回值：**此函数不返回任何值。

下面的程序演示了 PHP 中的 FilesystemIterator：：setFlags()函数：

**程序 1：**

```php
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(__DIR__, 
    FilesystemIterator::CURRENT_AS_PATHNAME);

// Set the flags
$fileItr->setFlags(FilesystemIterator::KEY_AS_FILENAME);

// Get the flag 
$flag = $fileItr->getFlags(); 

// Display the flag 
var_dump($flag); 

?>
```

**输出：**

```php
int(256)

```

**程序 2：**

```php
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(__DIR__, 
    FilesystemIterator::CURRENT_AS_PATHNAME);

// Set the flag
$fileItr->setFlags(FilesystemIterator::CURRENT_AS_SELF);

// Get the flag 
$flag = $fileItr->getFlags(); 

// Display the flag 
var_dump($flag); 

?>
```

**输出：**

```php
int(16)

```

**引用：**[https://www.php.net/manual/en/filesystemiterator.setflags.php](https://www.php.net/manual/en/filesystemiterator.setflags.php)