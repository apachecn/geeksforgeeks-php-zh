# PHP|变音位()函数

> Original: [https://www.geeksforgeeks.org/php-metaphone-function/](https://www.geeksforgeeks.org/php-metaphone-function/)

变音位()函数是 PHP 中的一个内置函数，用于计算给定字符串的[变音位键](https://en.wikipedia.org/wiki/Metaphone)。 变音位键是一种语音算法，用于根据单词的发音对单词进行索引。 它使用较大的一套英语发音规则。

**语法：**

```
string metaphone ( $str, $key )
```

**参数：**此函数接受上述两个参数，如下所述：

*   **$str：**必选参数，表示查找变音位密钥的字符串。
*   **$key：**可选参数，用于指定变音位密钥的最大长度。

**返回值：**以字符串形式返回变音键，失败时返回 false。

例如：

```
Input: $str = "Contribute Article on GeeksforGeeks"
Output: KNTRBTRTKLNJKSFRJKS

Input: $str = "Contribute Article on GeeksforGeeks"  $key = 5
Output: KNTRB

```

以下程序说明 PHP：
**程序 1：**中的变音位()函数

```
<?php
$str1 = "Contribute Article on GeeksforGeeks";
echo metaphone($str1) . "\n";

$str2 = "A computer science portal";
echo metaphone($str2);
?>
```

**Output:**

```
KNTRBTRTKLNJKSFRJKS
AKMPTRSNSPRTL

```

**程序 2：**

```
<?php
$str1 = "Contribute Article on GeeksforGeeks";
echo metaphone($str1, 6) . "\n";

$str2 = "A computer science portal";
echo metaphone($str2, 5);
?>
```

**Output:**

```
KNTRBT
AKMPT

```

**相关文章：**[PHP|Soundex()函数](https://www.geeksforgeeks.org/php-soundex-function/)

**引用：**[http://php.net/manual/en/function.metaphone.php](http://php.net/manual/en/function.metaphone.php)