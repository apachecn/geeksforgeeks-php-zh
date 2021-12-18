# PHP|erg_place()函数

> Original: [https://www.geeksforgeeks.org/php-ereg_replace-function/](https://www.geeksforgeeks.org/php-ereg_replace-function/)

*ERG_REPLACE()*是 PHP 中的内置函数，用于在其他字符串中搜索字符串模式。 如果在原始字符串中找到模式，则它将用替换字符串替换匹配的文本。 您可以参考关于[正则表达式](https://www.geeksforgeeks.org/write-regular-expressions/)的文章，了解使用正则表达式进行模式匹配的基本知识。

**语法：**

```
*string* ereg_replace ( $string_pattern, $replace_string,  $original_string )

```

**使用的参数：**此函数接受三个必选参数，所有这些参数如下所述。

*   ***$STRING_Pattern*：**此参数指定要在$Original_STRING 中搜索的模式。 它既可以与数组一起使用，也可以与带圆括号的子字符串类型一起使用。
*   ***$REPLACE_STRING*：**此参数指定将替换匹配文本的字符串，它可以与数组和字符串类型一起使用。 替换包含\digit 形式的子字符串，它替换匹配数字的带圆括号的子字符串的文本，并\0 生成整个内容字符串。
*   ***$Original_STRING*：**此参数指定输入字符串，可以是数组类型和字符串类型。

**返回值：**如果找到匹配的字符串或数组，此函数将返回修改后的字符串或数组。 如果与原始字符串不匹配，则它将返回未更改的原始字符串或数组。

**注意：**在 PHP 中，*erg_place()*函数是*区分大小写的*。 此函数在 PHP 5.3.0 中已被*弃用*，在 PHP 7.0.0 中删除了。

示例：

```
Input: $original_string = "Geeksforgeeks PHP article."; 
       $string_pattern = "(.*)PHP(.*)"; 
       $replace_string = " You should read \\1all\\2"; 
Output: You should read Geeksforgeeks all article.
Explanation: Within the parenthesis "\1" and "\2" to access
             the part of string and replace with 'PHP' to 'all'.

Input: $original_string = "Geeksforgeeks is no:one computer 
                                             science portal.";
       $replace_string = '1'; 
       $original_string = ereg_replace('one', $replace_string,
                                             $original_string);
Output: Geeksforgeeks is no:1 computer science portal. 

```

下面的程序说明了*ERG_REPLACE()*函数。

**程序 1：**

```
<?php 

// Original input string 
$original_string = "Write any topic .";

// Pattern to be searched
$string_pattern = "(.*)any(.*)"; 

// Replace string
$replace_string = " own yours own \\1biography\\2"; 

echo ereg_replace($patternstrVal, $replacesstrVal, $stringVal); 

?>
```

帖子主题：Re：Колибри

**注：**当使用整数值作为替换参数时，由于函数将数字解释为字符的序数值，因此不会得到预期的结果。

**程序 2：**

```
<?php 

// Original input string 
$original_string = "India To Become World's Fifth
                        Largest Economy In 2018.";

// Replace string
$replace_string = 5; 

// This function call will not show the expected output as the
// function interpret the number to ordinal value of character.
echo ereg_replace('Fifth',$replace_string, $original_string);

$original_string = "India To Become World's Fifth
                         Largest Economy In 2018.";

// Replace String
$replace_string = '5'; 

// This function call will show 
// the correct expected output
echo ereg_replace('Fifth',$replace_string, $original_string);

?> 
```

帖子主题：Re：Колибри

**参考**：[http://php.net/manual/en/function.ereg-replace.php](http://php.net/manual/en/function.ereg-replace.php)