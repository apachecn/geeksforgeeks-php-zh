# PHP str_place()函数

> Original: [https://www.geeksforgeeks.org/php-str_replace-function/](https://www.geeksforgeeks.org/php-str_replace-function/)

在本文中，我们将了解如何使用 PHP 中的 str_place()函数将搜索字符串的匹配项替换为替换字符串，并通过示例了解它们的实现。

**str_place()**是 PHP 中的一个内置函数，用于将所有出现的搜索字符串或搜索字符串数组分别替换为给定字符串或数组中的替换字符串或替换字符串数组。

**语法**：↔

```php
str_replace ( $searchVal, $replaceVal, $subjectVal, $count )
```

**参数**：此函数接受 4 个参数，其中 3 个为必选参数，1 个为可选参数。 所有这些参数都描述如下：

*   **$searchVal** : this parameter can be of either a string type or an array type. This parameter specifies the string to search for and replace.
*   **$replaceVal** : this parameter can be of either a string type or an array type. This parameter specifies the string to replace the *$searchVal* string.
*   **$subjectVal** : this parameter can be of either a string type or an array type. This parameter specifies the string or array of strings to search for *$searchVal* and replace with *$replaceVal* .
*   **$count** : this parameter is optional and, if passed, its value will be set to the total number of replacement operations performed on the string *$subjectVal* .

**返回值**：此函数返回基于*$subjectVal*参数的字符串或数组，其中包含替换的值。

**方法：**如果**$searchVal**和**$replaceVal**参数是数组，则在*$subjectVal*字符串中搜索*$searchVal*参数的所有元素，并替换为*$replaceVal*参数中的相应元素。 如果*$replaceVal*中的元素数量少于*$searchVal*数组中的元素数量，则如果在*$subjectVal*参数中出现*$searchVal*参数的附加元素，则这些元素将被空字符串替换。 如果*$SUBJECTVal*参数也是数组而不是字符串，则将搜索*$SUBJECTVal*的所有元素。

请考虑以下示例：

```php
Input:  $subjectVal  = "It was nice meeting you. May you shine brightly."
        str_replace('you', 'him', $subjectVal)
Output: It was nice meeting him. May him shine brightly.
Explanation: Every occurrence of *you* is replaced with *him*.

Input:  $subjectVal  = "You eat fruits, vegetables, fiber every day."
        $searchVal = array("fruits", "vegetables", "fiber")
        $replaceVal = array("pizza", "beer", "ice cream")
        str_replace($array1, $array2, $str)
Output: You eat pizza, beer, ice cream every day.
Explanation: Since both the arguments are arrays, therefore, 
every element from the first argument is replaced with 
the corresponding element from the second argument.
```

**示例 1**：下面的示例说明了 PHP 中的 str_place()函数。

## PHP

```php
<?php

  // Input string
  $subjectVal = "It was nice meeting you. May you shine bright.";

  // Using str_replace() function
  $resStr = str_replace('you', 'him', $subjectVal);
  print_r($resStr);
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2**：此示例描述了使用 str_place()函数将所有搜索字符串替换为替换字符串。

## PHP

```php
<?php

  // Input string
  $str  = "You eat fruits, vegetables, fiber every day.";

  // Array containing search string
  $searchVal = array("fruits", "vegetables", "fiber");

  // Array containing replace string from  search string
  $replaceVal = array("pizza", "beer", "ice cream");

  // Function to replace string
  $res = str_replace($searchVal, $replaceVal, $str);
  print_r($res);
?>
```

发帖主题：Re：Колибри0.7.8.0

**参考**：[http://php.net/manual/en/function.str-replace.php](http://php.net/manual/en/function.str-replace.php)

PHP 是一种专门为 Web 开发设计的服务器端脚本语言。 您可以按照这个[PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和[PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。