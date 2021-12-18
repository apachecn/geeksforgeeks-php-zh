# PHP|strchr()函数

> Original: [https://www.geeksforgeeks.org/php-strchr-function/](https://www.geeksforgeeks.org/php-strchr-function/)

**strchr()**函数是 PHP 中的一个内置函数，用于在另一个字符串(比如*OriginalStr*)中搜索给定字符串(比如*searchStr*)的第一个匹配项，并从*OrignalStr*中第一个匹配项*searchStr*开始返回*OriginalStr*中的其余字符串。

**注意：**strchr()函数区分大小写。

**语法：**

```
strchr($originalStr, $searchStr, $before_search

```

**参数：**

*   **$OriginalStr**：此参数指定要在其中搜索单词的字符串。 这是必填项
*   **$searchStr**：它指定要在给定的$OriginalStr 中搜索的单词，它可以是字符或数字，如果传递了数字，它还会在$OriginalStr 中搜索等效的 ASCII 值字符。 这是强制性的。
*   **$BEFORE_SEARCH：**这是一个可选参数，当设置为 True 时，它将返回第一次出现$searchStr 之前的$OriginalStr 部分。 默认情况下，它设置为**False**。

**返回值：**根据以下三种情况返回字符串：

*   当找到$searchStr 时，它返回从第一个$searchStr 出现在$OriginalStr 中到$OriginalStr 末尾的字符串。
*   当$searchStr 不存在于给定的$OriginalStr 中时，它不返回任何内容。
*   当**$BEFORE_SEARCH**设置为 TRUE 时，它返回第一次出现$searchStr 之前的字符串部分。

**示例：**

```
Input : $originalStr = "geeks for geeks" 
        $searchStr = "geeks" 
Output : geeks for geeks 

Input : $originalStr = "geeks for geeks" 
        $searchStr = "for" 
Output : for geeks 

Input : $originalStr = "striver has published 180 articles"
        $searchStr = "has"    $before_search = TRUE
Output :  striver

Input: $originalStr = "geeks for geeks" $searchStr = "gfg" 
Output: No output 

```

下面的程序演示了 PHP 中的 strchr()函数：

**程序 1：**当找到单词时演示 strchr()函数的程序。

## PHP

```
<?php
// Program to demonstrate the strchr()
// function when word is found
$originalStr = "geeks for geeks";
$searchStr = "geeks" ;

// prints the string from the
// first occurrence of the $searchStr
echo strchr($originalStr, $searchStr);
?>
```

**输出：**

```
geeks for geeks

```

**程序 2：**当找不到单词时演示 strchr()函数的程序。

## PHP

```
<?php
// Program to demonstrate the strchr()
// function when word is not found
$originalStr = "geeks for geeks";
$searchStr = "gfg" ;

// prints the string from the
// first occurrence of the $searchStr
echo strchr($originalStr, $searchStr);
?>
```

**输出：**

```
No Output

```

**程序 3：**当找到单词且$BEFORE_SEARCH 设置为 TRUE 时，演示 strchr()函数的程序。

## PHP

```
<?php
// Program to demonstrate the strchr()
// function when word is found and
// $before_search is set to true
$originalStr = "geeks for geeks";
$searchStr = "for" ;

// prints the string from the
// first occurrence of the word
echo strchr($originalStr, $searchStr, true);
?>
```

**输出：**

```
geeks

```

**程序 4：**当传递并找到单词的一部分时，演示 strchr()函数的程序。

## PHP

```
<?php
// Program to demonstrate the strchr()
// function when a part of word is passed and found
$originalStr = "geeks for geeks";
$searchStr = "eks" ;

// prints the string from the
// first occurrence of the word
echo strchr($originalStr, $searchStr);
?>
```

**输出：**

```
eks for geeks

```

**程序 5：**当传递数字并搜索其等效的 ASCII 字符时，演示 strchr()函数的程序。

## PHP

```
<?php
// Program to demonstrate the strchr()
// function when a number is passed and its equivalent
// ASCII character is searched

$originalStr = "geeks for geeks";

// 101 is the ASCII value of e
$searchStr = 101 ;

echo strchr($originalStr, $searchStr);
?>
```

发帖主题：Re：Колибри0.7.0

```
eeks for geeks

```

**参考**：
[http://php.net/manual/en/function.strchr.php](http://php.net/manual/en/function.strchr.php)