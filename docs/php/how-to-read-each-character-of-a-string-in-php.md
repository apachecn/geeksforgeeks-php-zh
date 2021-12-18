# 如何在 PHP 中读取字符串的每个字符？

> 原文:[https://www . geesforgeks . org/如何阅读 php 中的每个字符串字符/](https://www.geeksforgeeks.org/how-to-read-each-character-of-a-string-in-php/)

字符串是一系列字符。它可能包含整数，甚至特殊符号。字符串中的每个字符都存储在由唯一索引值表示的唯一位置。

**方法 1:使用**[**str _ split()**](https://www.geeksforgeeks.org/php-str_split-function/)**方法–****str _ split()**方法用于将指定的字符串变量拆分为一个值数组，每个值都映射到一个以 0 开头的索引值。此方法将输入字符串转换为数组。

```php
str_split(str)
```

[PHP foreach](https://www.geeksforgeeks.org/php-foreach-loop/) 循环迭代然后可以在数组值上完成，每个元素属于字符串的一个字符。然后，在每个值之间打印一个空格。

**示例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Declaring string variable 
$str = "Hi!GFG User.";

echo("Original string : ");
echo($str . "</br>");

$array = str_split($str);
echo("Characters : ");

foreach($array as $val){
    echo($val . " ");
}

?>
```

**输出:**

```php
Original string : Hi!GFG User.
Characters : H i ! G F G U s e r .
```

**方法二:使用 strlen()方法–**使用**[**strlen()**](https://www.geeksforgeeks.org/php-strlen-function/)**方法计算 PHP 中指定字符串的长度。使用字符串的长度应用循环迭代的[，每次打印第 i <sup>个</sup>索引字符。时间复杂度与前面的方法相同。但是，以数组对象的形式存储字符串不需要额外的空间。](https://www.geeksforgeeks.org/php-loops/)****

```php
**strlen(str)**
```

******示例:******

## ****服务器端编程语言（Professional Hypertext Preprocessor 的缩写）****

```php
**<?php

// Declaring string variable 
$str = "Hi!GFG User.";

echo("Original string : ");
echo($str."</br>");
echo("Characters : ");

// Iterating over the string 
$len = strlen($str);

for ($i = 0; $i < $len; $i++){
    echo ($str[$i]." ");
}

?>**
```

******输出:******

```php
**Original string : Hi!GFG User.
Characters : H i ! G F G U s e r .**
```