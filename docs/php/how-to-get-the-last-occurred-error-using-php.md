# 如何用 PHP 获取上次发生的错误？

> 原文:[https://www . geesforgeks . org/如何使用-php/](https://www.geeksforgeeks.org/how-to-get-the-last-occurred-error-using-php/) 获取最近发生的错误

使用 **error_get_last()** 函数很容易得到 PHP 中发生的最后一个错误的信息。我们可以获得关于错误的非常详细的信息，例如错误发生的文件和行号。

**语法:**

```
error_get_last();
```

**返回值:**

```
 (associative array | NULL)
```

上面返回的关联数组包含如下数据:

*   **Type:** Error type (error code)
*   **message:** error message
*   **File:** The path of the file where the error occurred.
*   **Line:** The line number where the error occurred in the above file.

**PHP 代码:**

## 【PHP】

```
<?php
  echo $var; // This line will throw error

  $error_info = error_get_last();

  print_r($error_info);
  echo '<br/>';
  print_r ($error_info['type']);
  echo '<br/>';
  print_r ($error_info['message']);
  echo '<br/>';
  print_r ($error_info['file']);
  echo '<br/>';
  print_r ($error_info['line']);
?>
```

**输出:**

```
Array ( 
    [type] => 8 
    [message] => Undefined variable: var 
    [file] => /home/nzH0BV/prog.php 
    [line] => 2 
)
8
Undefined variable: var
/home/nzH0BV/prog.php
2
```