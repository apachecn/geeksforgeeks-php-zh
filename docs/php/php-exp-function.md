# PHP|exp()函数

> Original: [https://www.geeksforgeeks.org/php-exp-function/](https://www.geeksforgeeks.org/php-exp-function/)

欧拉数或俗称**e**是一个非常流行的无理数，它接近于 2.718281828，是最重要的数学常数之一。 **E**是自然对数系统的底数。 指数值被广泛应用于许多场合，如复利、伯努利试验、正态分布、微积分等。

函数的作用是：计算给定参数的幂*e*。

**语法：**

```php
*float* exp($power)

```

**参数**：该函数接受单个参数$power，该参数定义必须提升到的幂*e*。

**返回类型**：此函数以浮点数的形式返回 e 的值，该值是给定参数的幂。

例如：

```php
Input :  $power = 0;
Output : 1

Input : $power = 1;
Output : 2.718281828459        

```

下面的程序演示了 exp()在 PHP 中的工作方式：

```php
<?php

// PHP code to illustrate the working of exp() Function 
for($i=-2;$i<=2;$i++)
    echo 'e^'.$i.' = '.exp($i)."\n";

?>
```

产出：

```php
e^-2 = 0.13533528323661
e^-1 = 0.36787944117144
e^0 = 1
e^1 = 2.718281828459
e^2 = 7.3890560989307

```

**需要注意的重要事项**：

*   Exp()函数是一种非常流行的计算指数值的方法。
*   Log()函数是 exp()函数的对应函数。

**参考**：
[http://php.net/manual/en/function.exp.php](http://php.net/manual/en/function.exp.php)