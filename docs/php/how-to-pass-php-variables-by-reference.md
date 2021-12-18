# 如何通过引用传递 PHP 变量？

> 原文:[https://www . geesforgeks . org/如何通过引用传递 php 变量/](https://www.geeksforgeeks.org/how-to-pass-php-variables-by-reference/)

默认情况下，PHP 变量在 PHP 中作为函数参数按值传递。当 PHP 中的变量通过值传递时，在函数级定义的变量的范围被绑定在函数的范围内。改变任何一个变量对任何一个变量都没有任何影响。

**示例:**

```php
<?php

// Function used for assigning new
// value to $string variable and 
// printing it
function print_string( $string ) {
    $string = "Function geeksforgeeks"."\n";

    // Print $string variable
    print($string);
}

// Driver code
$string = "Global geeksforgeeks"."\n";
print_string($string);
print($string);
?>
```

**Output:**

```php
Function geeksforgeeks
Global geeksforgeeks

```

**通过引用传递:**当变量通过引用传递时，使用&(和号)符号需要加在变量自变量之前。例如:函数(& $x)。全局变量和函数变量的范围都成为全局变量，因为这两个变量是由同一个引用定义的。因此，每当全局变量改变时，函数内部变量也会改变，反之亦然。

**示例:**

```php
<?php

// Function used for assigning new value to 
// $string variable and printing it
function print_string( &$string ) {

    $string = "Function geeksforgeeks \n";

    // Print $string variable
    print( $string );
}

// Driver code
$string = "Global geeksforgeeks \n";
print_string( $string );
print( $string );
?>
```

**Output:**

```php
Function geeksforgeeks 
Function geeksforgeeks

```