# PHP|SIMILAR_TEXT()函数

> Original: [https://www.geeksforgeeks.org/php-similar_text-function/](https://www.geeksforgeeks.org/php-similar_text-function/)

similar_text()函数是 PHP 中的内置函数。 此函数计算两个字符串的相似度，并返回两个字符串中匹配的字符数。 该函数的操作方式是查找最长的第一个公共子字符串，并递归地对前缀和后缀重复此操作。 返回所有公共子字符串的长度总和。

它还可以计算两个字符串的相似度(以百分比表示)。 该函数通过将结果除以给定字符串的平均长度乘以 100 来计算相似度(以百分比表示)。

**语法：**

```
similar_text( $string1, $string2, $percent)
```

**参数：**此函数接受上述语法中所示的三个参数，其中前两个参数必须提供，最后一个参数是可选的。 所有这些参数如下所述：

*   **$STRIN1，$STRIN2：**这些强制参数指定要比较的两个字符串
*   **$Percent：**此参数是可选的。 它指定了一个变量名，用于存储以百分比表示的相似度。 通过将引用作为第三个参数传递，该函数将以百分比计算相似度。

**返回值：**它返回两个字符串之间匹配的字符数。

例如：

```
Input : $string1 = "code", $string2 = "coders"
Output : 4 (80 %)

Input : $string1 = "hackers", $string2 = "hackathons"
Output : 5 (58.823529411765 %)

```

以下程序说明了 similar_text()函数：

**程序 1：**

```
<?php

$sim = similar_text("hackers", "hackathons", $percent);

// To display the number of matching characters
echo "Number of similar characters : $sim\n";

// To display the percentage of matching characters
echo "Percentage of similar characters : $percent\n";

?>
```

输出

```
Number of similar characters : 5
Percentage of similar characters : 58.823529411765>

```

**程序 2：**此程序将突出显示函数的区分大小写。

```
<?php

$output = similar_text("geeks for geeks",
                 "Geeks for Geeks",  $percent);

// To display the number of matching characters
echo "Number of similar characters : $output\n";

// To display the percentage of matching characters
echo "Percentage of similar characters : $percent\n";

?>
```

产出：

```
Number of similar characters : 13
Percentage of similar characters : 86.666666666667

```

**程序 3：**传递字符串的顺序非常重要。 改变变量会产生不同的结果。

```
<?php

$output1 = similar_text("with mysql", "php is best");

// To display the number of matching characters
echo "Number of similar characters : $output1\n";

$output2 = similar_text( "php is best", "with mysql");

// To display the number of matching characters
echo "Number of similar characters : $output2\n";

?>
```

产出：

```
Number of similar characters : 2
Number of similar characters : 3

```

**参考**：
[http://php.net/manual/en/function.similar-text.php](http://php.net/manual/en/function.similar-text.php)