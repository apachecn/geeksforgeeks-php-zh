# 如何将字符串放入数组，在 PHP 中按新行拆分？

> 原文:[https://www . geeksforgeeks . org/如何将字符串放入数组中-由 php 中的新行拆分/](https://www.geeksforgeeks.org/how-to-put-string-in-array-split-by-new-line-in-php/)

给定一个由几个新行字符连接的字符串。任务是将字符串拆分并存储到数组中，这样字符串就会被换行符拆分。

**例:**

```
 Input : string is 'Ankit \n Ram \n Shyam'
 Output : Array
(
    [0] => Ankit
    [1] => Ram
    [2] => Shyam
)

```

**[使用 explot()函数:](https://www.geeksforgeeks.org/php-explode-function/)**explot()函数根据字符串分隔符拆分字符串，即在分隔符出现的地方拆分字符串。此函数返回一个数组，该数组包含通过拆分原始字符串形成的字符串。此函数接受要分隔的分隔符和字符串，以及要分隔的字符串的可选参数长度。

**例:**

```
<?php

// PHP program to separate string
// using explode function

// String which to be converted
$str = "Ankit Mishra\nRam Singh\nShyam Pandey";

// Function to convert string to array
$arr = explode("\n", $str);

// Print the information of array
print_r($arr);
?>
```

**输出:**

```
Array
(
    [0] => Ankit Mishra
    [1] => Ram Singh
    [2] => Shyam Pandey
)

```