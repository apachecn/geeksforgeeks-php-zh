# PHP | chunk_split()函数

> 原文:[https://www.geeksforgeeks.org/php-chunk_split-function/](https://www.geeksforgeeks.org/php-chunk_split-function/)

**chunk_split()** 函数是 PHP 中的内置函数。chunk_split()函数用于将字符串分割成特定长度的较小块。

**语法:**

```
*string* chunk_split($string, $length, $end)

```

**参数:**该函数接受三个参数，如上面的语法所示，描述如下:

1.  **$string** :此参数指定需要分块的字符串。
2.  **$length** :此参数指定一个整数，该整数指定块长度。这是分块部分的长度。
3.  **$end** :此参数指定行结束顺序。

**返回值:**该函数返回分割成小块的字符串。

**示例:**

```
Input : string = "geeksforgeeks" 
        length = 4
        end = "."
Output: Geek.sfor.Geek.s. 

Input: string = "Twinkle bajaj" 
       length = 2 
       end = "*" 
Output: Tw*in*kl*e *ba*ja*j* 

```

下面的程序说明了 PHP 中的 chunk_split()函数:

**程序 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to illustrate the 
// chunk_split function

$str = "Twinkle bajaj";
echo chunk_split($str, 2, "*");

?>
```

**输出:**

```
Tw*in*kl*e *ba*ja*j* 

```

**程序 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to illustrate the 
// chunk_split function

$str = "geeksforgeeks";

// Returns a string with a '.'
// placed after every four characters.
echo chunk_split($str, 4, ".");
?>
```

**输出:**

```
geek.sfor.geek.s. 

```

**程序 3:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to illustrate the 
// chunk_split function

$str = "abcd";
echo chunk_split($str, 4, "@@");
?>
```

**输出:**

```
abcd@@

```

**程序 4:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to illustrate the 
// chunk_split function

// If specified length is more than
// string length, then added at the
// end.
$str = "abcd";
echo chunk_split($str, 10, "@@");
?>
```

**输出:**

```
abcd@@

```

**参考:**T2[http://php.net/manual/en/function.chunk-split.php](http://php.net/manual/en/function.chunk-split.php)T5】