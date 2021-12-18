# PHP 中如何获取两个字符之间的字符串？

> 原文:[https://www . geesforgeks . org/如何获取 php 中两个字符之间的字符串/](https://www.geeksforgeeks.org/how-to-get-string-between-two-characters-in-php/)

字符串是在 PHP 中以增量形式存储的字符序列。一组字符，一个或多个可以位于字符串的任意两个选定索引之间。PHP 中两个字符之间的文本可以使用以下两种方法提取:

**方法 1:使用** [**substr()方法**](https://www.geeksforgeeks.org/php-substr-function/)**:**substr()方法用于检索原始字符串的子字符串。它将开始和结束索引作为索引，并提取位于索引之间的字符串部分。为了从开头检索子字符串，起始索引被选择为 0。

```
substr(string, startIndex, lengthStr)
```

**参数:**

*   **字符串:**在这个参数中，我们传递原始字符串或者需要剪切或者修改的字符串。这是一个强制参数。
*   **startIndex:** 指需要提取零件的原始字符串的位置。在这里，我们传递一个整数。如果整数是正数，它指的是字符串中从开始的位置的开始。如果整数是负的，那么它指的是从字符串末尾开始的位置。这也是一个强制参数。
*   **lengthStr:** 是整数类型的可选参数。它指的是字符串中需要从原始字符串中剪切的部分的长度。如果整数为正数，则表示从 start_position 开始，从开始提取长度。如果整数是负的，那么它指的是从 start_position 开始，并从字符串的末尾提取长度。如果未传递此参数，substr()函数将返回从 start_position 开始直到字符串结束的字符串。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declaring a string variable
$str = "Hi! This is geeksforgeeks";
echo("Original String : ");
echo($str . "\n");

$final_str = substr($str, 4, 7);

echo("Modified String : ");
echo($final_str);
?>
```

**Output**

```
Original String : Hi! This is geeksforgeeks
Modified String : This is
```

**方法 2:使用 for 循环和** [**str_split()方法**](https://www.geeksforgeeks.org/php-str_split-function/)**:**str _ split()方法用于将指定的字符串拆分成数组，在数组中元素被映射到它们对应的索引。数组的索引从 0 开始。

```
array_split( string )
```

在数组长度上执行循环迭代。每次执行迭代时，都会检查索引是否位于开始索引和结束索引之间。如果在范围内，则提取字符。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Declaring a string variable
$str = "Hi! This is geeksforgeeks";
echo("Original String : ");
echo($str . "\n");

// Define the start index
$start = 5;

// Define the end index
$end = 8;
$arr = str_split($str);

echo("Modified String : ");

for($i = 0; $i < sizeof($arr); $i++) {
    if($i >= $start && $i <= $end) {
        print($arr[$i]);
    }
}
?>
```

**Output**

```
Original String : Hi! This is geeksforgeeks
Modified String : his 
```