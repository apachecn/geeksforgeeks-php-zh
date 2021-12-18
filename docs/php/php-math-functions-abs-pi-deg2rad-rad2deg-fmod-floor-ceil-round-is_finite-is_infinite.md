# PHP 数学函数(abs，pi，des2rad，rad2deg，fmod，loor，ceil，round，is_finite，is_infinite)

> Original: [https://www.geeksforgeeks.org/php-math-functions-abs-pi-deg2rad-rad2deg-fmod-floor-ceil-round-is_finite-is_infinite/](https://www.geeksforgeeks.org/php-math-functions-abs-pi-deg2rad-rad2deg-fmod-floor-ceil-round-is_finite-is_infinite/)

如您所知，PHP 是一种服务器端脚本语言，用于创建动态网页。 PHP 提供了许多内置的数学函数，这些函数有助于在处理数学数据时执行几个操作。 它对数学处理有很好的支持。 使用这些功能不需要安装。

PHP 中的一些数学函数示例如下：

1.**abs()：**
此函数将负值作为输入，返回整数或浮点数的绝对值(正值)。

**语法：**

```php
abs(number);
```

在此函数中，‘number’可以是浮点型，也可以是整型。

**示例：**

```php
<?php
// PHP code to return absolute value.
function absolute($degree)
{
    return (abs($degree));
}

// Driver Code
$number = -8.4;
echo(absolute($number));
?>
```

发帖主题：Re：Kolibrios

```php
8.4

```

2.**pi()：**
此函数返回 pi 的值。 命名常量 M_Pi 与 pi()相同。

**语法：**

```php
pi();
```

**示例：**

```php
<?php
# PHP function to convert degree to radian value.
echo(pi());
?>
```

发帖主题：Re：Kolibrios

```php
3.1415926535898

```

3.**dec2rad()：**
此函数接受度数值作为输入，并将其转换为弧度值。

**语法：**

```php
deg2rad(number);
```

**示例：**

```php
<?php
// PHP code to convert degree to radian value.
function deg_radian($degree)
{
    return (deg2rad($degree));
}

// Driver Code
$number = 180;
echo(deg_radian($number));
?>
```

发帖主题：Re：Kolibrios

```php
3.1415926535898

```

4.**rad2deg()：**
此函数接受弧度值作为输入，并将其转换为度数值。

**语法：**

```php
rad2deg(number);
```

**示例：**

```php
<?php
// PHP function to convert degree to radian value.
echo(rad2deg(pi()));
?>
```

发帖主题：Re：Kolibrios

```php
180

```

5.**fmod()：**
此函数接受两个参数作为输入，返回参数除法的浮点余数(模)。

**语法：**

```php
fmod(x, y);
```

这里，**x**是被除数，**y**是除数。 余数(R)定义为：对于某个整数 i，x=i*y+r。如果 y 不为零，则 r 与 x 符号相同，且幅度小于 y 的幅度。

**示例：**

```php
<?php
// PHP code to find modulo of x / y
function result($x, $y)
{
    return fmod($x, $y);
}

// Driver function
$x = 5.7;
$y = 1.3;
echo(result($x, $y));
?>
```

发帖主题：Re：Kolibrios

```php
0.5

```

这里，$r 等于 0.5，因为 4*1.3+0.5=5.7(x=i*y+r)

6.**Floor()：**
此函数以数值作为参数，必要时通过四舍五入返回下一个最小的整数值(浮点数)。
**语法：**

```php
floor($number);
```

**示例：**

```php
<?php
echo(floor(0.60)."\n");
echo(floor(5)."\n");
echo(floor(-5.9));
?>
```

发帖主题：Re：Kolibrios

```php
0
5
-6

```

7.**ceil()：**
此函数以数值作为参数，必要时通过向上舍入返回下一个最高整数值。

**语法：**

```php
ceil($number);
```

**示例：**

```php
<?php
echo(ceil(0.60)."\n");
echo(ceil(-5.9));
?>
```

发帖主题：Re：Kolibrios

```php
1
-5

```

8.**round()：**
此函数以数值作为参数，必要时通过向上舍入返回下一个最高整数值。

**语法：**

```php
round(number, precision, mode);
```

其中，**Number**指定要舍入的值，**Precision**指定要舍入到的小数位数(默认值为 0)，**MODE(可选)**指定以下常量之一以指定舍入发生的模式：

*   **PHP_ROUND_HARM_UP：**(默认设置)将数字向上舍入到精度小数，当它是精度小数的一半时。 1.5 到 2 和-1.5 到-2 的舍入
*   **PHP_ROUND_HARM_DOWN：**将数字向下舍入到小数点后的精度位，如果是半舍五入。 1.5 到 1 和-1.5 到-1 的舍入
*   **PHP_ROUND_HAME_EVEN：**将数字舍入到下一个偶数值的精度小数位。
*   **PHP_ROUND_Half_ODD：**将数字舍入到下一个奇数值的精确小数位。

**示例：**

```php
<?php
echo(round(1.95583, 2)."\n");
echo(round(1241757, -3)."\n");
echo(round(9.5, 0, PHP_ROUND_HALF_UP)."\n");
echo(round(9.5, 0, PHP_ROUND_HALF_DOWN)."\n");
echo(round(9.5, 0, PHP_ROUND_HALF_EVEN)."\n");
echo round(9.5, 0, PHP_ROUND_HALF_ODD);
?>
```

发帖主题：Re：Kolibrios

```php
1.96
1242000
10
9
10
9

```

9.**is_finite()：**
此函数接受任意值作为参数，并检查某个值是否有限。 如果指定值是有限数，则返回 True(1)，否则返回 False/Nothing。
如果该值在此平台上 PHP 浮点数的允许范围内，则该值是合法的限定值。

**语法：**

```php
is_finite(value);
```

**示例：**

```php
<?php
echo is_finite(234)."\n";
echo is_finite(log(0));
?>
```

发帖主题：Re：Kolibrios

```php
1

```

10.**IS_INFINITE()：**
此函数接受任意值作为参数，并检查某个值是否为无穷大。 如果指定的值是无穷大，则返回 TRUE(1)，否则返回 FALSE/Nothing。
如果该值超出此平台上 PHP 浮点数的允许范围，则该值是合法的无限大小。

**语法：**

```php
is_infinite(value);
```

**示例：**

```php
<?php
echo is_infinite(234)."\n";
echo is_infinite(log(0));
?>
```

发帖主题：Re：Kolibrios

```php
1
```