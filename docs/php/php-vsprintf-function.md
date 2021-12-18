# PHP|vprint intf()函数

> Original: [https://www.geeksforgeeks.org/php-vsprintf-function/](https://www.geeksforgeeks.org/php-vsprintf-function/)

PHP 中的**vprint intf()函数**是一个内置函数，用于将数组值显示为格式化字符串。 数组元素将插入到主字符串中的百分号(%)处。 根据格式将数组值显示为格式化字符串，并接受数组参数代替可变数量的参数。 函数**返回格式化字符串**。 而[vprintf()](https://www.geeksforgeeks.org/php-vprintf-function/)输出格式化字符串
**语法：**

```
 vsprintf (format, arr_arguments)
```

**使用的参数：**此函数接受两个参数，如下所述-

1.  **格式：**有必选参数。 它指定如何将字符串格式化为变量。 可能的格式值如下：
    *   **%%**-返回百分号
    *   **%b**-二进制数
    *   **%d**-有符号十进制数(负、零或正)
    *   **%u**-无符号十进制数(等于或大于零)
    *   **%x**-十六进制数字(小写字母)
    *   **%X**-十六进制数字(大写字母)
    *   **%f**-浮点数(本地设置感知)
    *   **%F**-浮点数(不支持本地设置)
    *   **%o**-八进制数
    *   **%c**-根据 ASCII 值的字符
    *   **%s**-字符串
    *   **%e**-使用小写的科学记数法(例如 1.2e+2)
    *   **%g**-%e 和%f 之间的较短
    *   **%G**-%E 和%f 之间的较短
    *   **%E**-使用大写的科学记数法(例如 1.2E+2)
2.  **ARR_ARGUMENTS：**插入%符号格式字符串的数组参数。

**附加格式：**

*   **-**->左对齐变量值。
*   **[0-9]**->数字的最大字符串长度。
*   **[0-9]**->变量值的最小字符串宽度。
*   **+**->同时用于[+或-](默认为负数)。

**程序 1：**字符串空间指定的程序。

## PHP

```
<?php
$str1 = "Geeks";
$str2 = "Geeksforgeeksarticle";

// print string-1 only
echo vsprintf("%s\n", array(
    $str1
));

// print string-15 space
echo vsprintf("%15s\n", array(
    $str1
));

// print string-1 with space
echo vsprintf("%-25s\n", array(
    $str1
));

// print string with zero
echo vsprintf("%020s\n", array(
    $str1
));

// print string with * symbol
echo vsprintf("%'*10s\n", array(
    $str1
));

// print string-2
echo vsprintf("%s\n", array(
    $str2
));

// print string-2 with decimal point
echo vsprintf("%2.10s\n", array(
    $str2
));

// print string-2 with space
echo vsprintf("%30s\n", array(
    $str2
));

// print string-2 with zero
echo vsprintf("%030s", array(
    $str2
));

?>
```

**Output:** 

```
Geeks
          Geeks
Geeks                    
000000000000000Geeks
*****Geeks
Geeksforgeeksarticle
Geeksforge
          Geeksforgeeksarticle
0000000000Geeksforgeeksarticle
```