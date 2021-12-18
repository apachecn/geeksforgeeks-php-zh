# PHP|substr_count()函数

> Original: [https://www.geeksforgeeks.org/php-substr_count-function/](https://www.geeksforgeeks.org/php-substr_count-function/)

**substr_count()**是 PHP 中的一个内置函数，用于计算子字符串在给定字符串中出现的次数。 该函数还为我们提供了在给定索引范围内搜索给定子字符串的选项。 区分大小写，即“abc”子串不在字符串“abcab”中。 如果为搜索指定的(Start+Length)值超过了传递的字符串的大小，它将向用户返回一条警告消息。

**语法：**

```
substr_count($string, $substring, $start, $length)
```

**参数**：该函数接受四个参数，如上述语法所示，如下所述。

1.  **$string**-传入参数的字符串是计算子字符串出现的字符串。 此参数是必须提供的。
2.  **$substring**-搜索参数中传递的子字符串是该字符串，并返回出现次数。 此参数是必须提供的。
3.  **$START**-此参数是可选的。 如果传递此参数，则从起始位置开始搜索，而不是在整个字符串中搜索子字符串的匹配项。
4.  **$LENGTH**-此参数是可选的。 该参数依赖于启动。 它将搜索操作从开始限制到开始+长度位置。 如果 start+length 的值增加了字符串的长度，则会生成一条警告消息

**返回值：**该函数在不同情况下可以返回不同的值，如下图所示。

*   如果未传递可选参数，则给定子字符串在字符串中出现的次数
*   传入 start 参数时，子字符串从开始位置到结束位置在字符串中出现的次数
*   传递 Start 和 Length 两个参数时，子字符串从 Start 到 Start+Length 位置在字符串中出现的次数。

**示例：**

```
Input: string= "geeks for geeks" substring="geeks" 
Output: 2
Explanation: "geeks" occurs two times in the given string 

Input: string= "geeks for geeks" substring="geeks" start=6 
Output: 1 
Explanation: "geeks" occurs one time in the given string, in 
this case search for substring starts from 6th position i.e., 
the substring is searched in "for geeks".  

```

以下程序说明 substr_count()函数：

**程序 1：**当两个可选参数均未传递时。

```
<?php
// PHP program to demonstrate the substr_count() function

$str = "geeks for geeks"; 

echo substr_count($str, "geeks");  // displays the count

?>
```

发帖主题：Re：Колибри0.7.0

```
2
```

**程序 2：**传递参数$start 时。

```
<?php
// PHP program to demonstrate the 
// substr_count() function

// $start is passed
$str = "geeks for geeks"; 

echo substr_count($str, "geeks", 6);  

?>
```

发帖主题：Re：Колибри0.7.0

```
1
```

**程序 3：**同时传递$start 和$length 时。

```
<?php
// PHP program to demonstrate the 
// substr_count() function 

$str = "geeks for geeks"; 

echo substr_count($str, "geeks", 6, 2);  

?>
```

发帖主题：Re：Колибри0.7.0

```
0
```

**程序 4：**当($START+$LENGTH)超过$STRING 长度时演示警告消息的程序。

```
<?php
// PHP program to demonstrate the 
// substr_count() function 

$str = "geeks for geeks"; 

// ($start + $length ) > length of $str
echo substr_count($str, "geeks", 6, 14); 

?>
```

发帖主题：Re：Колибри0.7.0

```
PHP Warning:  substr_count(): Length value 14 exceeds string length

```

**程序 5：**当 substr_count()不计算重叠的子字符串时，该程序演示 substr_count()。

```
<?php
// PHP program to demonstrate the 
// substr_count() function 

$str = "abcabcab"; 

echo substr_count($str, "abcab");  

?>
```

发帖主题：Re：Колибри0.7.0

```
1
```