# PHP|SplFileObject fputcsv()函数

> Original: [https://www.geeksforgeeks.org/php-splfileobject-fputcsv-function/](https://www.geeksforgeeks.org/php-splfileobject-fputcsv-function/)

SplFileObject fputcsv()函数是 PHP 中标准 PHP 库(SPL)的内置函数，用于将字段数组写为 CSV 行。

**语法：**

```
string SplFileObject::fputcsv()
```

**参数：**此函数接受四个参数，一个是必选的，三个是可选的。

*   **$field：**指定值的数组。
*   **$delimiter：**指定设置字段分隔符的可选参数。
*   **$enclosion：**可选参数，指定字段封闭。
*   **$ESCAPE：**用于转义字符的可选参数。

**返回值：**此函数返回写入字符串的长度，否则返回 False。

下面的程序演示了 PHP 中的 SplFileObject fputcsv()函数。

**程序：**

```
<?php

// Create an Array
$gfg = array (
    array('gfg', 'geeks', 'gced', 'Article'),
    array('Hello', 'Sudo', 'Placement'),
    array('"Contribute"', '"Interview"'),
    array('"System"', '"IDE"')
);

// Creating Spl Object
$file = new SplFileObject('gfg.csv', 'w');

foreach ($gfg as $arr) {
    $file->fputcsv($arr);
}

echo "Successfully write data in gfg.csv";
?>
```

发帖主题：Re：Колибри0.7.0

```
Successfully write data in gfg.csv
```

运行上述程序时，如果不存在 gfg.csv 文件，则会创建一个 gfg.csv 文件，并将数组内容写入文件中，如下图所示。

**引用：**[http://php.net/manual/en/splfileobject.fputcsv.php](http://php.net/manual/en/splfileobject.fputcsv.php)