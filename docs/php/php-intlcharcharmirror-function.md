# PHP|IntlChar：：charMirror()函数

> Original: [https://www.geeksforgeeks.org/php-intlcharcharmirror-function/](https://www.geeksforgeeks.org/php-intlcharcharmirror-function/)

**IntlChar：：charMirror()**函数是 PHP 中的一个内置函数，用于从给定的输入码位字符中查找“镜像”字符，该字符映射指定的字符。

**语法：**

```
*mixed* IntlChar::charMirror( $codepoint )
```

**参数：**此函数接受单个参数*$codepoint*，该参数是必需的。 输入参数是字符或整数值，编码为*UTF-8*字符串。

**返回值：**此函数返回可用作镜像替代的另一个 Unicode 代码点，或者如果没有这样的映射或代码点没有 BIDI_MIRRORED 属性，则返回代码点本身。 该函数返回一个整数，除非在*UTF-8*字符串中传递了代码点，否则将返回一个字符串。

下面的程序演示了 PHP 中的**IntlChar：：charMirror()**函数。
**程序 1：**

```
<?php
// PHP code to illustrate
// IntlChar::charMirror ()function

// Input Alphabet codepoint character
var_dump(IntlChar::charMirror("A"));
var_dump(IntlChar::charMirror("B"));

// Input codepoint is Symbloic 
var_dump(IntlChar::charMirror("&"));
var_dump(IntlChar::charMirror("{"));
var_dump(IntlChar::charMirror("^"));
var_dump(IntlChar::charMirror("]"));

// Input codepoint is integer 
var_dump(IntlChar::charMirror("2"));
var_dump(IntlChar::charMirror("10"));

?>
```

发帖主题：Re：Колибри0.7.0

```
string(1) "A" 
string(1) "B" 
string(1) "&" 
string(1) "}" 
string(1) "^" 
string(1) "[" 
string(1) "2" 
NULL

```

**程序 2：**

```
<?php
// PHP code to illustrate
// IntlChar::charMirror() function

// Declare an array $arr
$arr = array("G", "Geek", "801", "7", "F", " \\", "/ ", "\t");

// Loop run for every array element
foreach ($arr as $val){

    // Check each element as code point data
    var_dump(IntlChar::charMirror($val));
}
?>
```

发帖主题：Re：Колибри0.7.0

```
string(1) "G" 
NULL 
NULL 
string(1) "7" 
string(1) "F" 
NULL 
NULL 
string(1) "    " 

```

**相关文章：**

*   [IntlChar：：charDigitValue()函数](https://www.geeksforgeeks.org/php-intlcharchardigitvalue-function/)
*   [IntlChar：：isBlank()函数](https://www.geeksforgeeks.org/php-intlcharisblank-function/)
*   [IntlChar：：iscntrl()函数](https://www.geeksforgeeks.org/php-intlchariscntrl-function/)

**引用：**[http://php.net/manual/en/intlchar.charmirror.php](http://php.net/manual/en/intlchar.charmirror.php)