# PHP|preg_place()函数

> Original: [https://www.geeksforgeeks.org/php-preg_replace-function/](https://www.geeksforgeeks.org/php-preg_replace-function/)

Preg_place()函数是 PHP 中的一个内置函数，用于执行正则表达式以搜索和替换内容。

**语法：**

```
preg_replace( $pattern, $replacement, $subject, $limit, $count )
```

**参数：**此函数接受上述五个参数，如下所述。

*   **$Pattern:** this parameter contains the String element used to search for content, which can be a string or an array of strings.
*   **$Replace:** required parameter that specifies the string to replace or an array containing strings.
*   **$SUBJECT:** the string or array containing strings to search for and replace.
*   **$Limit:** this parameter specifies the maximum number of possible substitutions for each pattern.
*   **$count:** optional parameters. This variable will populate the number of completed replacements.

**返回值：**如果 Subject 参数是数组，则此函数返回数组，否则返回字符串。

下面的程序演示了 PHP 中的 preg_place()函数：

**程序 1：**

```
<?php

// PHP program to illustrate 
// preg_replace function

$string = 'November 01, 2018';
$pattern = '/(\w+) (\d+), (\d+)/i';
$replacement = '${1} 02, $3';

// print output of function
echo preg_replace($pattern, $replacement, $string);
?>
```

**输出：**

```
November 02, 2018

```

**程序 2：**

```
<?php

// PHP program to illustrate 
// preg_replace function
$subject = array('1', 'GFG', '2',
'Geeks', '3', 'GCET', 'Contribute', '4'); 
$pattern = array('/\d/', '/[a-z]/', '/[1a]/'); 
$replace = array('X:$0', 'Y:$0', 'Z:$0'); 

// Print Result return by function
echo "preg_replace returns\n";
print_r(preg_replace($pattern, $replace, $subject)); 
?>
```

**输出：**

```
preg_replace returns
Array
(
    [0] => X:Z:1
    [1] => GFG
    [2] => X:2
    [3] => GY:eY:eY:kY:s
    [4] => X:3
    [5] => GCET
    [6] => CY:oY:nY:tY:rY:iY:bY:uY:tY:e
    [7] => X:4
)

```

**程序 3：**

```
<?php

// PHP program to illustrate 
// preg_replace function
$count = 0;

// Display result after replace and count 
echo preg_replace(array('/\d/', '/\s/'),
        '*', 'Geeks 4 Geeks', -1, $count);
echo "\n" . $count;
?>
```

**输出：**

```
Geeks***Geeks
3

```

**引用：**[http://php.net/manual/en/function.preg-replace.php](http://php.net/manual/en/function.preg-replace.php)