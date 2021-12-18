# 如何删除 PHP 字符串中的控制字符？

> 原文:[https://www . geesforgeks . org/如何从 php 字符串中删除控制字符/](https://www.geeksforgeeks.org/how-to-remove-control-characters-from-php-string/)

给定包含控制字符的字符串。任务是从字符串中移除所有控制字符。在 ASCII 中，值小于 32 的所有字符都属于这一类。下面给出了一些控制字符:

| S.NO | ASCII 值 | 名字 | 标志 |
| 1. | Zero | null(null) | “\0” |
| 2. | nine | 水平标签 | " \t " |
| 3. | Ten | 进线(左前) | " \n " |
| 4. | Eleven | 垂直标签 | " \v " |
| 5. | Twenty-seven | 逃生 | " \e " |

**示例:**

```php
Input: str = "\0\eGeeks\t\e\tfor\v\vGeeks"
Output: GeeksforGeeks

```

在本文中，我们将使用两种不同的方法从 PHP 字符串中删除控制字符。

*   **使用通用正则表达式:**
*   **使用“cntrl”Regex:**

**使用通用正则表达式:**有许多正则表达式可以用来删除 ASCII 值低于 32 的所有字符。这里，我们将使用 **preg_replace()** 方法。

**注意:**ereg _ replace()方法是从 PHP > = 7 中移除的，所以这里我们将使用 preg_replace()方法。

*   **程序:**

    ```php
    <?PHP 

    // PHP program to remove all control 
    // characters from string 

    // String with control characters 
    $str = "\eGeeks\t\tfor\v\vGeeks\n"; 

    // Using preg_replace method to remove all  
    // control characters from string 
    $str = preg_replace('/[\x00-\x1F\x7F]/', '', $str); 

    // Display the modify string 
    echo($str); 

    ?> 
    ```

*   **输出:**

    ```php
    GeeksforGeeks
    ```

**使用‘cntrl’Regex:**这也可以用来移除所有控制字符。 **[:cntrl:]** 代表所有控制角色。

*   **程序:**

    ```php
    <?PHP 

    // PHP program to remove all control 
    // characters from string 

    // String with control characters 
    $str = "\eGeeks\t\tfor\vGeeks\n"; 

    // Using preg_replace method to remove all  
    // control characters from string 
    $str = preg_replace('/[[:cntrl:]]/', '', $str); 

    // Display the modify string 
    echo($str); 

    ?> 
    ```

*   **输出:**

    ```php
    GeeksforGeeks
    ```