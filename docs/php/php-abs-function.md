# PHP | abs()函数

> 原文:[https://www.geeksforgeeks.org/php-abs-function/](https://www.geeksforgeeks.org/php-abs-function/)

**abs()函数**是 PHP 中的一个内置函数，用来返回一个数字的绝对(正)值。PHP 中的 abs()函数和我们数学中所说的模数是一样的。负数的模或绝对值是正数。

**语法:**

```php
*number* abs( value )
```

**参数:**ABS()函数接受单个参数**值**，该值保存您想要查找其绝对值的数字。

**返回值:**返回作为参数传递给它的数字的绝对值。

示例:

```php
Input : abs(6)
Output : 6

Input : abs(-6)
Output : 6

Input : abs(6.4)
Output : 6.4

Input : abs(-6.4)
Output : 6.4

```

下面的程序说明了 PHP 中的 abs()函数:

**程序 1:** 当一个正数作为参数传递时:

```php
<?php

echo (abs(6);

?>      
```

**输出:**

```php
6
```

**程序 2:** 当负数作为参数传递时:

```php
<?php

echo (abs(-6);

?>
```

**输出:**

```php
6
```

**程序 3:** 当一个带小数位的正数作为参数传递时:

```php
<?php

echo (abs(6.4);

?>      
```

**输出:**

```php
6.4
```

**程序 4:** 当一个带小数位的负数作为参数传递时:

```php
<?php

echo (abs(-6.4);

?>      
```

**输出:**

```php
6.4
```

**参考:**T2】http://php.net/manual/en/function.abs.php