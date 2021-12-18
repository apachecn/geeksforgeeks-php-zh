# 如何用 PHP 统计一个目录中的文件？

> 原文:[https://www . geeksforgeeks . org/如何使用-php 计算目录中的文件数/](https://www.geeksforgeeks.org/how-to-count-files-in-a-directory-using-php/)

PHP 包含许多函数，如 count()、iterator_count()、glob()、openddir()、readdir()、scandir()和 FilesystemIterator()来计算目录中文件的数量。

**[count()函数](https://www.geeksforgeeks.org/php-count-function/):**count()函数是一个数组函数，用于对数组中的所有元素或对象中的某些东西进行计数。此函数使用 COUNT _ RECURSIVE 作为递归计数数组的模式，这对于计数多维数组的所有元素非常有用。

**语法:**

```php
*int* count( mixed $array_or_countable, int $mode = COUNT_NORMAL )
```

**glob()函数:**glob()函数是一个 Filesystem 函数，根据 libc glob()函数使用的规则搜索所有可能的路径名匹配模式。

**语法:**

```php
glob( string $pattern, int $flags = 0 )
```

**程序 1:** 该程序使用 glob()和 count()函数对目录内的所有文件进行计数。

```php
<?php

// Set the current working directory
$directory = getcwd()."/";

// Initialize filecount variavle
$filecount = 0;

$files2 = glob( $directory ."*" );

if( $files2 ) {
    $filecount = count($files2);
}

echo $filecount . "files ";

?>
```

**输出:**

```php
20 files
```

**[openddir()函数](https://www.geeksforgeeks.org/php-opendir-function/):**open ddir()函数用于打开一个目录句柄。要打开的目录的路径作为参数发送给 opendir()函数，成功时返回目录句柄资源，失败时返回 FALSE。

**语法:**

```php
opendir( string $path, resource $context )
```

**[readdir()函数:](https://www.geeksforgeeks.org/php-readdir-function/)**readdir()函数是一个目录函数，它从目录句柄中读取条目，这些条目按照文件系统存储的顺序返回。

**语法:**

```php
readdir( resource $dir_handle )
```

**程序 2:** 该程序使用 openddir()和 readdir()函数对目录内的所有文件进行计数。

```php
<?php

// Set the current working directory
$dir = getcwd();

// Initialize the counter variable to 0
$i = 0; 

if( $handle = opendir($dir) ) {

    while( ($file = readdir($handle)) !== false ) {
        if( !in_array($file, array('.', '..')) && !is_dir($dir.$file)) 
            $i++;
    }
}

// Display result
echo "$i files";

?>
```

**输出:**

```php
20 files
```

**[scandir()函数:](https://www.geeksforgeeks.org/php-scandir-function/)**scandir()函数用于返回指定目录的文件和目录的数组。函数的作用是:列出指定路径中的文件和目录。

**语法:**

```php
scandir( string $directory, int $sorting_order = SCANDIR_SORT_ASCENDING, resource $context )
```

**程序 3:** 该程序使用 scandir()和 count()函数对目录内的所有文件进行计数。

```php
<?php

// Set the current working directory
$directory = getcwd()."/";

// Returns array of files
$files1 = scandir($directory);

// Count number of files and store them to variable
$num_files = count($files1) - 2;

echo $num_files . " files";

?>
```

**输出:**

```php
20 files
```

**文件系统生成器()函数:**文件系统生成器::__construct()函数用于根据路径创建新的文件系统迭代器。

**语法:**

```php
FilesystemIterator::__construct( string $path, 
      int $flags = FilesystemIterator::KEY_AS_PATHNAME 
      | FilesystemIterator::CURRENT_AS_FILEINFO 
      | FilesystemIterator::SKIP_DOTS )

```

**迭代器 _count()函数:**迭代器 _count()函数是 SPL 用来计数迭代器元素的。

**语法:**

```php
int iterator_count( $iterator )
```

**程序 4:** 该程序使用 FilesystemIterator()和 iterator_count()函数对目录内的所有文件进行计数。

```php
<?php

$fi = new FilesystemIterator(__DIR__, FilesystemIterator::SKIP_DOTS);

printf("%d files", iterator_count($fi));

?>
```

**输出:**

```php
20 files
```