# 如何在 PHP 中将一个字符串重复到特定的次数？

> 原文:[https://www . geesforgeks . org/如何将字符串重复到特定的 php 次数/](https://www.geeksforgeeks.org/how-to-repeat-a-string-to-a-specific-number-of-times-in-php/)

字符串是存储在 PHP 中的一系列字符。该字符串可能包含特殊字符或数值或字符。字符串可以包含任意数量的字符，并且可以由较小的子字符串组合而成。

**方法 1:使用 for 循环:**声明一个空字符串变量，以便存储最终字符串的内容。声明一个整数值 n，表示字符串重复的次数。每次将原始字符串追加到声明的最终字符串变量的末尾时。然后显示最终字符串的内容。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Declaring string variable 
$str = "Hi!GFG User.";
echo("Original string : ");
echo($str . "</br>");

// Declaring number of times 
$n = 3;

// Declaring empty string
$final_str = "";

// Looping over n times
for($i = 0; $i < $n; $i++) {

      // Appending str to final string value
    $final_str .= $str;
}
echo("Final string : ");
echo($final_str . "</br>");

?>
```

**Output**

```php
Original string : Hi!GFG User.
Final string : Hi!GFG User.Hi!GFG User.Hi!GFG User.
```

**方法二:使用 str_repeat 方法:**PHP 中内置的 str_repeat()方法可以将指定的字符串重复指定的次数。内容可以存储在单独的变量名中。该方法具有以下语法:

```php
str_repeat( str, n)
```

**参数:**

*   **str–**是原字符串。
*   **n–**重复一个字符串的次数。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Declaring string variable 
$str = "Hi!GFG User.";
echo("Original string : ");
echo($str."</br>");

// Declaring number of times 
$n = 3;

// Computing final string
$final_str = str_repeat($str, $n);
echo("Final string : ");
echo($final_str . "</br>");

?>
```

**Output**

```php
Original string : Hi!GFG User.
Final string : Hi!GFG User.Hi!GFG User.Hi!GFG User.
```