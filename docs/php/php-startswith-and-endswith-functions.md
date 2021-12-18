# PHP|startswith()和 endsWith()函数

> Original: [https://www.geeksforgeeks.org/php-startswith-and-endswith-functions/](https://www.geeksforgeeks.org/php-startswith-and-endswith-functions/)

**startswith()函数**

函数的作用是：测试字符串是否以给定字符串开头。 此函数不区分大小写，它返回布尔值。 该功能可与过滤功能配合使用，实现对数据的查询。
**语法**

```
bool startsWith( string, startString )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **String：**该参数用于保存需要测试的文本。
*   **startString：**要在字符串开头搜索的文本。 如果它是空字符串，则返回 TRUE。

**返回值：**此函数成功时返回 True，失败时返回 False。
**示例 1：**

```
<?php

// Function to check string starting
// with given substring
function startsWith ($string, $startString)
{
    $len = strlen($startString);
    return (substr($string, 0, $len) === $startString);
}

// Main function
if(startsWith("abcde","c"))
    echo "True";
else
    echo "False";
?> 
```

**Output:**

```
False

```