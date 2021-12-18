# PHP mb_str_plit()函数

> Original: [https://www.geeksforgeeks.org/php-mb_str_split-function/](https://www.geeksforgeeks.org/php-mb_str_split-function/)

Mb_str_plit()函数是在 PHP 版本 7.4.0 中引入的，只有等于或高于 7.4.0 的 PHP 版本才支持该函数。 函数的作用是：替代 str_plit()函数。 它用于拆分具有指定块长度的给定字符串，成功时返回数组，失败时返回 False，但在 PHP 8 中，失败时不返回 False。

**语法：**

```
*array* mb_str_split(*string* $string, *int* $length, *string* $encoding)
```

**参数：**

<figure class="table">

| ***名称*** | ***类型*** | ***描述*** |
| $STRING | String [T28 . To split a string into blocks, it is required. |
| $Length | 集成 | The length of the substring to split the string. Optional parameters. |
| $coding | String | The encoding format to apply to the substring. Optional parameter, default is NULL. |

</figure>

**示例 1：**在下面的示例中，单词**“Awese”**正在使用 mb_str_plit()函数进行拆分，由于此函数返回一个字符数组 print_r()，因此已使用它来打印输出。

## PHP

```
<?php

print_r(mb_str_split("Awesome"));
?>
```

发帖主题：Re：Колибри0.7.8.0

**示例 2：**在下面的示例中，创建了两个变量$STUMENT 和$WORD。 $senance 用于存储任何字符串类型的随机语句，而$word 用于存储 mb_str_plit()返回的数组。 该代码的基本思想是将“GeeksforGeek”从存储在$语句中的句子中分离出来。 这里，mb_str_plit()用于分隔指定长度的子字符串，数组存储在$word 中，并相应地显示结果。

## PHP

```
<?php

$sentence = "GeeksforGeeks is Awesome";

$word = mb_str_split($sentence,13);
echo $word[0];

?>
```

发帖主题：Re：Колибри0.7.8.0

**引用：**[https://www.php.net/manual/en/function.mb-str-split.php](https://www.php.net/manual/en/function.mb-str-split.php)