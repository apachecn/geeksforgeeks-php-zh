# PHP|ctype_print()函数

> Original: [https://www.geeksforgeeks.org/php-ctype_print-function/](https://www.geeksforgeeks.org/php-ctype_print-function/)

PHP 中用于检查字符串的每个字符是否可见的 ctype_print()函数。 如果字符串的所有字符都可见，则返回**TRUE**，否则，如果有任何**控制字符**，则返回**FALSE**。

**控制字符：**不代表可打印字符但用于启动特定操作的字符。 例如**‘\n’**是一个控制字符，它不能打印，但执行动作**“Next Line”**

**语法：**

```php
ctype_print(string text)

```

**使用的参数：**

*   **$text：**测试的字符串。 这是必选参数。

**返回值：**
如果字符串的所有字符都是可打印的(不包含任何控制字符)，则此函数返回 TRUE。 如果字符串包含任何控制字符，则返回 False。

例如：

```php
Input  : Geeks for geeks article
Output : Geeks for geeks article -->Yes visible

Explanation : The string contains three blank space 
             and the function returns TRUE. 

Input  : \tgfg\n
Output :     gfg
--> No visible

Explanation : '\t' and '\n' are control character .
            Then the function returns False.

```

**程序：1**

```php
<?php
// PHP program to illustrate 
// ctype_print() function 

$string = 'GFG A Computer Science Portal';

// Checking above given strings 
// by used of ctype_print() function .
if (ctype_print($string)) {

    // if true then return Yes
    echo "$string: Yes visible\n";
} else {

    // if False then return No
    echo "$string: Not visible\n";
}
?>
```

**Output:**

```php
GFG A Computer Science Portal: Yes visible

```

**程序：2**驱动 ctype_print()函数的代码，其中输入将是整数，字符串数组中的符号。

```php
<?php
// PHP program to illustrate
// ctype_print() function 

$strings = array(
    "GeeksforGeeks",
    "GFG2018",
    "\nComputerScience",
    "G 4 G",
    "@#$.&*()_+;?~",
    "78 96 . 90"
);

// Checking above array of strings 
// by used of ctype_print() function.
foreach ($strings as $str) {

    if (ctype_print($str)) {

        // if true then return Yes
        echo "$str:   (Yes visible)\n";
    } else {
        // if False then return No
        echo "$str:   (No visible)\n";
    }
}

?>
```

**Output:**

```php
GeeksforGeeks:   (Yes visible)
GFG2018:   (Yes visible)

ComputerScience:   (No visible)
G 4 G:   (Yes visible)
@#$.&*()_+;?~:   (Yes visible)
78 96 . 90:   (Yes visible)

```

参考文献：[http://php.net/manual/en/function.ctype-print.php](http://php.net/manual/en/function.ctype-print.php)