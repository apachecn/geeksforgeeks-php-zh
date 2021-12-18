# PHP | bcscale()函数

> 原文:[https://www.geeksforgeeks.org/php-bcscale-function/](https://www.geeksforgeeks.org/php-bcscale-function/)

bcscale()函数是 PHP 中的一个内置函数。它为所有 bc 数学函数调用设置默认比例参数。当我们在程序中调用函数 bcscale()时，在这个函数中传递的参数就变成了默认的比例因子，默认情况下是零。

**语法:**

```php
*int* bcscale($scale)
```

**参数:**该函数接受单个参数 **$scale** ，并且是 int 类型，是强制的。此参数告诉所有 bc 数学函数的函数调用结果中小数点后出现的位数。它的默认值为零。

**返回值:**该函数返回旧的刻度值。

下面的程序说明了 PHP 中的 bcscale()函数:

**程序 1:**

```php
<?php

// default scale : 3
bcscale(3);

// takes the default scale value as 3 
// which is declared at the beginning 
echo bcadd('111', '6.55957'), "\n"; // 16.007

// this is not the same without bcscale()
echo bcadd('111', '6.55957', 1), "\n"; // 16.007

//  takes the default scale value as 3 
// which is declared at the beginning 
echo bcadd('111', '6.55957'), "\n"; 
?>
```

输出:

```php
117.559 
117.5 
117.559

```

**程序 2:**

```php
<?php

// default scale : 3
bcscale(5);

// takes the default scale value as 3 
// which is declared at the beginning 
echo bcadd('111', '6.55957'), "\n"; // 16.007

// this is not the same without bcscale()
echo bcadd('111', '6.55957', 1), "\n"; // 16.007

// default scale value changes
bcscale(2); 

// takes the default scale value as 2
// which is declared 
echo bcadd('111', '6.55957'), "\n"; 
?>
```

输出:

```php
117.55957 
117.5 
117.55

```

**参考:**T2[http://php.net/manual/en/function.bcscale.php](http://php.net/manual/en/function.bcscale.php)