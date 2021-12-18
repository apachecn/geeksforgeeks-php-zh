# PHP|CTYPE_CNTRL()函数

> Original: [https://www.geeksforgeeks.org/php-ctype_cntrl-function-2/](https://www.geeksforgeeks.org/php-ctype_cntrl-function-2/)

**CTYPE_CNTRL()**函数是 PHP 中的内置函数，用于检查给定字符串的所有字符是否都是控制字符。 如果字符串的所有字符都是控制字符，则返回 True，否则返回 False。
**控制字符：**不代表可打印字符但用于启动特定操作的字符。 例如，‘\n’是一个控制字符，它不能打印，但执行操作“Next Line”。
**语法：**和

```
ctype_cntrl( $text )
```

**参数：**该函数接受表示输入字符串的单个参数*$text*。
**返回值：**如果字符串的所有字符都是控制字符，则此函数返回 TRUE，否则返回 FALSE。
**示例**：

```
Input  : "\t"
Output : Yes

Input  : "\\\b"
Output : No                 
```

下面的程序说明了 ctype_CNTRL()函数：
**程序：1**和

## PHP

```
<?php
// PHP program to check given string has all
// characters as control character

$string = "\n";

// Checking above given strings
// by used of ctype_cntrl() function
if ( ctype_cntrl($string))
    echo "Yes\n";
else
    // if False then return No
    echo "No\n";
?>
```

**Output:** 

```
Yes
```

**程序：2**

## PHP

```
<?php
// PHP program to illustrate the ctype_cntrl() function

$strings = array("\c", "\f", "\n", "\\","123","GFG");

// Checking above given strings
// by use of ctype_cntrl() function .
foreach ($strings as $test) {

    if ( ctype_cntrl($test))
        echo "Yes\n";
    else
        echo "No\n";
}
?>
```

**Output:** 

```
No
Yes
Yes
No
No
No
```

**参考**：[http://php.net/manual/en/function.ctype-cntrl.php](http://php.net/manual/en/function.ctype-cntrl.php)