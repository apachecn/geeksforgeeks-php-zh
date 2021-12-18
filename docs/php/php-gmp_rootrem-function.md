# PHP|gmp_rootrem()函数

> Original: [https://www.geeksforgeeks.org/php-gmp_rootrem-function/](https://www.geeksforgeeks.org/php-gmp_rootrem-function/)

gmp_rootrem()是 PHP 中的一个内置函数，用于计算 GMP 数的 n 次方根(GNU 多精度：对于大数)，并返回 n 次方根的整数部分及其余数。

**语法：**

```php
gmp_rootrem($num,$n)
```

**参数：**此函数接受两个必选参数，如上面的语法所示。 具体如下：

*   **$num：**该参数可以是 PHP 5.6 版和更高版本中的 GMP 对象，也可以传递数字字符串，前提是可以将该字符串转换为数字。
*   **$n：**要计算的**$num**的正根。

**示例：**

```php
Input : $num = "8" $n = 2
Output :  Array ( 
                    [0] => GMP Object ( [num] => 2 )
                    [1] => GMP Object ( [num] => 4 )
                   )

Input : $num = "9" $n = 2
Output : Array ( 
                  [0] => GMP Object ( [num] => 3 )
                  [1] => GMP Object ( [num] => 0 ) 
              )

```

**返回值：**此函数返回一个两个元素的数组，两个元素都是 GMP 编号。

*   数组的**第一个元素**是$num 的第 n 个根的**整数部分**。
*   **第二个元素**是**余数**。

下面的程序将演示如何在 PHP 中使用 gmp_rootrem()函数：

**程序 1：**下面的程序说明了将 GMP 编号作为参数传递的函数的用法。

```php
<?php
// PHP program to calculate the 
// integer part and remainder  
// of nth root of a gmp number

// GMP number as arguments 
$num = gmp_init(8); 
$n = 3;

$rootrem = gmp_rootrem($num, $n);  

//Display the array elements
echo print_r($rootrem);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array
(
    [0] => GMP Object ( [num] => 2 )
    [1] => GMP Object ( [num] => 0 )
)
```

**程序 2：**下面的程序说明了将数字字符串作为参数传递的函数的用法。

```php
<?php
// PHP program to calculate the 
// integer part and remainder  
// of nth root of a gmp number

// Numeric string as argument 
$num = "178924890"; 
$n = 3;

$rootrem = gmp_rootrem($num, $n);  

//Display the array elements
echo print_r($rootrem);
?>
```

发帖主题：Re：Колибри0.7.0

```php
Array (
 [0] => GMP Object ( [num] => 563 ) 
[1] => GMP Object ( [num] => 471343 )  
)
```

**参考：**http://php.net/manual/en/function.gmp-rootrem.php