# PHP|substr()函数

> Original: [https://www.geeksforgeeks.org/php-substr-function/](https://www.geeksforgeeks.org/php-substr-function/)

Substr()是 PHP 中的一个内置函数，用于提取字符串的一部分。

**语法：**

```php
substr(string_name, start_position, string_length_to_cut)
```

**参数**：
substr()函数允许 3 个参数或参数，其中两个是必需的，一个是可选的。

1.  **STRING_NAME：**在此参数中，我们传递原始字符串或需要剪切或修改的字符串。 这是必选参数
2.  **START_POSITION：**这是指需要提取零件的原始字符串的位置。 在这里，我们传递一个整数。 如果整数为正，则表示字符串中的位置从开头开始。 如果整数为负，则它指的是从字符串末尾开始的位置。 这也是必选参数。
3.  **STRING_LENGTH_TO_CUT：**此参数是可选的，类型为整数。 这指的是需要从原始字符串中剪切的字符串部分的长度。 如果整数为正，则表示从 start_position 开始，并从开头提取长度。 如果整数为负，则引用从 start_position 开始并从字符串末尾提取长度。 如果没有传递此参数，则 substr()函数将返回从 START_POSITION 到 STRING 结尾的字符串。

**return Type**：
如果成功，则返回字符串的提取部分，否则返回 false，否则返回空字符串。

下面是一个演示在 PHP 中使用 substr()的程序：

```php
<?php

// PHP program to illustrate substr()
function Substring($str){
    $len = strlen($str);
    echo substr($str, 8), "\n";
    echo substr($str, 5, $len), "\n";
    echo substr($str, -5, 10), "\n";
    echo substr($str,-8, -5), "\n";
}

// Driver Code
$str="GeeksforGeeks";
Substring($str);

?>
```

产出：

```php
Geeks
forGeeks
Geeks
for

```