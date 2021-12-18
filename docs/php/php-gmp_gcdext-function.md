# PHP|gmp_gcdext()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_gcdext-function/](https://www.geeksforgeeks.org/php-gmp_gcdext-function/)

Gmp_gcdext()是 PHP 中的一个内置函数，它计算给定方程的 GCD(最大公约数)和乘数，使得*a*x+b*y=gcd(a，b)*，其中 gcd 是最大公约数。
此函数用于求解两个变量的线性[丢番图方程](https://en.wikipedia.org/wiki/Diophantine_equation)。

**语法：**

```
array gmp_gcdext ( GMP $a, GMP $b )

```

**参数：**gmp_gcdext()函数接受上述两个参数，如下所述：

*   ***$a*：**此参数可以是 PHP5.5 及更早版本中的 GMP 资源，也可以是 PHP5.6 中的 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。
*   ***$b*：**此参数可以是 PHP5.5 及更早版本中的 GMP 资源，也可以是 PHP5.6 中的 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数将返回 GMP 数字数组([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：对于大数)，即乘数(给定公式的 x 和 y)和 GCD。

**示例：**

```
Input: a = 12  ,  b = 21
       equation = 12 * x + 21 * y = 3
Output:  

Input: a = 5  ,  b = 10
       equation = 5 * x + 10 * y = 5
Output: x = 1  ,  y = 0  ,  GCD(12,21) = 5

```

下面的程序演示了 gmp_gcdext()函数：

```
<?php
// PHP code to solve a Diophantine equation 

// Solve the equation a*x + b*y = g
// where a =, b =, g = gcd(5, 6) = 1
$a = gmp_init(5);
$b = gmp_init(6);

// calculates gcd of two gmp numbers
$g = gmp_gcd($a, $b); 

$r = gmp_gcdext($a, $b);

$check_gcd = (gmp_strval($g) == gmp_strval($r['g'])); 
$eq_res = gmp_add(gmp_mul($a, $r['s']), gmp_mul($b, $r['t']));
$check_res = (gmp_strval($g) == gmp_strval($eq_res));

if ($check_gcd && $check_res) {

    $fmt = "Solution: %d * %d + %d * %d = %d\n";
    printf($fmt, gmp_strval($a), gmp_strval($r['s']), gmp_strval($b),
    gmp_strval($r['t']), gmp_strval($r['g']));
} 
else
    echo "Error generated\n";
?>
```

发帖主题：Re：Колибри0.7.0

```
Solution: 5 * -1 + 6 * 1 = 1

```

**引用：**[http://php.net/manual/en/function.gmp-gcdext.php](http://php.net/manual/en/function.gmp-gcdext.php)