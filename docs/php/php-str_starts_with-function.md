# PHP str_starts_with()函数

> Original: [https://www.geeksforgeeks.org/php-str_starts_with-function/](https://www.geeksforgeeks.org/php-str_starts_with-function/)

这是 PHP 8 中的一个预定义函数，用于对给定字符串执行区分大小写的搜索。 **str_starts_with()**通常检查字符串是否以子字符串开头。 如果字符串以子字符串开头，则**str_starts_with()**将返回*true*，否则将返回*false*。

**语法：**

```
str_starts_with($string, $substring) 
```

**参数：**

*   **$string:** this parameter refers to the string that needs to be checked for the starting string.
*   **$SUBSTRING:** this parameter represents the string that needs to be checked.

**返回类型：**如果字符串以子字符串开头，则**str_starts_with()**将返回*true*，否则将返回*false*。

**主要特点：**

*   **str_starts_with ()** is essentially case-sensitive.
*   **str_starts_with ()** always returns a Boolean value.
*   **str_starts_with ()** can be used to check both the beginning of a character and the beginning of a string.
*   **PHP versions less than 8 do not support STR_STARTS_WITH ()** .

**示例 1：**在下面的程序中，我们创建了三个变量***$NAME*来存储类型字符串的名称，*$BeginsWith*来存储需要用*$Name，*和*$Result*来存储根据**str_starts_with()**计算的表达式的结果。 如果字符串*$NAME*以子字符串*$BeginsWith*开头，则**str_start_with()**将返回*TRUE*，否则将返回*FALSE*，并相应地为*$Result*赋值。**

## **PHP**

```
<?php

    $name = 'Saurabh Singh';
    $beginsWith = 'S';

    $result = str_starts_with($name, $beginsWith) ? 'is' : 'is not';

    echo "The string \"$name\" $result starting with $beginsWith";

?>
```

****输出：****

```
The string "Saurabh Singh" is starting with S
```

****示例 2：**在第一个示例中，我们取句子的开头字符进行搜索。 在本例中，我们采用了句子开头的完整单词，它还将在 if 条件中返回*TRUE*，并进一步相应地执行条件部分。**

## **PHP**

```
<?php

    $sentance = 'The Big Brown Fox';
    $beginsWith = 'The';

    if(str_starts_with($sentance , $beginsWith) )
    {
      echo "The string \"$sentance\" begins with \"$beginsWith\" ";
    }
    else
    {
      echo "The string \"$sentance\" does not begins with \"$beginsWith\" ";
    }    

?>
```

****输出：****

```
The string "The Big Brown Fox" begins with "The" 
```

****引用：**[https://www.php.net/manual/en/function.str-starts-with.php](https://www.php.net/manual/en/function.str-starts-with.php)**