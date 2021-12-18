# PHP|vprintf()函数

> Original: [https://www.geeksforgeeks.org/php-vprintf-function/](https://www.geeksforgeeks.org/php-vprintf-function/)

PHP 中 vprintf()函数是一个内置函数，用于将数组值显示为格式化字符串。
根据格式将数组值显示为格式化字符串。它的工作方式类似于[printf()](https://www.geeksforgeeks.org/php-format-specifiers/)，但接受参数数组，而不是变量数参数。 成功时返回输出字符串的长度。
**语法：**

```
vprintf (format, array_arguments)
```

**参数：**

1.  **格式：**它是必需的参数，它指定字符串的格式。
    可能的格式值：
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
    *   **%E**-使用大写的科学记数法(例如 1.2E+2)
    *   **%G**-%E 和%f 之间的较短
2.  **ARRAY_ARGUMENTS**此处需要格式化的数组参数。

**程序 1：**本程序将使用 vprintf 函数显示**%b d u x X f F o**格式的用法。

## PHP

```
<?php
$obj = new stdClass();
$obj->val1 = 9;
$obj->val2 = 10;
$obj->val3 = 15;
$obj->val4 = -1;

echo "using %% format: ";

// below is using of vprintf function
// for printing % format
vprintf('%% %% %% %%', $obj);

echo "\nusing %b format: ";

// below is using of vprintf function
// for format %b will print equivalent
// binary number
vprintf('%b %b %b %b', $obj);

echo "\nusing %d format: ";

// below is using of vprintf function
// for  %d format
vprintf('%d %d %d %d', $obj);

echo "\nusing %u format: ";

// below is using of vprintf function
// for  % u (unsigned decimal) format
vprintf('%u %u %u %u', $obj);

echo "\nusing %x format: ";

// below is using of vprintf function
// for  %x  Hexadecimal number (lowercase letters) format
vprintf('%x %x %x %x', $obj);

echo "\nusing %X format: ";

// below is using of vprintf function
// for  %X  Hexadecimal number (uppercase letters) format
vprintf('%X %X %X %X', $obj);

echo "\nusing %f format: ";

// below is using of vprintf function
// for  %f  Floating-point number (local settings aware)
vprintf('%f %f %f %f', $obj);

echo "\nusing %F format: ";

// below is using of vprintf function
// for  %F Floating-point number (not local settings aware)
vprintf('%F %F %F %F', $obj);

echo "\nusing %o format: ";

// below is using of vprintf function
// for  %o octal number
vprintf('%o %o %o %o', $obj);

?>
```

**Output:** 

```
using %% format: % % % %
using %b format: 1001 1010 1111 1111111111111111111111111111111111111111111111111111111111111111
using %d format: 9 10 15 -1
using %u format: 9 10 15 18446744073709551615
using %x format: 9 a f ffffffffffffffff
using %X format: 9 A F FFFFFFFFFFFFFFFF
using %f format: 9.000000 10.000000 15.000000 -1.000000
using %F format: 9.000000 10.000000 15.000000 -1.000000
using %o format: 11 12 17 1777777777777777777777
```

**程序 2：**本程序将使用 vprintf 函数显示**c 和 s**格式的用法。

## PHP

```
<?php
$obj = new stdClass();
$obj->val1 = 65;
$obj->val2 = 66;
$obj->val3 = 97;
$obj->val4 = 98;

echo "using %c format: ";

// below is using of vprintf function
// for printing %c format will be print
// ASCII character
vprintf('%c %c %c %c', $obj);

echo "\nusing %s format: ";

// below is using of vprintf function
// for format %s will print as string
vprintf('%s %s %s %s', $obj);

?>
```

**Output:** 

```
using %c format: A B a b
using %s format: 65 66 97 98
```

**程序 3：**本程序将使用 vprintf 函数显示**例如 E G**格式的用法。

## PHP

```
<?php
$obj = new stdClass();
$obj->val1 = 999999999;
$obj->val2 = 145956566;
$obj->val3 = 111111111;
$obj->val4 = 100000000;

echo "using %e format: ";
// below is using of vprintf function
// for printing %e format will be print
// Scientific notation (lowercase)
vprintf('%e %e %e %e', $obj);

echo"\nusing %g format: ";
// below is using of vprintf function
// for format %g will be print
// Shorter of %e and %f
vprintf('%g %g %g %g', $obj);

echo "\nusing %E format: ";
// below is using of vprintf function
// for format %E will print
// Scientific notation (uppercase)
vprintf('%E %E %E %E', $obj);

echo "\nusing %G format: ";
// below is using of vprintf function
// for format %G will be print
// Shorter of %E and %f
vprintf('%G %G %G %G', $obj);

?>
```

**Output:** 

```
using %e format: 1.000000e+9 1.459566e+8 1.111111e+8 1.000000e+8
using %g format: 1.0e+9 1.45957e+8 1.11111e+8 1.0e+8
using %E format: 1.000000E+9 1.459566E+8 1.111111E+8 1.000000E+8
using %G format: 1.0E+9 1.45957E+8 1.11111E+8 1.0E+8
```

**程序 4：**在本程序中，所有四个变量将使用 vprintf 函数分别打印 10 20 30 40 空格。

## PHP

```
<?php
$obj = new stdClass();
$obj->val1 = 'gfg 1';
$obj->val2 = 'gfg 2';
$obj->val3 = 'gfg 3';
$obj->val4 = 'gfg 4';

// below is using of vprintf function
vprintf('%-10s %-20s %-30s %-40s', $obj);

?>
```

**Output:** 

```
gfg 1      gfg 2                gfg 3                          gfg 4
```