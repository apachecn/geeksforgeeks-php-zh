# PHP|fmod()函数

> Original: [https://www.geeksforgeeks.org/php-fmod-function/](https://www.geeksforgeeks.org/php-fmod-function/)

Fmod 代表浮动模数。 模计算除法的剩余部分，通常用‘%’符号表示。 然而，一般的模表达式要求除数和被除数都是整数类型，这对如此重要的运算是一个很大的限制。

在 PHP 中，fmod()函数用于计算任何除法的模数，这些除法可能同时包含浮点数作为被除数和除数。

**语法：**

```php
*float* fmod ($dividend, $divisor)

```

**参数**：该函数有两个参数，如下所示：

*   $DYARY：此参数接受一个要除以的浮点数。
*   $ditor：此参数接受一个浮点数，该浮点数将用作除数。

**返回类型**：此函数返回除法的浮点余数。

例如：

```php
Input :  $dividend = 2.7,  $divisor = 1.3;   
Output : 0.1

Input : $dividend = -2.7,  $divisor = 1.1; 
Output : -0.5        

```

下面的程序演示了 fmod()在 PHP 中的工作方式：

```php
<?php

// PHP code to illustrate the 
// working of fmod() Function 

$dividend = 2.5;
$divisor = 1.1;

for(;$divisor<1.25;$divisor+=0.05)
    echo $dividend.' % '.$divisor.' = '.
          fmod($dividend, $divisor)."\n";

?>
```

产出：

```php
2.5 % 1.1 = 0.3
2.5 % 1.15 = 0.2
2.5 % 1.2 = 0.1

```

**需要注意的重要事项**：

*   Fmod()函数返回浮点模数。
*   Fmod()是一种近似方法，可能并不总是返回准确的结果。

**参考**：
[http://php.net/manual/en/function.fmod.php](http://php.net/manual/en/function.fmod.php)