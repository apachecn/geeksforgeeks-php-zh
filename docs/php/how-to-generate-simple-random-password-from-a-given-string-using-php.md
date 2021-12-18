# 如何用 PHP 从给定的字符串生成简单的随机密码？

> 原文:[https://www . geesforgeks . org/如何使用 php 从给定字符串生成简单随机密码/](https://www.geeksforgeeks.org/how-to-generate-simple-random-password-from-a-given-string-using-php/)

在本文中，我们将看到如何使用给定的字符串生成随机密码。我们给出了一个字符串，任务是从中生成一个随机密码。

**示例:**

```
Input:  abgADKL123
Output: abgADKL123

Input: geeksforgeeks
Output:    egksegsfroeke
```

为此，我们使用以下方法。

**方法 1:** 在这种方法中，我们使用 PHP [**rand()**](https://www.geeksforgeeks.org/php-rand-function/) 函数并创建一个临时变量，并使用 for 循环从给定字符串创建随机字符，并将该字符连接到临时变量。下面是这种方法的实现。

**PHP 代码:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Function to generate password from 
// given string
function get_password($str, $len = 0) {

    // Variable $pass to store password
    $pass = "";

    // Variable $str_length to store 
    // length of the given string
    $str_length = strlen($str);

    // Check if the $len is not provided
    // or $len is greater than $str_length
    // then assign $str_length to $len
    if($len == 0 || $len > $str_length){
        $len = $str_length;
    }

    // Iterate $len times so that the 
    // resulting string's length is 
    // equal to $len
    for($i = 0;  $i < $len; $i++){

        // Concatenate random character 
        // from $str with $pass
        $pass .=  $str[rand(0, $str_length)];
    }
    return $pass;
}

// Print password of length 5 from 
// the given string
$str = "GeeksForGeeks";
echo get_password($str, 5) . "\n<br/>";

// Print password of length 15 from
// the given string
$str = 
"abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ123456789";
echo get_password($str, 15) ."\n<br/>";

// Print password if the length 
// is not given
echo get_password($str) . "\n<br/>";

?>
```

**输出:**

```
skGse
iWwf9jWZZE9ZL7O
GhRQ8zK4wpX93srUj1LhjsBEeBwBwo4Bh43RyZeSFZbwjVoonkKBgfXiBrEpY
```

**方法 2:** 在这个方法中，我们使用 PHP[**str _ shuffle**()](https://www.geeksforgeeks.org/php-str_shuffle-function/)函数，然后我们使用[**substr()**](https://www.geeksforgeeks.org/php-substr-function/)**函数提取给定字符串的部分。**

****PHP 代码:****

## **服务器端编程语言（Professional Hypertext Preprocessor 的缩写）**

```
<?php

// Function to generate password from
// given string
function get_password($str, $len = 0) {

    // Variable $pass to store password
    $pass = "";

    // Variable $str_length to store
    // length of the given string
    $str_length = strlen($str);

    // Check if the $len is not provided
    // or $len is greater than $str_length
    // then assign $str_length into $len
    if($len == 0 || $len > $str_length){
        $len = $str_length;
    }

    // Shuffle the string 
    $pass = str_shuffle($str);

    // Extract the part of string
    $pass = substr($pass, 0, $len);

    return $pass;
}

// Print password of length 5 from
// the given string
$str = "GeeksForGeeks";
echo get_password($str) . "\n<br/>";

// Print password of length 15 from
// the given string
$str = 
"abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ123456789";
echo get_password($str, 15) ."\n<br/>";

// Print password if the length is
// not given
echo get_password($str) . "\n<br/>";

?>
```

****输出:****

```
oeFssGkeGrkee
rxIhAjCi47wgW1z
r4LZQqlOFGU36i7gEAtzwsnduNXhHKD92ajpxBJc1MRvVmbyeokPIWfCTSY85
```