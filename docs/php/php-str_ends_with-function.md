# PHP str_ends_with()函数

> Original: [https://www.geeksforgeeks.org/php-str_ends_with-function/](https://www.geeksforgeeks.org/php-str_ends_with-function/)

函数**str_ends_with()**是 PHP 8 中的一个预定义函数，用于对给定字符串执行区分大小写的搜索。 Str_ends_with()通常检查字符串是否以子字符串结尾。 如果字符串以子字符串结尾，则 str_ends_with()将返回 TRUE，否则将返回 FALSE。 它与 str_starts_with()非常相似，str-starts_with()和 str_ends_with()之间唯一的关键区别在于，str-starts_with()搜索字符串开头的子字符串，而 str_ends_with()搜索字符串末尾的子字符串。

**语法：**

```php
str_starts_with(string $string, string $substring) 
```

**参数：**

*   **$string：**$string 是指需要搜索其结束字符串的字符串。
*   **$substring：**$substring 是需要在$string 中搜索的字符串。

**主要特点：**

*   它本质上是区分大小写的。
*   它始终返回布尔值。
*   它既可以用来检查 Sting 的结尾，也可以用来检查字符的结尾。
*   如果子字符串为空或 NULL，则始终返回 TRUE，因为每个字符串都以 NULL 结尾。
*   低于 8 的 PHP 版本不支持此功能。

**示例 1：**在此示例中，创建了三个变量。 ***$STRING***用于存储字符串值，***$endsWith***用于存储将在$字符串末尾搜索的值，***$Result***用于存储结果值。 在程序中，如果字符串$endsWith 位于$string 的末尾，则函数 str_ends_with()将返回 TRUE，否则它将返回 FALSE 给三元运算符，并相应地为变量$RESULT 赋值。

## PHP

```php
<?php

    $string = 'GFG is awesome';
    $endsWith = 'some';

    $result = str_ends_with($string, $endsWith) ? 'is' : 'is not';

    echo "The string \"$string\" $result ending with $endsWith";

?>
```

发帖主题：Re：Колибри0.7.8.0

```php
The string "GFG is awesome" is ending with some
```

**示例 2：**在本例中，我们创建了两个变量$string 用于存储字符串，$endsWith 用于存储需要在$string 末尾检查的结束值。 在这里，$endsWith 的值将为空，我们将检查字符串是否以空字符串结尾。 在这种情况下，if-Condition 的输出将始终为真，因为所有字符串都以‘\0’结尾，并相应地显示输出。

## PHP

```php
<?php

    $string = 'Checking for Blanks in the string';
    $endsWith = '';

    if(str_ends_with($string, $endsWith)) {
      echo 'Given String ends with an empty string';      
    }
    else {
      echo 'Given String does not ends with an empty string'; 
    }

?>
```

输出
**输出：**

```php
 Given String ends with an empty string
```

**引用：**[https://www.php.net/manual/en/function.str-ends-with.php](https://www.php.net/manual/en/function.str-ends-with.php)