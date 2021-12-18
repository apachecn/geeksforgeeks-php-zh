# PHP|IntlChar：：totitle()函数

> Original: [https://www.geeksforgeeks.org/php-intlchartotitle-function/](https://www.geeksforgeeks.org/php-intlchartotitle-function/)

**IntlChar：：totitle()**函数是 PHP 中的一个内置函数，用于检查输入码位是否为 Unicode 字符标题大小写。
**语法：**和

```php
*mixed* IntlChar::totitle( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 *$codepoint*参数是一个字符或整数值，编码为 UTF-8 字符串。
**返回值：**返回代码点的 Simple_Titlecase_Mapping(如果有)；否则返回代码点本身。 返回类型将是整数，除非代码点作为 UTF-8 字符串传递，在这种情况下将返回字符串。
以下程序说明 PHP：
**程序 1：**和
中的**IntlChar：：toTitle()**函数

## PHP

```php
<?php
// PHP function to illustrate the
// use of IntlChar::totitle()

// Input Capital letter  codepoint
var_dump(IntlChar::totitle("G"));

// Input Capital letter  codepoint
var_dump(IntlChar::totitle("g"));

// Input Capital letter  codepoint
var_dump(IntlChar::totitle("a"));

// Input int char an identifier
// of codepoint value
var_dump(IntlChar::totitle("\u{00A0}"));

// Input symbolic space codepoint value
var_dump(IntlChar::totitle(" "));

// Input symbolic codepoint value
var_dump(IntlChar::totitle(" ^ "));

// Input int codepoint value
var_dump(IntlChar::totitle("9"));

// Input control character codepoint value
var_dump(IntlChar::totitle("\n"));

// Input character value
// return its ASCII value
var_dump(IntlChar::totitle(ord("D")));
var_dump(IntlChar::totitle(ord("d")));

// Input  ASCII value 0054 is "T"
var_dump(IntlChar::totitle(ord("0054")));
var_dump(IntlChar::totitle(ord("@")));

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
string(1) "G" 
string(1) "G" 
string(1) "A" 
string(2) " " 
string(1) " " 
NULL 
string(1) "9" 
string(1) " " 
int(68) 
int(68) 
int(48) 
int(64)
```

**程序 2：**和

## PHP

```php
<?php
// PHP function to illustrate the
// use of IntlChar::totitle()

// Declare an array with
// different codepoint value
$arr = array("X",
            "x",
            "*",
            "8",
            "0",
            " ",              
        );

// For loop condition to check
// each character through function
foreach ($arr as $val) {

    // Check each element as code point data
    var_dump(IntlChar::totitle($val));
}
?>
```

发帖主题：Re：Колибри0.7.8.0

```php
string(1) "X"
string(1) "X"
string(1) "*"
string(1) "8"
string(1) "0"
string(1) " "
```

**相关文章：**和

*   [IntlChar：：isspace()函数](https://www.geeksforgeeks.org/php-intlcharisspace-function/)
*   [IntlChar：：isIDIgnorable()函数](https://www.geeksforgeeks.org/php-intlcharisidignorable-function/)
*   [IntlChar：：isIDStart()函数](https://www.geeksforgeeks.org/php-intlcharisidstart-function/)
*   [IntlChar：：isIDPart()函数](https://www.geeksforgeeks.org/php-intlcharisidpart-function/)

**引用：**[http://php.net/manual/en/intlchar.totitle.php](http://php.net/manual/en/intlchar.totitle.php)