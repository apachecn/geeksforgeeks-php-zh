# PHP | addslashes()函数

> 原文:[https://www.geeksforgeeks.org/php-addslashes-function/](https://www.geeksforgeeks.org/php-addslashes-function/)

**addslashes()** 函数是 PHP 中的一个内置函数，它返回一个在预定义字符前带有反斜杠的字符串。它不接受参数中的任何指定字符。

预定义的字符有:

1.  单引号(')
2.  双引号(")
3.  反斜杠(\)
4.  空

**注意:**addslashes()函数不同于[addcs 睫毛()](https://www.geeksforgeeks.org/php-addcslashes-function/)函数接受指定的字符，在这些字符之前要添加斜线，但是 addslashes()函数不接受参数中的任何字符，而是在一些指定的字符之前添加斜线。

**语法:**

```
addslashes($string)

```

**参数:**addslashes()函数只接受一个参数 *$string* ，该参数指定需要转义的输入字符串。我们也可以说，这个参数指定了一个字符串，在这个字符串中，我们希望在预定义的字符之前添加反斜杠。

**返回值:**返回参数中传递的预定义字符前带反斜杠的转义字符串。

示例:

```
Input : $string = "Geek's"
Output : Geek\'s

Input : $string='twinkle loves "coding"'
Output : twinkle loves \"coding\"

```

下面的程序说明了 PHP 中的 addslashes()函数:

**程序 1:**

```
<?php
// PHP program to demonstrate the 
// working of addslashes() function 

// Input String
$str = addslashes('twinkle loves "coding"'); 

// prints the escaped string
echo($str); 
?>
```

**输出:**

```
twinkle loves \"coding\"

```

**程序 2:**

```
<?php 
// PHP program to demonstrate the
// working of addslashes() function 

// Input String
$str = addslashes("Geek's"); 

// prints the escaped string
echo($str); 
?>
```

**输出:**

```
Geek\'s
```

**参考**:
T3】http://php.net/manual/en/function.addslashes.php