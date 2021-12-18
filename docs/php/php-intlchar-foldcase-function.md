# PHP|IntlChar foldCase()函数

> Original: [https://www.geeksforgeeks.org/php-intlchar-foldcase-function/](https://www.geeksforgeeks.org/php-intlchar-foldcase-function/)

**IntlChar：：foldCase()函数**是 PHP 中的一个内置函数，用于在代码点上执行案例折叠。 大小写折叠意味着给定的字符被映射到其等效的小写字符。
**语法：**和

```php
*mixed* IntlChar::foldCase( $codepoint, $options = 
IntlChar::FOLD_CASE_DEFAULT )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$codepoint：**此参数是一个字符或整数值，编码为 UTF-8 字符串。
*   **$OPTIONS：**默认情况下，此参数保存字符常量*IntlChar：：Fold_Case_Default*或*IntlChar：：Fold_Case_Exclude_Special_I*。

**返回值：**此函数返回码点的*SIMPLE_CASE_Folding*。 如果码点没有大小写折叠等效项，则返回码点本身。
下面的程序说明了 PHP：
**程序：**和
中的**IntlChar：：foldCase()**函数

## PHP

```php
<?php
// PHP program to illustrate the IntlChar::foldCase() function

var_dump(IntlChar::foldCase('AA', IntlChar::FOLD_CASE_EXCLUDE_SPECIAL_I));

var_dump(IntlChar::foldCase('@', IntlChar::FOLD_CASE_EXCLUDE_SPECIAL_I));

var_dump(IntlChar::foldCase('&', IntlChar::FOLD_CASE_EXCLUDE_SPECIAL_I));

var_dump(IntlChar::foldCase('C', IntlChar::FOLD_CASE_DEFAULT));

var_dump(IntlChar::foldCase('Lt', IntlChar::FOLD_CASE_DEFAULT));

var_dump(IntlChar::foldCase('/', IntlChar::FOLD_CASE_DEFAULT));

var_dump(IntlChar::foldCase('g', IntlChar::FOLD_CASE_DEFAULT));

var_dump(IntlChar::foldCase('1', IntlChar::FOLD_CASE_DEFAULT));

?>
```

**Output:** 

```php
NULL
string(1) "@"
string(1) "&"
string(1) "c"
NULL
string(1) "/"
string(1) "g"
string(1) "1"
```

**引用：**[https://www.php.net/manual/en/intlchar.foldcase.php](https://www.php.net/manual/en/intlchar.foldcase.php)