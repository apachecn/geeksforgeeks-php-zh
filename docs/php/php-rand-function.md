# PHP rand()函数

> Original: [https://www.geeksforgeeks.org/php-rand-function/](https://www.geeksforgeeks.org/php-rand-function/)

在本文中，我们将了解如何使用 PHP 中的 rand()函数获取随机数，并通过示例了解其实现。 Rand()是 PHP 中的一个内置函数，用于生成随机数，即，它可以生成范围为[min，max]的随机整数值。

**语法：**

```
rand();
```

函数的作用是：生成一个随机整数。 要生成某个范围内的随机整数，请执行以下操作：

**语法：**

```
rand(min,max);
```

**参数值：**

*   **min**：这是一个可选参数，指定将返回的最低值。 默认值为 0。
*   **max**：可选参数，指定要返回的最大值。 默认值为 getrandmax()。

**返回值：**此函数将返回从 min 到 getrandmax()的随机整数值，包括最大值。

**注意：**如果未指定最小值和最大值，则默认值分别为 0 和 getrandmax()。

**示例：**在本例中，我们将使用 rand()函数，该函数将返回一个介于 0 和 getrandmax()之间的随机整数。 兰德(15，35)将返回范围[15，35]内的随机整数。

## PHP

```
<?php
      // Generating a random number
      $randomNumber = rand();
      print_r($randomNumber);
      print_r("\n");

      // Generating a random number in a
      // Specified range.
      $randomNumber = rand(15,35);
      print_r($randomNumber);
?>
```

**注意：**代码的输出可能在每次运行时发生变化。 因此，输出可能与指定的输出不匹配。

发帖主题：Re：Колибри0.7.8.0