# PHP |数组()函数

> 原文:[https://www.geeksforgeeks.org/php-array-function/](https://www.geeksforgeeks.org/php-array-function/)

array()函数是 PHP 中的一个内置函数，用于创建一个数组。PHP 中有三种类型的数组:

*   **索引数组:**包含数值索引的数组。
    **语法:**

    ```php
    array( val1, val2, val3, ... )
    ```

*   **关联数组:**包含名称作为关键字的数组。
    **语法:**

    ```php
    array( key=>val, key=>val, key=>value, ... )
    ```

*   **多维数组:**包含一个或多个数组的数组。
    **语法:**

    ```php
    array( array( val11, val12, ...)
           array( val21, val22, ...)
           ... )
    ```

**参数:**该功能接受上面提到的和下面描述的两个大气参数:

*   **val:** 此参数用于保存数组的值。
*   **键:**该参数用于保存键值:

**返回值:**这个函数返回一个参数数组。

下面的程序说明了 PHP 中的 array()函数:

**程序 1:** 这个例子说明了索引数组。

```php
<?php

// Create an array
$sub = array("DBMS", "Algorithm", "C++", "JAVA");

// Find length of array
$len = count( $sub );

// Loop to print array elements
for( $i = 0; $i < $len; $i++) {
    echo $sub[$i] . "\n";
}
?>
```

**Output:**

```php
DBMS
Algorithm
C++
JAVA

```

**程序 2:** 这个例子说明了关联数组。

```php
<?php

// Declare an associative array
$detail = array( "Name"=>"GeeksforGeeks", 
                 "Address"=>"Noida", 
                 "Type"=>"Educational site");

// Display the output
var_dump ($detail);
?> 
```

**Output:**

```php
array(3) {
  ["Name"]=>
  string(13) "GeeksforGeeks"
  ["Address"]=>
  string(5) "Noida"
  ["Type"]=>
  string(16) "Educational site"
}

```

**程序 3:** 这个例子说明了多维数组。

```php
<?php

// Declare 2D array
$detail = array(array(1, 2, 3, 4),
                array(5, 6, 7, 8));

// Display the output
var_dump ($detail);
?> 
```

**Output:**

```php
array(2) {
  [0]=>
  array(4) {
    [0]=>
    int(1)
    [1]=>
    int(2)
    [2]=>
    int(3)
    [3]=>
    int(4)
  }
  [1]=>
  array(4) {
    [0]=>
    int(5)
    [1]=>
    int(6)
    [2]=>
    int(7)
    [3]=>
    int(8)
  }
}

```