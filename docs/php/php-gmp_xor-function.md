# PHP|gmp_xor()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_xor-function/](https://www.geeksforgeeks.org/php-gmp_xor-function/)

**gmp_xor()**是 PHP 中的一个内置函数，用于计算 2 个 GMP 数字的 XOR([GNU Multiple Precision：](http://https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library)表示大数)。

**语法：**

```php
gmp_xor( $num1, $num2 )
```

**参数：**此函数接受两个 GMP 编号*$num1*和*$num2*作为上述语法中显示的强制参数。 这些参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回一个正 GMP 数，它是$num1 和$num2 的[XOR](http://php.net/manual/en/class.gmp.php)。

**示例：**

```php
Input : $num1 = "3" $num2 = "5"
Output : 6

Input : $num1 = 1 $num2 = 1
Output : 0 

```

以下程序说明了 gmp_xor()函数：

**程序 1：**当作为 GMP 编号的数字字符串作为参数传递时，该程序计算两个数字的异或。

```php
<?php
// PHP program to calculate the XOR 
// of two numbers using gmp_xor() 

// numeric string passed as arguments 
$xor = gmp_xor("3", "5"); 

// prints the GMP number which xor 
// of two numeric strings 
echo $xor;

?>
```

产出：

```php
6

```

**程序 2：**当 GMP 编号作为参数传递时，该程序计算两个数字的异或。

```php
<?php
// PHP program to calculate XOR 
// of two numbers 

// GMP numbers passed as arguments 
$xor1 = gmp_init("1101101110", 2);
$xor2 = gmp_init("0110011001", 2);

// function calculates the XOR of two numbers 
$xor3 = gmp_xor($xor1, $xor2);

// prints the GMP number which is the 
// XOR of two GMP numbers 
// gmp_strval Convert GMP number to string
//  representation in given base(default 10).
echo gmp_strval($xor3, 2);
?>
```

产出：

```php
1011110111

```

**引用：**
[http://php.net/manual/en/function.gmp-xor.php](http://php.net/manual/en/function.gmp-xor.php)