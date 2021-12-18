# PHP|str_repeat()函数

> Original: [https://www.geeksforgeeks.org/php-str_repeat-function/](https://www.geeksforgeeks.org/php-str_repeat-function/)

函数的作用是：在 PHP 中内置函数，用于通过将给定字符串重复固定次数来创建新字符串。 它接受一个字符串和一个整数作为参数，并返回一个新字符串，该字符串是通过将作为参数传递的字符串重复传递给此函数的整数定义的次数而生成的。

**语法**：

```
*string* str_repeat ( $string, $no_of_times )

```

**参数**：此函数接受两个参数，并且这两个参数都是必须传递的。

1.  **$string**：该参数表示要重复的字符串
2.  **$no_of_Times**：该参数表示一个数字，表示参数$string 重复的次数。 此参数应大于或等于零。

**返回值**：此函数返回通过重复给定的字符串$STRING 给定次数而组成的新字符串。 如果传递给函数的参数$NO_OF_TIMES 等于 0，则函数返回空字符串。

例如：

```
Input : $str = \'GeeksForGeeks\';
        print_r(str_repeat($str, 2));
Output :GeeksForGeeksGeeksForGeeks

Input : $str = \' Run\';
        print_r(str_repeat($str, 7));
Output : Run Run Run Run Run Run Run

```

以下程序说明了 PHP 中的 str_repeat()函数：
**Program-1**：

```
<?php

// Input string
$str = 'GeeksForGeeks';

// Repeated string
print_r(str_repeat($str, 2));

?>
```

产出：

```
GeeksForGeeksGeeksForGeeks

```

**程序-2**：

```
<?php

// Input string 
$str = ' Run';

// Repeated string
print_r(str_repeat($str, 7));

?>
```

产出：

```
 Run Run Run Run Run Run Run

```

**参考**：
[http://php.net/manual/en/function.str-repeat.php](http://php.net/manual/en/function.str-repeat.php)