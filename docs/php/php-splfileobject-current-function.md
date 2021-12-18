# PHP|SplFileObject Current()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-current-function/](https://www.geeksforgeeks.org/php-splfileobject-current-function/)

**SplFileObject：：Current()**函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于获取当前文件行。
**语法：**

```php
string SplFileObject::current( void )
```

**参数：**此函数不接受任何参数。

**返回值：**返回文件当前行。

下面的程序演示了 PHP 中的 SplFileObject：：Current()函数。

**注意：**程序 1 使用了包含以下数据的 gfg.txt 文件。

```php
GeeksforGeeks
A Computer Science 
Portal for Geeks
```

**Program 1:** Print All lines of file one by one.

```php
<?php

// Creating SplFile Object
$file = new SplFileObject("gfg.txt");

foreach ($file as $gfg => $line) {
   echo $file->key() + 1 ." Line".  
        ':> ' . $file->current();
}
?>
```

发帖主题：Re：Колибри0.7.0

```php
1 Line:  GeeksforGeeks
2 Line:  A Computer Science 
3 Line:  Portal for Geeks

```

**程序 2：**打印当前文件的所有行。

```php
<?php

// Create SplFileObject object
$file = new SplFileObject(__FILE__);

// Print all characters of file 
while (false !== ($gfg = $file->fgetc()))

{
    echo "$gfg";
}
?>
```

**Output:**

```php

1 Line:<?php
2 Line: 
3 Line: // Creating SplFile Object
4 Line: $file = new SplFileObject(__FILE__);
5 Line: 
6 Line: foreach ($file as $k => $line) {
7 Line:    echo $file->key() + 1 ." Line".  
8 Line:         ': ' . $file->current();
9 Line: }
10 Line: ?>

```

**引用：**[http://php.net/manual/en/splfileobject.current.php](http://php.net/manual/en/splfileobject.current.php)