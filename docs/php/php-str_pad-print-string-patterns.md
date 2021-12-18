# PHP str_pad 打印字符串模式

> Original: [https://www.geeksforgeeks.org/php-str_pad-print-string-patterns/](https://www.geeksforgeeks.org/php-str_pad-print-string-patterns/)

**str_pad**：
用另一个字符串填充某个长度的字符串。

```
Syntax:- str_pad (input, pad_length, pad_string_value, pad_type)
It returns the padded string.

```

**参数说明**

> **输入：-**输入字符串。
> **PAD_LENGTH：-**如果 PAD_LENGTH 的值为负，小于或等于输入字符串的长度，则不会进行填充，并返回输入。
> **PAD_STRING_INPUT：-**如果所需的填充字符数不能平均除以 PAD_STRING 的长度，则 PAD_STRING 可能会被截断。
> **PAD_TYPE：-**可选参数 PAD_TYPE 可以是 STR_PAD_RIGHT、STR_PAD_LEFT 或 STR_PAD_BOTH。 如果未指定 PAD_TYPE，则假定为 STR_PAD_RIGHT。

在循环下使用单行代码打印如下所示的简单模式。
**示例：** 

```
Input : 5
Output :
    *
   **
  ***
 ****
*****

Input : 6
Output :
     *
    **
   ***
  ****
 *****
******

```

```
<?php
// PHP program to print a pattern using only
// one loop.

function generatePattern($n)
{
    // Initialize the string
    $str = "";

    // Iterate for n lines
    for ($i=0 ; $i<$n ; $i++)
    {
        // Concatenate the string
        $str .= "*";
        echo str_pad($str, $n, " ", STR_PAD_LEFT), "\n";
    }
}

// Driver code
$n = 6;
generatePattern($n);
?>
```

**Output:**

```
     *
    **
   ***
  ****
 *****
******

```