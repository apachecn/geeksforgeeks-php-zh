# 如何处理 PHP 中 file_get_contents()函数的警告？

> 原文:[https://www . geesforgeks . org/如何处理文件警告 _ get _ contents-function-in-PHP/](https://www.geeksforgeeks.org/how-to-handle-the-warning-of-file_get_contents-function-in-php/)

PHP 中的 [**file_get_contents()函数**](https://www.geeksforgeeks.org/php-file_get_contents-function/) 是一个内置函数，用于将文件读入字符串。该函数使用服务器支持的内存映射技术，因此提高了性能，使其成为读取文件内容的首选方式。
要读取的文件的路径作为参数发送给函数，成功时返回读取的数据，失败时返回 FALSE。

**返回值:**成功返回读取数据，失败返回 FALSE。

**错误和异常:**

*   如果要打开特殊字符的文件，比如空格，需要先使用 [urlencode()](https://www.geeksforgeeks.org/php-urlencode-function/) 进行编码。
*   [file_get_contents()函数](https://www.geeksforgeeks.org/php-file_get_contents-function/)返回布尔值 FALSE，但也可能返回计算结果为 FALSE 的非布尔值。
*   如果找不到文件名，最大长度小于零，或者如果在流中查找指定的偏移量失败，则会生成 E_WARNING 级别的错误。

**示例:**

```
Input:  file_get_contents('https://www.geeksforgeeks.org/');
Output: A computer science portal for geeks

Input:  file_get_contents('gfg.txt', FALSE, NULL, 0, 14);
Output: A computer science portal for geeks
```

**程序 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Reading contents from the
// GeeksforGeeks homepage
$homepage = file_get_contents(
      "https://www.geeksforgeeks.org/");
echo $homepage;

?>
```

**运行时错误:**

> PHP 警告:file _ get _ contents():PHP _ network _ getaddress:getaddrinfo 失败:在/home/3d 11 f 9784 b 99 e2c 83058d 5842d 5533 ce . PHP 第 5 行
> PHP 警告:file _ get _ contents(https://www . geeksforgeks . org/)中出现系统错误:无法打开流:PHP _ network _ getaddress:getaddrinfo 失败:在/home/3d 11 f 97844 中出现系统错误

**输出:**

```
It will redirect to GeeksforGeeks Home Page
```

**程序 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Reading 36 bytes starting from
// the 0th character of gfg.txt
$text = file_get_contents('gfg.txt',
                  FALSE, NULL, 0, 36);
echo $text;

?>
```

**运行时错误:**

> PHP 警告:file _ get _ contents():PHP _ network _ getaddress:getaddinfo 失败:在/home/4659 aeca 06 fdba 457 da 0 C5 d 78 befb 39a . PHP 第 6 行
> PHP 警告:file_get_contents(gfg.txt):无法打开流:在/home/4659 aeca 06 fdba 457 da 0 C5 d 78 befb 39a . PHP 第 6 行没有这样的文件或目录

**输出:**

```
It will display the content of gfg.txt file.
For Example: A computer science portal for geeks
```

我们可以清楚地看到，上面 PHP 警告表单中的运行时错误已经发生，这确实是意想不到的。这里出现了消除这些错误的问题，有办法处理这些错误吗？
是的，PHP 为我们提供了一个简单的解决方案。

PHP 支持一个错误控制操作符:符号(@)。在 PHP 中添加到表达式之前，该表达式可能生成的任何错误消息都将被忽略。因此，只需在函数调用 *file_get_contents()* 之前插入错误控制运算符(@)就可以抑制上述 PHP Warning，方法如下:

**更新程序 1:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Reading contents from the
// GeeksforGeeks homepage
$homepage = @file_get_contents(
      "https://www.geeksforgeeks.org/");
echo $homepage;

?>
```

**输出:**

```
It will redirect to GeeksforGeeks Home Page
```

**更新程序 2:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Reading 36 bytes starting from
// the 0th character from gfg.txt
$text = @file_get_contents('gfg.txt',
                  FALSE, NULL, 0, 36);
echo $text;

?>
```

**输出:**

```
It will display the content of gfg.txt file.
For Example: A computer science portal for geeks
```

所以，在添加 **'@'** 符号之后，我们可以看到所有那些 PHP 警告都被抑制了，只有输出显示如上。
**参考:**[https://www . PHP . net/manual/en/language . operators . error control . PHP](https://www.php.net/manual/en/language.operators.errorcontrol.php)