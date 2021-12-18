# 如何用 PHP 脚本显示文本？

> 原文:[https://www . geesforgeks . org/如何用 php 脚本显示文本/](https://www.geeksforgeeks.org/how-to-display-text-with-a-php-script/)

PHP 允许我们使用各种内置方法以各种格式显示文本。

**使用 echo 命令:**echo 命令可用于显示文本，包括数字、字符串和数组。

**例 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$string = "GeeksforGeeks!!";

// Printing the string directly
echo ("Printing the string: ");

// Printing the variable
echo $string;
?>
```

**输出**

```php
Printing the string: GeeksforGeeks!!
```

**例 2:** 数组不能直接打印到脚本中。它兼容显示以字符串格式存储的数据。因此，json_encode()方法用于模拟数组到字符串的转换。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Declaring an array
$arr = array(1, 2, 3, 4, 5);
echo('Array : ');

// Printing array
echo(json_encode($arr));

?>
```

**输出**

```php
Array : [1, 2, 3, 4, 5]
```

**使用 print 命令:**PHP 中 print 函数的运行时间略多于 echo 函数。
T3】例 1:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

$string = "GeeksforGeeks!!";

// Printing the string directly
print("Printing the string: ");

// Printing the variable
print $string;
?>
```

**输出**

```php
Printing the string: GeeksforGeeks!!
```

**示例 2:** 可以使用 print_r 方法打印数组，该方法用于打印索引及其值。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// Declaring an array
$arr = array(1, 2, 3, 4, 5);
echo('Array : ');

// Printing array
print_r($arr);
?>
```

**输出**

```php
Array : Array ( [0] => 1 [1] => 2 [2] => 3 [3] => 4 [4] => 5 )
```