# PHP|sqrt()函数

> Original: [https://www.geeksforgeeks.org/php-sqrt-function/](https://www.geeksforgeeks.org/php-sqrt-function/)

很多时候，在求解数学表达式时，我们需要计算一个数的平方根。像其他编程语言一样，为了解决这个问题，PHP 提供了一个内置函数*sqrt()*，它可以用来计算一个数的平方根。 PHP 中的*sqrt()*函数用于计算一个数的平方根。
我们已经在文章[PHP|数学函数](https://www.geeksforgeeks.org/php-math-functions-is_nan-pow-sqrt-exp-log-log10-log1p-max-min-getrandmax-rand-mt_rand/)中简要讨论了 sqrt()函数。 在本文中，我们将详细了解 sqrt()函数。

**语法：**

```php
*float* sqrt(value)

```

**参数：**此函数接受单个参数*$value*。 这是你想知道其平方根的数字。

**返回值：**它返回一个浮点值，它是传递给它的参数*$value*的平方根。

**示例：**

```php
Input : sqrt(25) 
Output : 5

Input : sqrt(-25) 
Output : NaN

Input : sqrt(0.09) 
Output :0.3

Input : sqrt(0)
Output : 0

```

下面的程序说明了 sqrt()在 PHP 中的工作方式：

*   将正数作为参数传递时：

## PHP

```php
<?php

echo(sqrt(25));

?>
```

**输出：**

```php
5

```

*   当负数作为参数传递时：

## PHP

```php
<?php

echo(sqrt(-25));

?>
```

发帖主题：Re：Колибри0.7.0

```php
NaN

```

*   将带有小数位的数字作为参数传递时：

## PHP

```php
<?php

echo(sqrt(0.09));

?>
```

**输出：**

```php
0.3

```

*   当零作为参数传递时：

## PHP

```php
<?php

echo(sqrt(0));

?>
```

发帖主题：Re：Колибри0.7.0

```php
0

```

**重要注意事项：**

*   Sqrt()函数用于计算数字的平方根。
*   它比一般的平方根计算方法效率高得多。
*   精度取决于用户的精度指令。

**参考**：
[http://php.net/manual/en/function.sqrt.php](http://php.net/manual/en/function.sqrt.php)