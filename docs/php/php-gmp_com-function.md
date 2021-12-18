# PHP|gmp_com()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_com-function/](https://www.geeksforgeeks.org/php-gmp_com-function/)

Gmp_com()是 PHP 中的一个内置函数，用于计算 GMP 数字的**个一的补码**([GNU Multiple Precision：for Large 数字](https://en.wikipedia.org/wiki/GNU_Multiple_Precision_Arithmetic_Library))。

**语法：**

```
gmp_com($num)
```

**参数：**此函数接受 GMP 编号*$num*作为强制参数，如上面的语法所示。 在 PHP 5.6 版和更高版本中，该参数可以是 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。

**返回值：**此函数返回一个 GMP 编号，它是作为参数传递给它的 GMP 编号的补码。

例如：

```
Input : gmp_com("1235")
Output : -1236

Input : gmp_com("1234")
Output : -1235

```

以下程序说明了 PHP 中的 gmp_com()函数：

**程序 1：**当作为 GMP 编号的数字字符串作为参数传递时，计算 GMP 编号的补码的程序。

```
<?php
// PHP program to calculate the one's complement
// of a GMP number passed as arguments 

// strings as GMP numbers 
$num = "1345";

// calculate the one's complement of a GMP number
$res = gmp_com($num);

echo $res;

?>
```

产出：

```
-1346

```

**程序 2：**当 GMP 编号作为参数传递时，计算 GMP 编号的补码的程序。

```
<?php
// PHP program to calculate the one's complement
// of a GMP number passed as arguments 

// creating GMP numbers using gmp_init()
$num = gmp_init(132);

// calculate the one's complement of a GMP number
$res = gmp_com($num);

echo $res;

?>
```

产出：

```
-133

```

**引用：**
[http://php.net/manual/en/function.gmp-com.php](http://php.net/manual/en/function.gmp-com.php)