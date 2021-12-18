# PHP|lcg_value()函数

> Original: [https://www.geeksforgeeks.org/php-lcg_value-function/](https://www.geeksforgeeks.org/php-lcg_value-function/)

Lcg_value()函数是 PHP 中的一个内置函数，用于生成(0，1)范围内的伪随机数。

**语法：**

```php
lcg_value()
```

**使用的参数：**此函数不接受任何参数。

**返回值：**此函数返回 0 到 1 范围内的伪随机浮点值。

**错误和异常：**对于加密目的没有用处，因为此函数不会生成加密安全值。

下面的程序说明了 lcg_value()函数

**程序 1：**

```php
<?php
// PHP program to illustrate 
// lcg_value() function

//print the value in range between 0 and 1
echo lcg_value();

?>
```

**输出：**

```php
0.13542664978974

```

**程序 2：**函数每次打印不同的值，并返回值的类型。

```php
<?php
echo lcg_value(). "\n";
echo lcg_value(). "\n";
echo lcg_value(). "\n";
echo lcg_value(). "\n";
echo lcg_value(). "\n";
echo lcg_value(). "\n";

// for checking types 
// of return value
$x = lcg_value();

//print the type of value returned
echo gettype($x);
?>
```

**输出：**

```php
0.07786871705105
0.70944065438839
0.91109571202142
0.44844141753786
0.63726317430881
0.2004533497305
double

```