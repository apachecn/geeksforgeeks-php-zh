# 如果 PHP 中的 URL 中不存在 http://如何添加？

> 原文:[https://www . geesforgeks . org/how-add-http-if-it-not-exists-in-the-URL-in-PHP/](https://www.geeksforgeeks.org/how-to-add-http-if-it-doesnt-exists-in-the-url-in-php/)

如果 URL 中不存在 **http://** 的话，有很多方法可以添加。其中一些将在下面讨论。
**方法 1:使用 preg_match()函数:**该函数在字符串中搜索模式，如果模式存在则返回 true，否则返回 false。通常，搜索从主题字符串的开头开始。可选参数 offset 用于指定开始搜索的位置。

**语法:**

```
int preg_match($pattern, $string, $pattern_array, $flags, $offset )
```

**返回值:**如果模式存在则返回真，否则返回假。

**例 1:** 本例取不带 **http://** 的 URL，返回完整的 URL。

```
<?php

// Function to add http
function addHttp($url) {

    // Search the pattern
    if (!preg_match("~^(?:f|ht)tps?://~i", $url)) {

        // If not exist then add http
        $url = "http://" . $url;
    }

    // Return the URL
    return $url;
}

// Declare a variable and initialize 
// it with URL
$url = "geeksforgeeks.org";

// Display URL
echo $url;
echo "\n";

// Display URL with http
echo addHttp($url);

?>
```

**Output:**

```
geeksforgeeks.org
http://geeksforgeeks.org

```