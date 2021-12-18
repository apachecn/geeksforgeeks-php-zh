# PHP strpos()和 stripos()函数

> Original: [https://www.geeksforgeeks.org/php-strpos-stripos-functions/](https://www.geeksforgeeks.org/php-strpos-stripos-functions/)

在本文中，我们将了解如何使用 PHP 中的 strpos()和 stripos()函数查找一个字符串在另一个字符串中第一次出现的位置，并通过示例了解它们的实现。

PHP 中的 strpos()和 stripos()函数都是**二进制安全的**，这意味着该函数将把它的输入作为原始字节流处理，并忽略它可能包含的所有文本内容。 在这里，当传递任意二进制数据(即具有非 ASCII 字节&/或空字节的字符串)时，该函数将正确工作。

**strpos()函数：**该函数帮助我们找到一个字符串在另一个字符串中第一次出现的位置。 这将返回字符串第一次出现的位置的整数值。 此函数区分**大小写**，这意味着它对大小写字符的处理方式不同。

**语法：**

```php
strpos(original_str, search_str, start_pos);
```

**参数值**：语法中指定的三个参数中，两个是必选的，一个是可选的。 下面介绍这三个参数：

*   **Original_str：**这是一个必选参数，引用我们需要在其中搜索所需字符串的匹配项的原始字符串。
*   **search_str：**这是一个必选参数，引用我们需要搜索的字符串。
*   **start_pos：**这是一个可选参数，表示必须开始搜索的字符串位置。

**返回类型**：此函数返回一个整数值，表示字符串*search_str*首次出现的*Original_str*的索引。

**示例：**此示例说明了指定一个字符串在另一个字符串中出现的位置的**strpos()**函数。

## PHP

```php
<?php

    // PHP code to search for a specific string's position
    // first occurrence using strpos() case-sensitive function
    function Search($search, $string)
    {
        $position = strpos($string, $search, 5);
        if (is_numeric($position))
        {
            return "Found at position: " . $position;
        }
        else
        {
            return "Not Found";
        }
    }

    // Driver Code
    $string = "Welcome to GeeksforGeeks";
    $search = "Geeks";
    echo Search($search, $string);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Found at position 11
```

**stripos()函数：**该函数还帮助我们找到一个字符串在另一个字符串中第一次出现的位置。 这将返回字符串第一次出现的位置的整数值。 此函数是**不区分大小写的**，这意味着它对大小写字符一视同仁。 此函数的工作方式与 strpos()类似，不同之处在于它区分大小写，而 strpos()区分大小写。

**语法：**

```php
stripos(original_str, search_str, start_pos);
```

**参数值**：语法中指定的三个参数中，两个是必选的，一个是可选的。

*   **Original_str：**这是一个必选参数，引用我们需要在其中搜索所需字符串的匹配项的原始字符串。
*   **search_str：**这是一个必选参数，引用我们需要查找的字符串。
*   **start_pos：**这是一个可选参数，表示必须开始搜索的字符串位置。

**返回类型**：此函数返回一个整数值，表示字符串*search_str*首次出现的*Original_str*的索引。

**示例：**此示例说明了指定一个字符串在另一个字符串中出现的位置的**stripos()**函数。

## PHP

```php
<?php

    // PHP code to search for a specific string
    // first occurrence using stripos() case-insensitive function
    function Search($search, $string)
    {
        $position = stripos($string, $search, 5);
        if ($position == true)
        {
            return "Found at position " . $position;
        }
        else
        {
            return "Not Found";
        }
    }

    // Driver Code
    $string = "Welcome to GeeksforGeeks";
    $search = "geeks";
    echo Search($search, $string);
?>
```

**输出：**

```php
Found at position 11
```