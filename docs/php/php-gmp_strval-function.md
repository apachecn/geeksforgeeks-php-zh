# PHP|gmp_strval()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_strval-function/](https://www.geeksforgeeks.org/php-gmp_strval-function/)

Gmp_strval()是 PHP 中的一个内置函数，它返回 GMP 编号的字符串值。 ([GNU Multiple Precision](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)：适用于大数)。

**语法：**

```php
string gmp_strval ( GMP $num, int $base )
```

**参数：**该函数接受两个参数$num 和$base，如下所示。

1.  **$num-**该函数接受一个 GMP 编号*$num*并返回其字符串值。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。
2.  **$base-**此参数指定函数返回的数字的基数。 **$base**的基值是从 2 到 62 和-2 到-36。 这是一个可选参数，默认值为 10。

**返回值：**此函数返回给定 GMP 编号*$num*的字符串值。

例如：

```php
Input : $num = "110" $base = 2 
Output : 6

Input : $num = "110" 
Output :  110

```

以下程序说明了**gmp_strval()**函数：

**程序 1：**下面的程序演示了当数字字符串作为参数传递且缺少第二个参数时，gmp_strval()函数的工作原理。

```php
<?php
// PHP program to demonstrate the gmp_strval() function

// when the argument is numeric string and 
// the second parameter is missing
echo gmp_strval("10");  
?>
```

产出：

```php
10
```

**程序 2：**下面的程序演示了当数字字符串作为参数传递并且存在第二个参数时，gmp_strval()函数的工作原理。

```php
<?php
// PHP program to demonstrate the gmp_strval() function

// when the argument is numeric string and 
// the second parameter is present 

echo gmp_strval("10", 2);  
?>
```

产出：

```php
1010
```

**程序 3：**下面的程序演示了当传递 GMP 编号且没有第二个参数时，gmp_strval()函数的工作原理。

```php
<?php
// PHP program to demonstrate the gmp_strval() function

// when the argument is GMP number and 
// the second parameter is missing 

$num = gmp_init("101", 2);

//// gmp_strval converts GMP number to string 
// representation in given base(default 10).
echo gmp_strval($num);   
?>
```

产出：

```php
5
```

**程序 4：**下面的程序演示了当 GMP 编号作为参数传递且存在第二个参数时，gmp_strval()函数的工作原理。

```php
<?php
// PHP program to demonstrate the gmp_strval() function

// when the argument is numeric string and 
// the second parameter is present 
$num = gmp_init("1010", 2);  

// GMP number in base 8
echo gmp_strval($num, 8);  
?>
```

产出：

```php
12
```

**引用：**
[http://php.net/manual/en/function.gmp-strval.php](http://php.net/manual/en/function.gmp-strval.php)；