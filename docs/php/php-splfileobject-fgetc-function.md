# PHP|SplFileObject fgetc()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-fgetc-function/](https://www.geeksforgeeks.org/php-splfileobject-fgetc-function/)

**SplFileObject：：fgetc()**函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于从文件中获取字符。
**语法：**

```
string SplFileObject::fgetc( void )
```

**参数：**此函数不接受任何参数。

**返回值：**返回从文件读取的单个字符，或者在 EOF 上返回 False。

下面的程序演示了 PHP 中的 SplFileObject：：fgetc()函数。

**注意：**程序 1 使用了包含以下数据的 gfg.txt 文件。

```
GeeksforGeeks
```

**程序 1：**用一个空格分隔打印文件的所有字符。

```
<?php

// Create SplFileObject object
$file = new SplFileObject("gfg.txt");

// Print all characters of file 
while (false !== ($gfg = $file->fgetc()))

{
    echo "$gfg";
}
?>
```

发帖主题：Re：Колибри0.7.0

```
G e e k s f o r G e e k s

```

**程序 2：**打印当前文件的所有字符。

```
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

```
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

**引用：**[http://php.net/manual/en/splfileobject.fgetc.php](http://php.net/manual/en/splfileobject.fgetc.php)