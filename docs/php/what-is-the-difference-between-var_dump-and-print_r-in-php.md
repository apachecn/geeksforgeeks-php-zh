# PHP 中 var_dump()和 print_r()有什么区别？

> 原文:[https://www . geesforgeks . org/var _ dump-and-print _ r-in-PHP/](https://www.geeksforgeeks.org/what-is-the-difference-between-var_dump-and-print_r-in-php/)的区别是什么

在本文中，我们将讨论 PHP 中 [**var_dump()**](https://www.geeksforgeeks.org/php-var_dump-function/) 和 [**print_r()**](https://www.geeksforgeeks.org/php-print_r-function/) 函数的区别。

**var_dump()函数:****var _ dump()**函数用于转储关于变量的信息，该变量显示给定变量的类型和值等结构化信息。

**语法:**

```
void var_dump ($expression)
```

**参数:**

*   **$expression:** 可以是单个变量，也可以是包含任意类型的多个空格分隔变量的表达式。

**返回值:**该函数没有返回类型。

**示例:**演示 **var_dump()** 函数工作的 PHP 代码。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Using var_dump function on
// different data type variables
var_dump(var_dump(45, 62.1, TRUE, 
    "sravan", array(1, 2, 3, 4,5,6))
);

?>
```

**输出:**

```
int(45) float(62.1) bool(true) string(6) "sravan" array(6) 
{ [0]=> int(1) [1]=> int(2) [2]=> int(3) 
  [3]=> int(4) [4]=> int(5) [5]=> int(6) } NULL
```

**print_r()函数:****print _ r()**函数是 PHP 中的内置函数，用于打印变量中存储的信息。

**语法:**

```
print_r( $variable, $isStore )
```

**参数:**该函数接受两个参数，如上语法所示，如下所述。

*   **$变量:**该参数指定要打印的变量，是必选项。
*   **$isStore:** 这是可选参数。该参数为布尔类型，默认值为 FALSE，用于将 **print_r()** 函数的输出存储在变量中，而不是打印出来。如果该参数设置为真，那么**打印 _r()** 功能将返回它应该打印的输出。

**返回值:**如果*$变量*是整数、浮点数或字符串，则函数打印变量的值。如果变量是一个数组，函数以显示键和值的格式打印数组，类似的符号用于对象。如果参数 *$isStore* 设置为真，那么 **print_r()** 函数将返回一个字符串。

**示例:**使用 **print_r()** 函数显示所有数据类型变量的 PHP 代码。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

  // String variable
  $a = "Welcome to GeeksforGeeks";

  // Integer variable
  $b = 450;

  // Array variable
  $arr = array('0' => "Computer", 
               '1' => "science", 
               '2' => "portal");

  // Printing the variables
  print_r($a);
  echo"\n<br>";
  print_r($b);
  echo"\n<br>";
  print_r($arr);
?>
```

**输出:**

```
Welcome to GeeksforGeeks 
450
Array ( [0] => Computer [1] => science [2] => portal )
```

**var _ dump()和 print_r()函数的区别:**

<figure class="table">

| **var _ dump()** | **print _ r()** |
| --- | --- |
| Var _ dump () displays values and data types as output. | Print_r () only displays values as output. |
| It has no return type. | It will return a value in string format. |
| The data returned by this function is hard to understand. | The data returned by this function is human readable. |
| This function can be used for debugging purposes. | This function is used for database and web applications. |
| Var_dump () displays the number of elements in a variable. | Print_r () does not display the number of elements in a variable. |
| Var_dump () displays the length of the variable. | Print_r () does not display the length of the variable. |

</figure>