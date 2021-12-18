# 如何用 PHP 把第一个字符转换成大写？

> 原文:[https://www . geesforgeks . org/如何使用-php/](https://www.geeksforgeeks.org/how-to-convert-the-first-character-to-uppercase-using-php/) 将第一个字符转换为大写

字符串是组合在一起的单词的组合。如果字符串的第一个字符是小写字母字符，则可以转换为大写。

**方法 1:使用** [**chr()**](https://www.geeksforgeeks.org/php-chr-function/) **方法**

*   **第一步:**可以使用第一个索引*提取字符串的第一个字符，str【0】*返回输入字符串的第一个字符。

*   **第二步:**从字符串中提取的字符可以转换为大写，使用[**order()**](https://www.geeksforgeeks.org/php-ord-function/)函数，然后从其 ASCII 值中减去 32。然后使用 **chr()** 方法将大写字符的结果 ASCII 值转换为字符。

*   **第三步:**[**substr()**](https://www.geeksforgeeks.org/php-substr-function/)方法用于从索引的开始到结束返回原始字符串的子字符串。

可以使用 **substr()** 方法从字符串的第二个字符开始提取，直到字符串的长度。然后，转换为大写的第一个字符可以连接到获得的子字符串，以获得最终字符串。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
  //declaring string
  $str = "how!to?code? in geeksforgeeks";
  print("Original String : ".$str."\n<br/>"); 
//getting first char
  $ch = $str[0];
//converting to upper case
  $upper = chr(ord($ch)-32);
//appending the first remaining string to upper case character
  $fin_str = $upper.substr($str,1);
  print("Modified String : ".$fin_str);
?>
```

**Output**

```php
Original String : how!to?code? in geeksforgeeks
Modified String : How!to?code? in geeksforgeeks
```

**方法二:使用**[**【ucfirst()**](https://www.geeksforgeeks.org/php-ucfirst-function/)**方法**

**ucfirst()** 方法接受一个输入字符串，并将其第一个字符转换为大写，如果它是小写字母字符的话。输出必须保存在变量中以保留更改。

```php
ucfirst ( str )
```

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

  $str = "how!to?code? in geeksforgeeks";
  print("Original String : ".$str."\n<br/>"); 
  $upper = ucfirst($str);
  print("Modified String : ".$upper);
?>
```

**Output**

```php
Original String : how!to?code? in geeksforgeeks
Modified String : How!to?code? in geeksforgeeks
```

**方法三:使用**[**strtooper()**](https://www.geeksforgeeks.org/php-strtoupper-function/)**方法**

*   **步骤 1:** 可以使用第一个索引提取字符串的第一个字符， *str[0]* 返回输入字符串的第一个字符。

*   **第二步:**从字符串中提取的字符可以转换为大写，使用 **strtoupper()** 方法，该方法将输入作为字符串并将其转换为大写。因为一个字符也是一个字符串，所以在这个方法中它可以作为输入。

*   **步骤 3:** 在这种情况下，可以使用 **substr()** 方法从字符串的第二个字符提取字符串的长度。然后，转换为大写的第一个字符可以连接到获得的子字符串，以获得最终的字符串。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php
  //declaring string
  $str = "how!to?code? in geeksforgeeks";
  print("Original String : ".$str."\n<br/>"); 
//getting first char
  $ch = $str[0];
//converting to upper case
  $upper = strtoupper($ch);
//appending the first remaining string to uppercase character
  $fin_str = $upper.substr($str,1);
  print("Modified String : ".$fin_str);
?>
```

**Output**

```php
Original String : how!to?code? in geeksforgeeks
Modified String : How!to?code? in geeksforgeeks
```