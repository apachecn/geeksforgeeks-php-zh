# PHP|CTYPE_UPPER()函数

> Original: [https://www.geeksforgeeks.org/php-ctype_upper-function/](https://www.geeksforgeeks.org/php-ctype_upper-function/)

PHP 中用于检查给定字符串的每个字符是否为大写的 ctypeupper()函数。 如果字符串为大写，则返回 TRUE，否则返回 FALSE。

**语法：**

```
ctype_upper (string text)

```

**使用的参数：-**

*   **$text：**测试的字符串。

**返回值：**
函数如果文本的每个字符都是大写，则返回 True；如果文本不是大写，则返回 False。

例如：

```
Input  : GEEKSFORGEEKS
Output : Yes
Explanation: All characters of  "GEEKSFORGEEKS" 
             in UPPERCASE.

Input  : GFG2018
Output : No
Explanation : In text "GFG2018",  '2', '0', '1', '8'
              are not in UPPERCASE.

Input : GFG INDIA
Output : No
Explanation : In String "GFG INDIA" a special character [space] 
              between GFG and INDIA. so answer will be No.

```

```
Note: Except string, if we input anything then it will return FALSE.
```

下面的程序演示了 PHP 中的 ctype_upper()函数：

**程序：1**

```
<?php
// PHP program to check given string is 
// all characters -Uppercase characters

$string1 = 'GEEKSFORGEEKS';

   if (ctype_upper($string1)) {

        // if true then return Yes
        echo "Yes\n";
    } else {

        // if False then return No
        echo "No\n";
    }
?>
```

**Output:**

```
Yes

```

**程序：2**将字符串数组作为文本传递，并打印单个值的结果。

```
<?php

// PHP program to check given string is 
// all characters -Uppercase characters

$strings = array('GEEKSFORGEEKS', 'First', 
                'PROGRAMAT2018', 'ARTICLE');

// Checking above given four strings 
//by used of ctype_upper() function .

foreach ($strings as $test) {

    if (ctype_upper($test)) {
        // if true then return Yes
        echo "Yes\n";
    } else {
        // if False then return No
        echo "No\n";
    }
}

?>
```

**Output:**

```
Yes
No
No
Yes

```

**程序：3**驱动代码**CTYPE_UPPER()**函数，其中输入将是空格，特殊符号，返回 FALSE。

```

<?php
// PHP program to check given string is 
// all characters -Uppercase characters

$strings = array('GEEK @ . com');

// Checking above given four strings 
//by used of ctype_upper() function .

foreach ($strings as $test) {

    if (ctype_upper($test)) {
        // if true then return Yes
        echo "Yes\n";
    } else {
        // if False then return No
        echo "No\n";
    }
}

?>
```

**Output:**

```
No

```

参考文献：[http://php.net/manual/en/function.ctype-upper.php](http://php.net/manual/en/function.ctype-upper.php)