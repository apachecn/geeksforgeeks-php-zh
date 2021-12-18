# PHP|SplFileObject 倒带()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-rewind-function/](https://www.geeksforgeeks.org/php-splfileobject-rewind-function/)

**SplFileObject：：Rewind()**函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于将文件倒回到第一行。

**语法：**

```
*void* SplFileObject::rewind( $line_num)
```

**参数：**此函数不接受任何参数。

**返回值：**此函数不返回任何值。

下面的程序说明了 PHP：
**Program-1：**中的 SplFileObject：：Rewind()函数

## PHP

```
<?php

// PHP program to illustrate
// SplFileObject::rewind function

$file = new SplFileObject(__FILE__);

$file->rewind();

echo $file->current();
?>
```

发帖主题：Re：Колибри0.7.0

```
<?php
```

**程序-2：**

## PHP

```
<?php

// PHP program to use array to check
// multiple files
$GFG = array(
    "/home/rajvir/Desktop/GeeksforGeeks/dummy.php",
    "gfg.txt",
    "mime.php"
    );

foreach ($GFG as &$file_name) {

    $file = new SplFileObject($file_name);
    $file->rewind();
    echo $file->current();
    }
?>
```

**Output:** 

```
GeeksforGeeks
gfg
contribute
```

**引用：**[http://php.net/manual/en/splfileobject.rewind.php](http://php.net/manual/en/splfileobject.rewind.php)