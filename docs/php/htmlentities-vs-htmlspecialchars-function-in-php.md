# html entities()vs html specialchars()PHP 中的函数

> 原文:[https://www . geesforgeks . org/htmlentities-vs-html specialchars-function-in-PHP/](https://www.geeksforgeeks.org/htmlentities-vs-htmlspecialchars-function-in-php/)

在本文中，我们将了解 html entities()& html specialchars()函数的用途，并通过示例了解它们的实现。

**htmlentities()函数:**HTML entities()函数是 PHP 中的一个内置函数，用于转换所有适用于 HTML 实体的字符。该函数转换适用于 HTML 实体的所有字符。

**语法:**

```
string htmlentities( $string, $flags, $encoding, $double_encode )
```

**参数值:**该函数接受如上所述及如下所述的四个参数:

*   **$ string:** This parameter is used to store the input string.
*   **$ flags:** This parameter is used to save flags. It is a combination of one or two flags that tell how to handle the quotation.
*   **$ encoding:** It is an optional parameter that specifies the encoding used when converting characters. If no encoding is given, it will be converted according to the default version of PHP.
*   [T0】 $ double_encode: 【T1 If double _ encode is turned off, PHP will not encode the existing HTML entities. The default value is to convert everything.

**返回值:**该函数返回已编码的字符串。

**示例:**本示例使用 htmlentities()函数来转换适用于 HTML 实体的所有字符。

## PHP

```
<?php

  // String convertable to htmlentities
  $str = '<a href="https://www.geeksforgeeks.org">GeeksforGeeks</a>';

  // It will convert htmlentities and print them
  echo htmlentities( $str );
?>
```

**输出:**

```
<a href="https://www.geeksforgeeks.org">GeeksforGeeks</a>
```

**htmlspecialchars()函数:**HTML specialchars()函数是 PHP 中的内置函数，用于将所有预定义的字符转换为 HTML 实体。

**语法:**

```
string htmlspecialchars( $string, $flags, $encoding, $double_encode )
```

**参数值:**

*   **$ string:** This parameter is used to store the input string.
*   **$ flags:** This parameter is used to save flags. It is a combination of one or two flags that tell how to handle the quotation.
*   **$ encoding:** It is an optional parameter that specifies the encoding used when converting characters. If no encoding is given, it will be converted according to the default version of PHP.
*   [T0】 $ double_encode: 【T1 If double _ encode is turned off, PHP will not encode the existing HTML entities. The default value is to convert everything.

**返回值:**该函数返回转换后的字符串。如果输入字符串无效，将返回一个空字符串。

**示例:**本示例使用 htmlspecialchars()函数将所有预定义字符转换为 HTML 实体。

## PHP

```
<?php

  // String to be converted
  $str = '"geeksforgeeks.org" Go to GeeksforGeeks';

  // Converts double and single quotes
  echo htmlspecialchars($str, ENT_QUOTES);
?>
```

**输出:**

```
"geeksforgeeks.org" Go to GeeksforGeeks
```

**htmlentities()和 htmlspecialchars()函数的区别:**这两个函数唯一的区别是 htmlspecialchars()函数将特殊字符转换为 HTML 实体，而 HTML entities()函数将所有适用的字符转换为 HTML 实体。