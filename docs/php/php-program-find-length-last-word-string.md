# 查找字符串

中最后一个单词的长度的 PHP 程序

> Original: [https://www.geeksforgeeks.org/php-program-find-length-last-word-string/](https://www.geeksforgeeks.org/php-program-find-length-last-word-string/)

我们得到一个字符串。 我们需要用 PHP 编写一个程序，使用内置函数查找字符串中最后一个单词的长度。
我们已经在这里讨论了解决该问题的方法[。 本文讨论该问题的 PHP 解决方案。](https://www.geeksforgeeks.org/length-of-last-word-in-a-string/)

例如：

```
Input : "php exercises" 
Output : 9

Input : "geeks for geeks"
Output : 5

```

**我们主要使用 PHP 内置的这三个函数来解决这个问题：**

*   [**substr()函数**](https://www.geeksforgeeks.org/php-substr-function/)：PHP 中的这个内置函数用于提取字符串的一部分。
*   [**strrpos()函数**](https://www.geeksforgeeks.org/php-strrpos-strripos-functions/)：PHP 中的这个内置函数用于查找字符串在原始字符串或另一个字符串中的最后位置。 它返回与字符串最后一次出现的位置相对应的整数值，并且唯一地处理大写和小写字符。
*   [**strlen()函数**](https://www.geeksforgeeks.org/php-string-functions/)：PHP 中的这个内置函数用于查找字符串的长度。

使用上面提到的内置函数解决这个问题的想法是，首先使用 strpos()函数查找字符串中最后出现的空格的位置。 在获得最后出现的空格的位置之后，我们可以使用 substr()函数轻松地获得字符串中的最后一个单词，并将其存储在一个新的字符串变量中。 最后，我们可以使用 strlen()函数来查找字符串中最后一个单词的长度。

```
<?php
// PHP code to find the length of last word
// in a string

    // function to find length of last word
    function length_last_word($string)
    {   
        // position of last occurring space
        // in the string
        $pos = strrpos($string, ' ');

        // if the string has only one word
        if(!$pos)
        {
            $pos = 0;
        }
        else
        {
            $pos = $pos + 1;
        }

        // get the last word in the string
        $lastWord = substr($string,$pos);

        // return length of last word 
        return strlen($lastWord);
    }

    // Driver Code
    print_r(length_last_word('geeksforgeeks')."\n");
    print_r(length_last_word('computer science portal')."\n");

?>
```

产出：

```
13
6

```