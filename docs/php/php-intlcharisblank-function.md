# PHP|IntlChar：：isBlank()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharisblank-function/](https://www.geeksforgeeks.org/php-intlcharisblank-function/)

**IntlChar：：isBlank()**函数是 PHP 中的一个内置函数，用于确定给定的输入代码数据是空白字符还是水平空格字符，并且可见字符将一行中的单词隔开。

如果输入包含 U+0009(TAB)和除零宽度空格(ZWSP、U+200B)之外的字符“Z”(空格分隔符)，则它将为 True。
当垂直空格控制字符包含以下字符时，Unicode 空白字符(“垂直空格控制”字符除外)为真：U+000A(LF)U+000b(VT)U+000C(FF)U+000D(CR)U+0085(NEL)U+2028(LS)U+2029(PS)。

**语法：**

```
*bool* IntlChar::isblank ( $codepoint )

```

**参数：**此函数接受上述单个参数，如下所述：

*   **$codepoint：**输入参数$codepoint 是整数值或字符，编码为*UTF-8*字符串。 该函数在编译函数后返回一个布尔值。

**返回值：**如果$codepoint 是空格或水平空格字符，则返回 TRUE，否则返回 FALSE。

例如：

```
Input : $codepoint = "G"
Output :bool(false)
// Character becomes False

Input : $codepoint = " "
Output : bool(true)
// Space becomes TRUE

Input : $codepoint = "Geeks"
Output : NULL
// String  becomes NULL

```

下面的程序演示了 PHP 中的**IntlChar：：isBlank()**函数：

**程序 1：**

```
<?php
// PHP code to illustrate the 
// IntlChar::isblank() function.

// input alphabe character
var_dump(IntlChar::isblank("X"));

// Plus operator 
var_dump(IntlChar::isblank("+"));

// Space character
var_dump(IntlChar::isblank(" "));

// % sign operator
var_dump(IntlChar::isblank("%"));

// tab character
var_dump(IntlChar::isblank("\t"));

// new line character
var_dump(IntlChar::isblank("\n"));
?>
```

产出：

```
bool(false)
bool(false)
bool(true)
bool(false)
bool(true)
bool(false)

```

**程序 2：**

```
<?php
// PHP code to illustrate the 
// IntlChar::isblank() function.

// input alphabe character
var_dump(IntlChar::isblank('X'));

// Plus operator 
var_dump(IntlChar::isblank('+'));

// Space character
var_dump(IntlChar::isblank(' '));

// % sign operator
var_dump(IntlChar::isblank('%'));

// tab character
var_dump(IntlChar::isblank('\t'));

// new line character
var_dump(IntlChar::isblank('\n'));
?>
```

产出：

```
bool(false)
bool(false)
bool(true)
bool(false)
NULL
NULL

```

**程序 3：**如果函数输入是字符串或数字，则打印 NULL。

```
<?php
// PHP code to illustrate the 
// IntlChar::isblank() function.

// In case of input string
var_dump(IntlChar::isblank("GeeksforGeeks is Computer Portal"));

// In case of number input
var_dump(IntlChar::isblank("2018"));
?>
```

产出：

```
NULL
NULL

```

**引用：**[http://php.net/manual/en/intlchar.isblank.php](http://php.net/manual/en/intlchar.isblank.php)