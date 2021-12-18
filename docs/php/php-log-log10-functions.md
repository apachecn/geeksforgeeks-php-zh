# PHP|log()、log10()函数

> Original: [https://www.geeksforgeeks.org/php-log-log10-functions/](https://www.geeksforgeeks.org/php-log-log10-functions/)

对数是对幂运算的计数器运算。 一个数的对数实际上是另一个数的指数，即必须将底数提高才能产生该数。 如果欧拉数‘e’被用作任何对数运算的底，那么它就被称为自然对数运算，另一个流行的对数运算是以 10 为底。

在 PHP 中，如果没有指定底数，那么 log()函数用于计算数字的自然对数，log10()函数用于计算数字的以 10 为底的对数。

**log()函数**

**语法：**

```
*float* log ($arg, $base)

```

**参数**：函数最多可以接受两个参数，如下：

*   $arg：这是必需的参数，指的是要计算对数的个数。
*   $BASE：这是一个可选参数，引用对数运算的底。 如果没有给定，则使用 M_E，即欧拉数作为基数来计算自然对数。

**返回类型**：此函数返回对数运算的结果。

例如：

```
Input :  $arg = M_E * M_E;
Output : 2

Input : $arg = 1024;
        $base = 2;
Output : 10    

```

下面的程序演示了 log()在 PHP 中的工作原理：

```
<?php
// PHP code to illustrate the working of log() Function 
$arg = 81;
$base = 3;
for(;$base<=$arg;$base*=$base)
  echo 'log('.$arg.', '.$base.') = '.log($arg, $base)."\n";
?>
```

产出：

```
log(81, 3) = 4
log(81, 9) = 2
log(81, 81) = 1

```

**log10()函数**

**语法：**

```
*float* log10 ($arg)

```

**参数**：该函数接受单个参数$arg，该参数表示要计算其对数的数字。

**返回类型**：此函数返回以 10 为底的对数运算的结果。

例如：

```
Input :  $arg = 100;
Output : 2

Input : $arg = 10000;
        $base = 4;
Output : 10    

```

下面的程序演示了 PHP 中 log10()的工作原理：

```
<?php
// PHP code to illustrate the working of log10() Function 
$arg = 100000;
for(;$arg>=10;$arg/=10)
  echo 'log10('.$arg.') = '.log10($arg)."\n";
?>
```

产出：

```
log10(100000) = 5
log10(10000) = 4
log10(1000) = 3
log10(100) = 2
log10(10) = 1

```

**需要注意的重要事项**：

*   Log()函数是一种非常流行的计算对数值的方法。
*   [PHP|exp()函数](https://www.geeksforgeeks.org/php-exp-function/)是 log()的函数对应。