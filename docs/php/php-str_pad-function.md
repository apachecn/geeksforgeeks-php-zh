# PHP|str_pad()函数

> Original: [https://www.geeksforgeeks.org/php-str_pad-function/](https://www.geeksforgeeks.org/php-str_pad-function/)

Str_pad()函数是 PHP 中的内置函数，用于将字符串填充到给定长度。 我们可以用任何其他字符串填充输入字符串，直到指定的长度。 如果我们没有将另一个字符串传递给 str_pad()函数，那么输入字符串将用空格填充。

**语法：**

```
*string* str_pad($string, $length, $pad_string, $pad_type)
```

**参数**：此函数接受四个参数，如上面的语法所示，其中前两个参数是强制提供的，其余两个参数是可选的。 所有这些参数如下所述：

*   **$string：**此参数是必需的。 它指定需要填充的输入字符串。
*   **$Length：**此参数也是必需的。 它指定填充输入字符串*$STRING*后将生成的新字符串的长度。 如果该长度小于或等于输入字符串的长度，则不会进行填充。
*   **$PAD_STRING：**此参数是可选的，其默认值为空格‘’。 它指定要用于填充的字符串。
*   **$PAD_TYPE：**此参数也是可选的。 它指定字符串的哪一侧需要填充，即左侧、右侧或两者都填充。 默认情况下，它的值设置为 STR_PAD_RIGHT。 如果希望填充输入字符串的左侧，则应将该参数设置为 STR_PAD_LEFT，如果希望填充两侧，则应将该参数设置为 STR_PAD_BOTH。

**返回值**：此参数返回填充输入字符串*$string*后获得的新字符串。

例如：

```
Input : $string = "Hello World", $length = 20, 
        $pad_string = "."
Output : Hello World........

Input : $string = "Geeks for geeks", $length = 18,
        $pad_string = ")"
Output : Geeks for geeks)))

```

下面的程序演示了 PHP 中的 str_pad()函数：

**程序 1**：在此程序中，通过将最后一个参数设置为*STR_PAD_BOTHY*，我们将填充到输入字符串的两侧。 如果填充长度不是偶数，则右侧获得额外的填充。

```
<?php
   $str = "Geeks for geeks";
   echo str_pad($str, 21, ":-)", STR_PAD_BOTH); 
?>
```

产出：

```
:-)Geeks for geeks:-)

```

**程序 2**：在此程序中，通过将最后一个参数设置为*STR_PAD_LEFT*，我们将填充到输入字符串的左侧。

```
<?php
   $str = "Geeks for geeks";
   echo str_pad($str, 25, "Contribute", STR_PAD_LEFT); 
?>
```

产出：

```
ContributeGeeks for geeks

```

**程序 3**：在此程序中，通过将最后一个参数设置为*STR_PAD_RIGHT*，我们将填充到输入字符串的右侧。

```
<?php
   $str = "Geeks for geeks";
   echo str_pad($str, 26, " Contribute", STR_PAD_RIGHT); 
?>
```

产出：

```
Geeks for geeks Contribute

```

**参考**：
[http://php.net/manual/en/function.str-pad.php](http://php.net/manual/en/function.str-pad.php)