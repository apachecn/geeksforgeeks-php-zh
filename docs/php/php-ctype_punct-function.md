# PHP|ctype_point()函数

> Original: [https://www.geeksforgeeks.org/php-ctype_punct-function/](https://www.geeksforgeeks.org/php-ctype_punct-function/)

Ctype_point()是 PHP 中的一个内置函数，用于检查非空格或字母数字字符的可打印字符。 字符串中的每个字符都是可打印的，但字母数字、数字或空白都不能返回 True，否则将返回 False。

**语法：**

```php
bool ctype_punct ( $text )
```

**参数：**此函数接受单个参数*$text*。 它是指定字符串的必选参数。

**返回值：**如果字符串不包含任何字母数字、数字或空白字符，则返回 True；如果失败，则返回 False。
示例：

```php
Input : GeeksforGeeks
Output : No
Explanation: String (GeeksforGeeks) contains only the alphanumeric characters.

Input : $%^&@
Output : Yes
Explanation: String ($%^&@) contains only the punctuation character.

```

下面的程序演示了 ctype_point()函数。
**程序 1：**

```php
<?php
// PHP program to check the given
// string is not containing any 
// alphanumeric or digit or blank
// character

$string1 = 'GeeksforGeeks';
if ( ctype_punct($string1)) 
        echo "Yes\n";
    else
        echo "No\n";

$string2 = '$%^&@';
if ( ctype_punct($string2)) 
        echo "Yes\n";
    else
        echo "No\n";
?>
```

**Output:**

```php
No
Yes

```

**程序 2：**ctype_point()函数的代码接受包含整数和特殊符号的输入字符串数组。

```php
<?php
// PHP program to check given
// string is not contain any 
// alphanumeric or digit or
// blank character

$strings = array (
    'Geeks',
    'Geeks space',
    '@@##-- /',
    '12345',
    '\n',
    '&%@!()^'
);

// Checking above given strings 
// by used of ctype_punct()
// function .
foreach ($strings as $test) {

    if (ctype_punct($test))
        echo "Yes\n";
    else
        echo "No\n";
}

?>
```

**Output:**

```php
No
No
No
No
No
Yes

```

**引用：**[http://php.net/manual/en/function.ctype-punct.php](http://php.net/manual/en/function.ctype-punct.php)