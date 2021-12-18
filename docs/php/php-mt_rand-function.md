# PHP|mt_rand()函数

> Original: [https://www.geeksforgeeks.org/php-mt_rand-function/](https://www.geeksforgeeks.org/php-mt_rand-function/)

在使用算法时，我们经常会遇到需要生成随机整数的情况。 生成随机数最常见的方法是使用 Mersenne Twister。
Mersenne Twister 是一种伪随机数发生器，它的名字来源于它的周期长度被选为 Mersenne 素数的事实。 它是第一个提供高质量伪随机整数快速生成的伪随机数生成器。 它是专门为纠正旧的伪随机数生成器中发现的大多数缺陷而设计的。
所以在 PHP 中，有一个内置的函数 mt_rand()，它基于 Mersenne Twister，帮助生成随机数。

*mt_rand()*函数在指定的最小值和最大值之间生成一个随机整数。 它会产生更好的随机值，并且比 rand()函数更快。 您还可以参考关于[PHP|rand()函数](https://www.geeksforgeeks.org/php-rand-function/)的文章，它是 PHP 中用于生成随机数的另一个内置函数。

**语法：**

```php
*int* mt_rand($min, $max)
```

**参数：**此函数接受两个参数，如下所述：

1.  **$min**：可选参数。 指定要返回的最小数字，默认值为 0。
2.  **$max**：可选参数。 它指定要返回的最高数字。

**返回值：**返回一个介于 min(或 0)和 max 之间的随机数，返回类型为整型。

例如：

```php
Input : mt_rand()
Output : 34567

Input : mt_rand(15, 50)
Output : 49

```

以下程序说明了 mt_rand()在 PHP 中的工作方式：

**程序 1：**

```php
<?php

echo mt_rand();

?>
```

产出：

```php
34567
```

**程序 2：**

```php
<?php

echo mt_rand(15, 50);

?>
```

产出：

```php
49
```

**需要注意的重要事项：**

*   Mt_rand()函数使用 Mersenne Twister 算法生成一个随机整数。
*   它会产生更好的随机值，并且比 rand()函数更快。

**参考**：
[http://php.net/manual/en/function.mt-rand.php](http://php.net/manual/en/function.mt-rand.php)