# PHP 中字符串操作的 split()和 explode()函数的区别

> 原文:[https://www . geeksforgeeks . org/split-and-exploit-functions-for-string-operation-in-PHP/](https://www.geeksforgeeks.org/difference-between-split-and-explode-functions-for-string-manipulation-in-php/)

在本文中，我们将看到 PHP 中用于字符串操作的 split()和 explode()函数之间的区别。split()和 explode()函数在基本 PHP 中可用，用于执行字符串操作和转换。

**split()函数:**PHP 中的 split()函数用于将输入字符串分隔成不同的元素。元素根据字符串中模式的出现情况进行划分。可选参数描述了划分数组的元素数量。它从字符串的左边到右边开始。方法返回一个数组。

```
array split (string pattern, string string [, int limit])
```

**参数:**

*   **模式–**断开字符串的分隔符。
*   **弦–**要分成几部分的弦。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$str = "Geeks_for_geeks_is_fun!";
$arr = split("\_", $str);
print("String components : ");
print_r($arr);
?>
```

**输出**

```
String components : Array ( 
    [0] => Geeks 
    [1] => for 
    [2] => geeks 
    [3] => is 
    [4] => fun! 
)
```

[**【explode()】函数**](https://www.geeksforgeeks.org/php-explode-function/)**:**PHP 中的 explode()函数用于根据指定的分隔符将字符串划分为数组组件。limit 参数指示要将数组分成的部分的数量。此方法返回一个索引数组，其索引映射到数组元素。

```
explode(separator, string, limit)
```

**参数:**

*   **分隔符–**分隔符断开字符串。
*   **弦–**要分成几部分的弦。
*   **限制–**将数组分成多个部分的数组元素数量的指示符。
    *   **大于 0–**返回一个数组，该数组最多包含个限制元素
    *   **小于 0–**返回除最后一个*–*极限元素()以外的数组
    *   **等于 0–**返回包含一个元素的数组

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$str = "Geeks for geeks is fun!";
$arr = explode(" ", $str);
print("String components : ");
print_r($arr);

?>
```

**Output**

```
String components : Array
(
    [0] => Geeks
    [1] => for
    [2] => geeks
    [3] => is
    [4] => fun!
)

```

下面的代码片段将字符串分成单个数组组件:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$str = "Geeks for geeks is fun!";
$arr = explode(" ", $str, 0);
print("String components : ");
print_r($arr);
?>
```

**Output**

```
String components : Array
(
    [0] => Geeks for geeks is fun!
)

```

下面的代码片段指出了小于 1 的最后一个参数的用法:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
$str = "Geeks for geeks is fun!";
$arr = explode(" ", $str, -1);
print("String components : ");
print_r($arr);
?>
```

**Output**

```
String components : Array
(
    [0] => Geeks
    [1] => for
    [2] => geeks
    [3] => is
)

```

<figure class="table">

| **拆分()功能** | **爆炸()功能** |
| 使用模式分割字符串。 | 使用字符串分隔符分隔字符串。 |
| 更多的执行时间。 | 至少是执行时间。 |
| 基于正则表达式匹配字符串。 | 与基于正则表达式的字符串不匹配。 |
| 从 PHP 5.3 开始已弃用 | 仍在使用。 |

</figure>