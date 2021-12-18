# PHP|FilesystemIterator getFlags()函数

> Original: [https://www.geeksforgeeks.org/php-filesystemiterator-getflags-function/](https://www.geeksforgeeks.org/php-filesystemiterator-getflags-function/)

**FilesystemIterator：：getFlags()函数**是 PHP 中的内置函数，用于获取处理标志。

**语法：**

```
*int* FilesystemIterator::getFlags( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回表示标志集的整数值。

下面的程序演示了 PHP 中的 FilesystemIterator：：getFlags()函数：

**程序 1：**

```
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(__DIR__, 
    FilesystemIterator::CURRENT_AS_PATHNAME);

// Store the flag 
$flag = $fileItr->getFlags(); 

// Display the flag 
var_dump($flag); 

?>
```

**输出：**

```
int(4128)

```

**程序 2：**

```
<?php

// Create new file system iterator
$fileItr = new FilesystemIterator(__DIR__, 
    FilesystemIterator::CURRENT_AS_PATHNAME);

// Set the flag
$fileItr->setFlags(FilesystemIterator::KEY_AS_FILENAME);

// Get the flag 
$flag = $fileItr->getFlags(); 

// Display the flag 
var_dump($flag); 

?>
```

**输出：**

```
int(256)

```

**引用：**[https://www.php.net/manual/en/filesystemiterator.getflags.php](https://www.php.net/manual/en/filesystemiterator.getflags.php)