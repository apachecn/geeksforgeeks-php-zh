# PHP|preg_filter()函数

> Original: [https://www.geeksforgeeks.org/php-preg_filter-function/](https://www.geeksforgeeks.org/php-preg_filter-function/)

Preg_filter()函数是 PHP 中的一个内置函数，用于执行正则表达式搜索和替换文本。

**语法：**

```php
preg_filter( $pattern, $replacement, $subject, $limit, $count )
```

**参数：**此函数接受上述五个参数，如下所述。

*   **$Pattern：**此参数包含要搜索的字符串元素，它可以是字符串或字符串数组。
*   **$Replace：**必选参数，指定要替换的字符串或包含字符串的数组。
*   **$SUBJECT：**要搜索和替换的字符串或包含字符串的数组。
*   **$Limit：**此参数指定每个模式可能的最大替换数。
*   **$count：**可选参数，用于填充完成的替换次数。

**返回值：**如果 Subject 参数是数组，则此函数返回数组，否则返回字符串。

下面的程序说明了 PHP：
**程序 1：**中的 preg_filter()函数

```php
<?php

// PHP program to illustrate 
// preg_filter function
$string = 'November 01, 2018';
$pattern = '/(\w+) (\d+), (\d+)/i';
$replacement = '${1} 02, $3';

// print result 
echo preg_filter($pattern, $replacement, $string);
?>
```

**Output:**

```php
November 02, 2018

```

**程序 2：**

```php
<?php

// PHP program to illustrate preg_filter function
$subject = array('1', 'GFG', '2', 
        'Geeks', '3', 'GCET', 'Contribute', '4'); 
$pattern = array('/\d/', '/[a-z]/', '/[1a]/'); 
$replace = array('X:$0', 'Y:$0', 'Z:$0'); 

echo "Returned Array by preg_filter";
print_r(preg_filter($pattern, $replace, $subject)); 
?>
```

**Output:**

```php
Returned Array by preg_filterArray
(
    [0] => X:Z:1
    [2] => X:2
    [3] => GY:eY:eY:kY:s
    [4] => X:3
    [6] => CY:oY:nY:tY:rY:iY:bY:uY:tY:e
    [7] => X:4
)

```

**引用：**[http://php.net/manual/en/function.preg-filter.php](http://php.net/manual/en/function.preg-filter.php)