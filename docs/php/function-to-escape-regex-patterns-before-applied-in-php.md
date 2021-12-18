# 函数在 PHP 中应用前转义正则表达式模式

> 原文:[https://www . geeksforgeeks . org/function-to-escape-regex-patterns-before-applied-in-PHP/](https://www.geeksforgeeks.org/function-to-escape-regex-patterns-before-applied-in-php/)

在运行时应用 regex 模式之前，在 PHP 中使用 preg_quote()函数对其进行转义。preg_quote()函数在指定字符串中的每个字符前加一个反斜杠，这将是 PHP 中 regex 语法的一部分，从而使它们成为转义序列。这些字符包括:
**。\ + * ?[ ^ ] $ ( ) { } = !|:–#**

**语法:**

```
*string* preg_quote( *string* $str, *string* $delimiter = NULL )
```

**参数:**

*   **$str:** 此参数保存输入字符串。
*   **$分隔符:**可选参数。最常见的分隔符是“/”，因为它不是通常由 preg_quote()处理的特殊正则表达式字符。主要与 [preg_replace()](https://www.geeksforgeeks.org/php-preg_replace-function/) 功能配合使用。

**返回:**返回包含字符串的分隔符。

下面的程序说明了 preg_quote()函数。

**程序 1:**

```
<?php

// Create a string which need to be escaped
$str = "Welcome to GfG! (+ The course fee. $400) /";

echo "Before Processing - " . $str . PHP_EOL;

// Use preg_quote() on above string
$processedStr = preg_quote($str);

// Display the output
echo "After Processing - " . $processedStr;

?>
```

**Output:**

```
Before Processing - Welcome to GfG! (+ The course fee. $400) /
After Processing - Welcome to GfG\! \(\+ The course fee\. \$400\) /

```

请注意，反斜杠放在每个特殊字符的前面，但不是正斜杠。为此，我们可以使用分隔符，参见下面的程序:

**程序 2**

```
<?php

// Create a string which need to be escaped
$str = "Welcome to GfG! (+ The course fee. $400) /";

echo "Before Processing - " . $str . PHP_EOL;

// Use preg_quote() on above string
$processedString = preg_quote($str, '/');

// Display the output
echo "After Processing - " . $processedString;

?>
```

**Output:**

```
Before Processing - Welcome to GfG! (+ The course fee. $400) /
After Processing - Welcome to GfG\! \(\+ The course fee\. \$400\) \/

```

下面的程序演示了 **preg_quote()** 和 **preg_replace()** 功能的组合使用。

**程序 3:**

```
<?php

// PHP Program emphasize the word within * * and 
// use font style to italic within [ ] using
// both preg_quote() and preg_replace() function

$str = "The *article* was written by [GFG]";

// The words to be formatted
$word1 = "*article*";
$word2 = "[GFG]";

// The first string only applies bold to word 1,
// preg_quote() escapes the * *
$processedStr1 = preg_replace("/" . preg_quote($word1, '/')
            . "/", "<strong>" . $word1 . "</strong>", $str);

echo "BOLD ONLY - " . $processedStr1 . PHP_EOL;

// The second string only applies italics to 
// word 2, preg_quote() escapes the [ ]
$processedStr2 = preg_replace("/" . preg_quote($word2, '/')
            . "/", "<em>" . $word2 . "</em>", $str);

echo "ITALIC ONLY - " . $processedStr2 . PHP_EOL;

// Combining both text formattings and display
$bothReplacementsCombined = preg_replace("/" .
            preg_quote($word2, '/') . "/",
            "<em>" . $word2 . "</em>", $processedStr1);

echo "BOTH COMBINED - " . $bothReplacementsCombined;

?>
```

**Output:**

```
BOLD ONLY - The *article* was written by [GFG]
ITALIC ONLY - The *article* was written by *[GFG]*
BOTH COMBINED - The *article* was written by *[GFG]*

```

**注意:**要注意文本格式标签的应用，应该在本地服务器上运行 PHP 并回显到浏览器。