# PHP 中如何去除字符串中的特殊字符？

> 原文:[https://www . geesforgeks . org/如何从 php 字符串中删除特殊字符/](https://www.geeksforgeeks.org/how-to-remove-special-character-from-string-in-php/)

在本文中，我们将看到如何在 PHP 中删除字符串中的特殊字符，并通过示例了解它们的实现。我们已经给了一个字符串，我们需要从 PHP 中的字符串 **str** 中删除特殊字符，为此，我们在 PHP 中有以下方法:

**使用** [**str_replace** **()方法**](https://www.geeksforgeeks.org/php-str_replace-function/)**:****str _ replace()**方法用于通过用空格**(" ")替换给定字符串 **str** 中的所有特殊字符来移除这些字符。**

**语法** :

```
str_replace( $searchVal, $replaceVal, $subjectVal, $count )
```

**示例:**此示例说明了如何使用 **str_replace()** 函数从字符串中删除特殊字符。

## PHP

```
<?php
  // PHP program to Remove 
  // Special Character From String

  // Function to remove the spacial 
  function RemoveSpecialChar($str) {

      // Using str_replace() function 
      // to replace the word 
      $res = str_replace( array( '\'', '"',
      ',' , ';', '<', '>' ), ' ', $str);

      // Returning the result 
      return $res;
      }

  // Given string
  $str = "Example,to remove<the>Special'Char;"; 

  // Function calling
  $str1 = RemoveSpecialChar($str); 

  // Printing the result
  echo $str1; 
?>
```

**输出:**

```
Example to remove the Special Char
```

**使用** [**str_ireplace()方法**](https://www.geeksforgeeks.org/php-str_ireplace-function/) **:** 使用 **str_ireplace()方法**通过用空格**(" ")替换给定字符串中的所有特殊字符来移除这些字符。**str _ replace 和 **str_ireplace** 的区别在于 **str_ireplace** 不区分大小写。

**语法** :

```
str_ireplace( $searchVal, $replaceVal, $subjectVal, $count )
```

**示例:**此示例说明了如何使用 **str_ireplace()** 方法从字符串中移除所有特殊字符。

## PHP

```
<?php
  // PHP program to Remove 
  // Special Character From String

  // Function to remove the spacial 
  function RemoveSpecialChar($str){

      // Using str_ireplace() function 
      // to replace the word 
      $res = str_ireplace( array( '\'', '"',
      ',' , ';', '<', '>' ), ' ', $str);

      // returning the result 
      return $res;
      }

  // Given string
  $str = "Example,to remove<the>Special'Char;"; 

  // Function calling
  $str1 = RemoveSpecialChar($str); 

  // Printing the result
  echo $str1; 
?>
```

**输出:**

```
Example to remove the Special Char
```

**使用** [**preg_replace()方法**](https://www.geeksforgeeks.org/php-preg_replace-function/) **:** 使用 **preg_replace()方法**执行正则表达式搜索并替换内容。

**语法** :

```
preg_replace( $pattern, $replacement, $subject, $limit, $count )
```

**示例:**此示例说明了 **preg_replace()** 方法的使用，其中输入字符串中找到的特定或所有匹配模式将被替换为子字符串或空格。

## PHP

```
<?php
  // PHP program to Remove 
  // Special Character From String

  // Function to remove the spacial 
  function RemoveSpecialChar($str){

      // Using preg_replace() function 
      // to replace the word 
      $res = preg_replace('/[^a-zA-Z0-9_ -]/s',' ',$str);

      // Returning the result 
      return $res;
  }

  // Given string
  $str = "Example,to remove<the>Special'Char;"; 

  // Function calling
  $str1 = RemoveSpecialChar($str); 

  // Printing the result
  echo $str1; 
?>
```

**输出:**

```
Example to remove the Special Char
```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。