# 如何在 PHP 中检查字符串是否包含子字符串？

> 原文:[https://www . geesforgeks . org/如何检查字符串是否包含 php 子字符串/](https://www.geeksforgeeks.org/how-to-check-if-a-string-contains-a-substring-in-php/)

字符串是给定字符的集合，子字符串是给定字符串中的字符串。

在本文中，我们将使用 PHP[**strpos()**](https://www.geeksforgeeks.org/php-strpos-stripos-functions/)**函数**来检查给定的字符串是否包含子字符串。****

****语法**:**

```
strpos($original_string,$sub_string);
```

****参数**:**

*   **原始字符串:输入字符串**
*   **sub_string:在原始输入字符串中搜索的子字符串。**

****返回类型:**布尔值**

*   **如果找到子字符串，则为真**
*   **如果未找到子字符串，则为 False。**

****示例:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php
//input string
$input_string = "sravan kumar author at geeks for geeks ";

//sub string to be checked
$sub = "geeks";

// Test if string contains the word
if (strpos($input_string, $sub) !== false)
{
    echo "True";
}
else
{
    echo "False";
}
?>
```

****输出:****

```
True
```

****例 2:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php
//input string
$input_string = "sravan kumar author at geeks for geeks ";

//sub string to be checked
$sub = "computer";

// Test if string contains the word
if (strpos($input_string, $sub) !== false)
{
    echo "True";
}
else
{
    echo "False";
}
?>
```

****输出:****

```
False
```

****例 3:** 下面的例子也考虑了空间。**

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php
//input string
$input_string = "geeks for geeks java python php";

//sub string to be checked
$sub = " ";

// Test if string contains the word
if (strpos($input_string, $sub) !== false)
{
    echo "True";
}
else
{
    echo "False";
}
?>
```

****输出:****

```
True
```

****例 4:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php
//input string
$input_string = "geeks for geeks java python php";

//sub string to be checked
$sub = " dbms";

// Test if string contains the word
if (strpos($input_string, $sub) !== false)
{
    echo "True";
}
else
{
    echo "False";
}
?>
```

****输出:****

```
False
```