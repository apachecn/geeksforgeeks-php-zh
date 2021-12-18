# 确定 PHP 中 foreach 循环的第一次和最后一次迭代？

> 原文:[https://www . geeksforgeeks . org/确定 php 中的第一次和最后一次迭代/](https://www.geeksforgeeks.org/determine-the-first-and-last-iteration-in-a-foreach-loop-in-php/)

给定一个元素数组，任务是确定 foreach 循环中的第一次和最后一次迭代。解决这个问题的方法有很多，列举如下:
**方法 1:** 寻找迭代是 foreach 循环内部的幼稚方法。使用计数器变量，检查计数器值何时为零，这是第一次迭代，计数器值何时为 length-1，这是最后一次迭代。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// PHP program to get first and
// last iteration

// Declare an array and initialize it
$myarray = array( 1, 2, 3, 4, 5, 6 );

// Declare a counter variable and
// initialize it with 0
$counter = 0;

// Loop starts from here
foreach ($myarray as $item) {

    // Check condition if count is 0 then
    // it is the first iteration
    if( $counter == 0 ) {

        // Print the array content
        print( $item );
        print(": First iteration \n");
    }

    // Check condition if count is length -1
    // then it is last iteration
    if( $counter == count( $myarray ) - 1) {

        // Print the array content
        print( $item );
        print(": Last iteration");
    }

    $counter = $counter + 1;
}

?>
```

**Output:** 

```php
1: First iteration 
6: Last iteration
```

**方法二:**利用复位和结束函数寻找第一次和最后一次迭代。 [reset()函数](https://www.geeksforgeeks.org/php-reset-function/)是 PHP 中的一个内置函数，以数组名为参数，返回数组的第一个元素。 [end()函数](https://www.geeksforgeeks.org/php-end-function/)是 PHP 中的一个内置函数，它以数组名为参数，返回最后一个元素。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// PHP program to get first and
// last iteration

// Declare and array and initialize it
$myarray = array( 1, 2, 3, 4, 5, 6 );

// Loop starts here
foreach ( $myarray as $item ) {

    // Check item and the return value of
    // reset() function is equal then it
    // will be the first iteration
    if ( $item === reset( $myarray ) ) {

        // Display the array element
        print( $item );
        print(": First iteration \n");
    }

    // Check if item and return value of
    // end() function is equal then it
    // will be last iteration
    else if( $item === end( $myarray ) ) {

        // Display the array element
            print( $item );
        print(": :ast iteration \n");
    }
}
?>
```

**Output:** 

```php
1: First iteration 
6: :ast iteration
```

**方法 3:**[重置()函数](https://www.geeksforgeeks.org/php-reset-function/)用于寻找 foreach 循环中的第一次迭代。当数组中没有下一个元素可用时，它将是最后一次迭代，并由 [next()函数](https://www.geeksforgeeks.org/php-next-function/)计算。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```php
<?php

// PHP program to get first and
// last iteration

// Declare an array and initialize it
$myarray = array( 1, 2, 3, 4, 5, 6 );

// Assign first array element to variable
$first = reset( $myarray );

// Loop starts here
foreach ($myarray as $item) {

    // Check if item is equal to first
    // element then it is the first
    // iteration
    if ($item == $first) {

        // Display array element
        print( $item );
        print(": First iteration \n");
    }

    // If there is no next element
    // in array then this is last iteration
    if( !next( $myarray ) ) {

        // Display array element
        print( $item );
        print(": Last iteration \n");
    }
}
?>
```

**Output:** 

```php
1: First iteration 
6: Last iteration
```