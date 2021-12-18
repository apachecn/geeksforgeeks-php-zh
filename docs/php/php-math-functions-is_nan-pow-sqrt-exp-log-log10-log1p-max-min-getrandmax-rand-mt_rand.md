# PHP 数学函数(is_nan、power、sqrt、exp、log、log10、log1p、max、min、getrandmax、rand、mt_rand)

> Original: [https://www.geeksforgeeks.org/php-math-functions-is_nan-pow-sqrt-exp-log-log10-log1p-max-min-getrandmax-rand-mt_rand/](https://www.geeksforgeeks.org/php-math-functions-is_nan-pow-sqrt-exp-log-log10-log1p-max-min-getrandmax-rand-mt_rand/)

11.**is_nan()：**
此函数接受任何值作为参数，并检查值是否为 Number。 如果指定的值不是数字，则返回 True(1)，否则返回 False/Nothing。

**语法：**

```php
is_nan(value);
```

**示例：**

```php
<?php
echo is_nan(234) . "\n";
echo is_nan(asin(1.1)) ;
?>
```

发帖主题：Re：Kolibrios

```php
1

```

**注意：**(IS_FINITED(值))等同于(！IS_INFINITE(值)&&(！IS_NAN(值))，即一个数字只能是 FINDITED、INFINITE 和 NAN(不是数字)中的一个。 您不需要同时检查 IS_INFINITE()和 IS_NaN()来查看数字是否无效或超出范围。

12.**power()：**
此函数将 base 和指数作为参数，并返回 base 的指数幂。
**语法：**

```php
pow(base,exponent);
```

**示例：**

```php
<?php
echo(pow(2,4) . "\n");
echo(pow(-2,-4));
?>
```

发帖主题：Re：Kolibrios

```php
16
0.0625

```

13.**sqrt()：**
此函数以数值为参数，返回值的平方根。
**语法：**

```php
sqrt(number);
```

**示例：**

```php
<?php
echo(sqrt(9) . "\n");
echo(sqrt(0.64));
?>
```

发帖主题：Re：Kolibrios

```php
3
0.8

```

14.**exp()：**
该函数返回 e 的 x 次方。‘e’是自然对数系统的底(大约 2.718282)，x 是传递给它的数。
**语法：**

```php
exp(x);
```

**示例：**

```php
<?php
# PHP code to calculate exponent of e.
function exponent($number){
    return (exp($number));
}

// Driver Code
$number = 0;
echo (exponent($number));
?>
```

发帖主题：Re：Kolibrios

```php
1

```

15.**log()：**
此函数接受任何数字和底数作为参数，并返回数字的自然对数或以底数为底的数字的对数。

**语法：**

```php
log(number, base);
```

其中，**数字**指定要计算对数的值。
**base(可选)**指定要使用的对数底(默认值为‘e’)。

**示例：**

```php
<?php
echo(log(5.987) . "\n");
echo(log(1));
?>
```

发帖主题：Re：Kolibrios

```php
1.7895904519432
0

```

16.**log10()：**
此函数接受任何数字作为参数，并返回一个数字的以 10 为底的对数。

**语法：**

```php
log10(number);
```

这里，**数字**指定要计算对数的值。

**示例：**

```php
<?php
echo(log10(5.987) . "\n");
echo(log10(0));
?>
```

发帖主题：Re：Kolibrios

```php
0.77720925814568
-INF

```

17.**log1p()：**
此函数接受任何数字作为参数，并返回 log(1+number)，即使在 number 的值接近于零的情况下，其计算方式也是准确的。

**语法：**

```php
log1p(number);
```

这里，**数字**指定要处理的数字。

**示例：**

```php
<?php
echo(log1p(5.987) . "\n");
echo(log1p(0));
?>
```

发帖主题：Re：Kolibrios

```php
1.9440512795703
0

```

18.**max()：**
在此函数中，如果第一个也是唯一一个参数是数组，max()将返回该数组中的最高值。 如果至少提供了两个参数，max()将返回这些值中最大的一个。

**语法：**

```php
max(array_values);
or
max(value1,value2,...);
```

**示例：**

```php
<?php
echo(max(3,4,6,12,10) . "\n");
echo(max(array(48,76,83,22)));
?>
```

发帖主题：Re：Kolibrios

```php
12
83

```

19.**min()：**
在此函数中，如果第一个也是唯一一个参数是数组，min()将返回该数组中的最低值。 如果至少提供了两个参数，min()将返回这些值中最小的一个。

**语法：**

```php
min(array_values);
or
min(value1,value2,...);
```

**示例：**

```php
<?php
echo(min(3,4,6,12,10) . "\n");
echo(min(array(48,76,83,22)));
?>
```

发帖主题：Re：Kolibrios

```php
3
22

```

20.**getrandmax()：**
此函数不接受任何参数，并返回 rand()函数可能返回的最大值。

**语法：**

```php
getrandmax();
```

**示例：**

```php
<?php
echo(getrandmax()); 
?>
```

发帖主题：Re：Kolibrios

```php
2147483647

```

21.。 **rand()：**
如果在不带可选 min 的情况下调用此函数，max 参数 rand()将返回一个介于 0 和 getrandmax()之间的伪随机整数。 如果您想要一个介于 12 和 56(包括 12 和 56)之间的随机数。 例如，使用 rand(12，56)。

**语法：**

```php
rand();
or
rand(min,max);
```

**示例：**
这里，**min**指定要返回的最小数字(默认值为 0)。
**max**指定要返回的最大数字(默认值为 getrandmax())

```php
<?php
echo(rand() . "\n");
echo(rand(12,100));
?>
```

发帖主题：Re：Kolibrios

```php
1135079733
76

```

输出可能会不时变化，因为它会生成随机数。

22.。 **mt_rand()：**
该函数是旧版 rand()的临时替代函数。 它使用具有已知特征的随机数生成器，该生成器使用**Mersenne Twister 算法**，生成随机数的速度比平均 rand()提供的随机数快四倍。
如果在没有可选 min 的情况下调用，max 参数 mt_rand()将返回一个介于 0 和 mt_getrandmax()之间的伪随机值。 例如，如果您想要一个介于 12 和 56(包括 12 和 56)之间的随机数，请使用 mt_rand(12，56)。

**语法：**

```php
mt_rand();
or
mt_rand(min,max);
```

**示例：**
这里，**min**指定要返回的最小数字(默认值为 0)。
**max**指定要返回的最大数字(默认值为 getrandmax())

```php
<?php
echo(mt_rand() . "\n");
echo(mt_rand(12,100));
?>
```

发帖主题：Re：Kolibrios

```php
952458556
87

```

输出可能会不时变化，因为它会生成随机数。