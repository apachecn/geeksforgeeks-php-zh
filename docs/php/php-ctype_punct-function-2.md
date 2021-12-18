# PHP|ctype_point()函数

> Original: [https://www.geeksforgeeks.org/php-ctype_punct-function-2/](https://www.geeksforgeeks.org/php-ctype_punct-function-2/)

PHP 中的 ctype_part()函数用于检查给定字符串的所有字符是否都是标点符号。 如果所有字符都是标点符号，则此函数返回 TRUE，否则返回 FALSE。

**注**：标点符号为：句点、逗号、问号、连字符、破折号、圆括号、撇号、省略号、引号、冒号、分号、感叹号。

**语法：**

```php
ctype_punct( $text )
```

**参数：**此函数接受单个参数*文本*。 它是指定输入字符串的必选参数。

**返回值：**如果$text 中的每个字符都是标点符号，则函数返回 TRUE，否则返回 FALSE。

**示例**：

```php
Input  : @#$.&*()_+;><?~
Output : Yes

Input  : GeeksforGeeks@2018
Output : No

Note: The string should not contain a letter, blank-space  or digit.  

```

下面的程序说明了 ctype_point()函数：
**程序：1**

```php
<?php
// PHP program to check given string is 
// punctuation character or not

$string = 'GeeksforGeeks';

    if ( ctype_punct($string)) 
        echo "Yes \n";
     else 
        echo "No \n";

?>
```

**Output:**

```php
No

```

**程序：2**

```php
<?php
// PHP program to check given string is 
// punctuation character or not
$strings = array(
    "Reg no CE:20",
    '()()()()',
    'GFG',
    '@@@@##$%%^^',
    '\n'
);

// Checking above given strings 
//by used of ctype_punct() function .
foreach ($strings as $test) {
    if (ctype_punct($test))
        echo "Yes \n";
    else
        echo "No \n";
}

?>
```

**Output:**

```php
No 
Yes 
No 
Yes 
No

```

**参考**：[http://php.net/manual/en/function.ctype-punct.php](http://php.net/manual/en/function.ctype-punct.php)