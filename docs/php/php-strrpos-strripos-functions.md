# PHP|strrpos()和 strripos()函数

> Original: [https://www.geeksforgeeks.org/php-strrpos-strripos-functions/](https://www.geeksforgeeks.org/php-strrpos-strripos-functions/)

我们已经了解了[strpos()和 stripos()](https://www.geeksforgeeks.org/php-strpos-stripos-functions/)，它们有助于查找一个字符串在另一个字符串中的第一个匹配项。 在本文中，我们将了解另外两个类似的函数 strrpos()和 strripos()。

PHP 中的**strrpos()**

与 strpos()不同，strrpos()函数帮助我们找到一个字符串在另一个字符串中最后出现的位置。 此函数返回与字符串最后一次出现的位置相对应的整数值。 此函数是**区分大小写的**，这意味着它对大小写字符的处理方式不同。

**语法：**

```
strrpos(original_str, search_str, start_pos)

```

**参数**和
在语法中指定的三个参数中，两个是必需的，一个是可选的。 下面介绍这三个参数：

1.  **Original_str(必选)：**该参数表示需要查找所需字符串匹配项的原始字符串。
2.  **search_str(必选)：**该参数是指我们需要搜索的字符串。
3.  **start_pos(可选)：**表示字符串的位置，必须从该位置开始搜索。

**返回类型**：此函数返回一个整数值，表示字符串 search_str 最后出现的 Original_str 的索引。

**示例：**

## PHP

```
<?php
// PHP code to search for a specific string's position
// last occurrence using strrpos() case-sensitive function
function Search($search, $string){
    $position = strrpos($string, $search, 5); 
    if ($position == true){
        return "Found at position " . $position;
    }
    else{
        return "Not Found";
    }
}

// Driver Code
$string = "Welcome to GeeksforGeeks";
$search = "Geeks";
echo Search($search, $string);
?>
```

**输出：**

```
Found at position 19

```

PHP__t1 中的\\t0++strripos()\\

与 stripos()不同，strripos()函数帮助我们找到一个字符串在另一个字符串中最后出现的位置。 此函数返回与字符串最后一次出现的位置相对应的整数值。 此函数是**不区分大小写的**，这意味着它对大小写字符一视同仁。

**语法：**

```
strripos(original_str, search_str, start_pos)

```

**参数**和
在语法中指定的三个参数中，两个是必需的，一个是可选的。 下面介绍这三个参数：

1.  **Original_str(必选)：**该参数表示需要查找所需字符串匹配项的原始字符串。
2.  **search_str(必选)：**该参数是指我们需要搜索的字符串。
3.  **start_pos(可选)：**表示字符串的位置，必须从该位置开始搜索。

**返回类型**：此函数返回一个整数值，表示字符串 search_str 最后出现的 Original_str 的索引。

**示例：**

## PHP

```
<?php
// PHP code to search for a specific string
// last occurrence using strripos() case-insensitive function
function Search($search, $string){
    $position = strripos($string, $search, 5); 
    if ($position == true){
        return "Found at position " . $position;
    }
    else{
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

```
Found at position 19

```