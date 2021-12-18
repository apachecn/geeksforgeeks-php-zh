# PHP|preg_Match()函数

> Original: [https://www.geeksforgeeks.org/php-preg_match-function/](https://www.geeksforgeeks.org/php-preg_match-function/)

此函数在字符串中搜索模式，如果模式存在，则返回 TRUE，否则返回 FALSE。 搜索通常从主题字符串的开头开始。 可选参数 Offset 用于指定开始搜索的位置。

**语法：**

```php
int preg_match( $pattern, $input, $matches, $flags, $offset )
```

**参数：**此函数接受五个参数，如上所述，如下所述：

*   **pattern:** this parameter saves the pattern to be searched as a string.
*   **input:** this parameter saves the input string.
*   **match:** if there is a match, the search results are included. $matches [0] will contain text that matches the full pattern, $matches [1] will contain text that matches the first captured parenthesized subpattern, and so on.
*   **flag:** flag can be the following:
    *   **PREG_OFFSET_CAPTURE:** if this flag is passed, an additional string offset is returned for each match.
    *   **PREG_UNMATCHED_AS_NULL:** if this flag is passed, mismatched subpatterns are reported as NULL; otherwise they are reported as empty strings.
*   **offset:** usually, the search starts at the beginning of the input string. This optional parameter offset is used to specify where to start the search in bytes.

**返回值：**如果模式存在，则返回 TRUE，否则返回 FALSE。

下面的示例说明了 PHP 中的 preg_Match()函数：

**示例 1：**此示例接受 PREG_OFFSET_CAPTURE 标志。

```php
<?php

// Declare a variable and initialize it
$geeks = 'GeeksforGeeks';

// Use preg_match() function to check match
preg_match('/(Geeks)(for)(Geeks)/', $geeks, $matches, PREG_OFFSET_CAPTURE);

// Display matches result
print_r($matches);

?>
```

**输出：**

```php
Array
(
    [0] => Array
        (
            [0] => GeeksforGeeks
            [1] => 0
        )

    [1] => Array
        (
            [0] => Geeks
            [1] => 0
        )

    [2] => Array
        (
            [0] => for
            [1] => 5
        )

    [3] => Array
        (
            [0] => Geeks
            [1] => 8
        )

)

```

**示例 2：**

```php
<?php

// Declare a variable and initialize it
$gfg = "GFG is the best Platform.";

// case-Insensitive search for the word "GFG"
if (preg_match("/\bGFG\b/i", $gfg, $match)) 
    echo "Matched!";
else
    echo "not matched";

?>
```

**输出：**

```php
Matched!

```

**引用：**[http://php.net/manual/en/function.preg-match.php](http://php.net/manual/en/function.preg-match.php)