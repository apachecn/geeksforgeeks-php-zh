# PHP|preg_plit()函数

> Original: [https://www.geeksforgeeks.org/php-preg_split-function/](https://www.geeksforgeeks.org/php-preg_split-function/)

Preg_plit()函数是 PHP 中的内置函数，用于将给定的字符串转换为数组。 该函数将字符串拆分为较小的字符串或用户指定长度的子字符串。 如果指定了限制，则限制的小字符串或子字符串将通过数组返回。 Preg_plit()函数类似于 EXPLODE()函数，但区别用于正则表达式以指定分隔符，但未使用 EXPLODE。

**语法：**

```
array preg_split( $pattern, $subject, $limit, $flag )
```

**参数：**此函数接受上述四个参数，如下所述：

*   **$Pattern：**该值是字符串类型，模式将作为字符串进行搜索，否则它将分隔元素。
*   **$SUBJECT：**$SUBJECT 是用于存储输入字符串的变量。
*   **$Limit：**$Limit 表示限制。 如果指定了限制，则返回小字符串或子字符串直至限制。如果限制为 0 或-1，则表示“无限制”，然后由标志($strflag)使用。
*   **$FLAGS：**$FLAGS 用于发信号，其变量类型用于指示两种状态 True 或 False 来控制程序。 其不同标志的组合如下：
    *   **PREG_SPLIT_NO_EMPTY：**如果标志变量设置为 PREG_SPLIT_NO_EMPTY，则 preg_plit()函数将只返回非空段。
    *   **PREG_SPLIT_DELIM_CAPTURE：**如果标志变量设置为 PREG_SPLIT_DELIM_CAPTURE，则还将捕获并返回分隔符模式中的带括号表达式。
    *   **PREG_SPLIT_OFFSET_CAPTURE：**如果标志变量设置为 PREG_SPLIT_OFFSET_CAPTURE，则对于每个匹配项，将返回附加字符串偏移量，并更改数组中的返回值，其中匹配的字符串偏移量为 0，输入字符串偏移量为 1。

**返回值：**此函数返回分割边界匹配后的数组。 当原始数组或字符串超出限制时，则返回一个数组元素，否则为 false。

下面的程序说明了 PHP：
**程序 1：**中的 preg_plit()函数

```
<?php

// Input string
$inputstrVal  = 'Geeksarticle';

// Implementaion of preg_split() function
$result = preg_split('//', $inputstrVal , -1, PREG_SPLIT_NO_EMPTY);

// Display result
print_r($result);
?>
```

**Output:**

```
Array
(
    [0] => G
    [1] => e
    [2] => e
    [3] => k
    [4] => s
    [5] => a
    [6] => r
    [7] => t
    [8] => i
    [9] => c
    [10] => l
    [11] => e
)

```

**程序 2：**

```
<?php

// PHP program of preg_split() function
// split the phrase by any number of commas 
// space characters include \r, \t, \n and \f

$result = preg_split("/[\s,]+/", "Geeks for Geeks");

// Display result
print_r($result);
?>
```

**Output:**

```
Array
(
    [0] => Geeks
    [1] => for
    [2] => Geeks
)

```

**程序 3：**

```
<?php 

// PHP program to implementation of
// preg_split() function

// Input original string
$inputstrVal = "http://php.net/archive/2018.php"; 
$patternstrVal= "/[http:\/\/|\.]/"; 

// Implement preg_split() function
$result = preg_split($patternstrVal, $inputstrVal, 0, 
   PREG_SPLIT_NO_EMPTY | PREG_SPLIT_OFFSET_CAPTURE); 

// Display result
print_r($result ); 
?> 
```

**Output:**

```
Array
(
    [0] => Array
        (
            [0] => ne
            [1] => 11
        )

    [1] => Array
        (
            [0] => arc
            [1] => 15
        )

    [2] => Array
        (
            [0] => ive
            [1] => 19
        )

    [3] => Array
        (
            [0] => 2018
            [1] => 23
        )

)

```

**引用：**[http://php.net/manual/en/function.preg-split.php](http://php.net/manual/en/function.preg-split.php)