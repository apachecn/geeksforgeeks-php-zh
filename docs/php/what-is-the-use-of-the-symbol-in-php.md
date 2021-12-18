# PHP 中的@符号有什么用？

> 原文:[https://www . geesforgeks . org/PHP 中符号的用途是什么/](https://www.geeksforgeeks.org/what-is-the-use-of-the-symbol-in-php/)

在 PHP 中，at 符号(@)用作错误控制运算符。当表达式前面带有@符号时，可能由该表达式生成的错误消息将被忽略。如果启用了 track_errors 功能，则由表达式生成的错误消息将保存在变量 *$php_errormsg* 中。该变量将在每个错误时被覆盖。

**节目 1:**

```
<?php

// File error 
$file_name = @file ('non_existent_file') or
    die ("Failed in opening the file: error: '$errormsg'");

// It is used for expression
$value = @$cache[$key];

// It will not display notice if the index $key doesn't exist.

?>
```

**运行时错误:**

```
PHP Notice:  Undefined variable: errormsg in /home/fe74424b34d1adf15aa38a0746a79bed.php on line 5
```

**输出:**

```
Failed in opening the file: error: ''
```

**程序 2:**

```
<?php

// Statement 1
$result= $hello['123']

// Statement 2
$result= @$hello['123']
?>
```

它将只执行语句 1 并显示通知消息

```
PHP Notice:  Undefined variable: hello.
```

**注意:**使用@是非常糟糕的编程实践，因为它没有使错误消失，它只是隐藏了它们，并且由于我们看不到我们的代码实际上有什么问题，它使调试变得更糟。

**参考:** [误差控制操作员](http://php.net/manual/en/language.operators.errorcontrol.php)