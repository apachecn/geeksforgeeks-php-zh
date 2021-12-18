# PHP|ctype_alpha()(检查字母值)

> Original: [https://www.geeksforgeeks.org/php-ctype_alpha-checks-for-alphabetic-value/](https://www.geeksforgeeks.org/php-ctype_alpha-checks-for-alphabetic-value/)

PHP 中的**ctype_alpha()**函数，用于检查给定字符串的所有字符是否为字母。 如果所有字符都是字母，则返回 True，否则返回 False。

**语法：**

```php
ctype_alpha($text)
```

**使用的参数：**

*   **$text：-**它是指定字符串的强制参数。

**返回值：**
如果字符串的所有字符都是字母，则返回 True；如果失败，则返回 False。

例如：

```php
Input  : GeeksforGeeks
Output : Yes

Explanation : String (GeeksforGeeks) contains only alphabets

Input  : GFG-GCET-2018
Output : No

Explanation : String contains Integer and special characters.

Note: Except string ,if you input anything then it will return FALSE.    

```

下面的程序演示了 ctype_alpha()函数。

**程序：1**

```php
<?php
// PHP program to check given string is 
// all characters -alphabetic

$string = 'GeeksforGeeks';

    if ( ctype_alpha($string)) 

        echo "Yes\n";
    else 
        echo "No\n";
?>
```

**Output:**

```php
Yes

```

**程序：2**驱动代码**ctype_alpha()**函数，其中输入包含整数和特殊字符的字符串数组。

```php
<?php
// PHP program to check given string is 
// all characters are alphabetic

$strings = array(
    'GFG',
    'GFG space',
    '@@##-- /',
    '789543',
    '\n'
);

// Checking above given strings 
// by used of ctype_alpha() function .
foreach ($strings as $test) {

    if (ctype_alpha($test))
        echo "Yes\n";
    else
        echo "No\n";

}

?>
```

**Output:**

```php
Yes
No
No
No
No

```

**相关文章：**[php|ctype_alnum()(检查字母数字)](https://www.geeksforgeeks.org/php-ctype_alnum-check-for-alphanumeric/)
**参考：**
[http://php.net/manual/en/function.ctype-alpha.php](http://php.net/manual/en/function.ctype-alpha.php)