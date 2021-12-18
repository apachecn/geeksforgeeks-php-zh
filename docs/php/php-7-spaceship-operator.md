# PHP 7 |宇宙飞船操作员

> 原文:[https://www.geeksforgeeks.org/php-7-spaceship-operator/](https://www.geeksforgeeks.org/php-7-spaceship-operator/)

这篇文章会让你意识到一个非常有用的操作符，也就是飞船操作符 PHP 7。宇宙飞船运算符或组合比较运算符用“< = >”表示。这是一个三向比较运算符，它可以在两个操作数之间执行大于、小于和等于的比较。
该运算符具有类似的行为，如 [strcmp()](https://www.geeksforgeeks.org/strcmp-in-c-cpp/) 或 version_compare()。该运算符可用于整数、浮点、字符串、数组、对象等。
**该< = >运算符提供组合比较:= >**

*   如果两边的值相等，则返回 0
*   如果左边的值大于 1，则返回 1
*   如果右边的值更大，则返回-1

**例**:

```
 // Comparing Integers

echo 1 <=> 1; // outputs 0
echo 3 <=> 4; // outputs -1
echo 4 <=> 3; // outputs 1

// String Comparison

echo "a" <=> "a"; // outputs 0 
echo "m" <=> "y"; // outputs -1
echo "y" <=> "c"; // outputs 1
=>=>=>=>=>=>
```

```
<?php
echo"Integers \n";
echo 7 <=> 7 ;
echo"\n";
echo 7 <=> 6;
echo"\n";
echo 6 <=> 7;

echo"\nFloat\n";

echo 2.5 <=> 1.5; 
echo"\n";
echo 0.5 <=> 1.5; 
echo"\n";
echo 1.5 <=> 1.5; 

echo"\nStrings\n";
echo "a" <=> "a" ;
echo"\n";
echo "g" <=> "b" ; 
echo"\n";
echo "a" <=> "b" ; 

echo"\nArrays\n";
echo [] <=> []; 
echo"\n";
echo [1, 7, 3] <=> [1, 7, 3];
echo"\n";
echo [1, 7, 3, 5] <=> [1, 7, 3];
echo"\n";
echo [1, 7, 3] <=> [4, 4, 4];
echo"\n";

?>
```

**输出**:

```
Integers 
0
1
-1
Float
1
-1
0
Strings
0
1
-1
Arrays
0
0
1
-1

```

**参考**:[http://php.net/manual/en/language.operators.comparison.php](http://php.net/manual/en/language.operators.comparison.php)

=>