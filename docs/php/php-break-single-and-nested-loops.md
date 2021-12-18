# PHP 中断(单循环和嵌套循环)

> 原文:[https://www . geesforgeks . org/PHP-break-single-and-nested-loops/](https://www.geeksforgeeks.org/php-break-single-and-nested-loops/)

在 PHP 中，break 用于立即终止循环，程序控制在循环后的下一条语句中继续。
**方法 1:** 给定一个数组，任务是运行一个循环并显示数组中的所有值，遇到 5 时终止循环。

**示例:**

```php
Input : array1 = array( 1, 2, 3, 4, 5, 6, 7 )
Output : 1 2 3 4
         Loop Terminated
The loop contains an if condition and when condition is true then
loop will break otherwise display the array content. 

Input : array1 = array( '10', '2', '5', '20', '40' )
Output : 10 2
        Loop Terminated

```

**程序:**

```php
<?php
// PHP program to break the loop

// Declare an array and initialize it
$array = array( 1, 2, 3, 4, 5, 6, 7 );

// Use foreach loop
foreach ($array as $a) {
    if ($a == 5)
        break;
    else
        echo $a . " ";
}
echo "\n";
echo "Loop Terminated";
?>
```

**Output:**

```php
1 2 3 4 
Loop Terminated

```

**方法 2:** 给定嵌套循环，在 PHP 中我们可以使用*中断 2* 来终止两个循环。下面的程序包含嵌套循环，并使用 break 语句终止它。
例如给定两个数组 arr1 和 arr2，任务是为 arr1 的每个值显示 arr2 的所有值，直到 arr1 的值不等于 arr2。如果 arr1 中的值等于 arr2 的值，则使用*中断 2* 终止两个循环，并执行进一步的语句。

**示例:**

```php
Input : arr1 = array( 'A', 'B', 'C' );
        arr2 = array( 'C', 'A', 'B', 'D' );
Output : A C 
         Loop Terminated

Input : arr1 = array( 10, 2, 5, 20, 40 )
        arr2 = array( 1, 2 )
Output :10 1 2
        2 1
        Loop Terminated

```

```php
<?php
// PHP program to break the loop

// Declare two array and initialize it
$arr1 = array( 'A', 'B', 'C' );
$arr2 = array( 'C', 'A', 'B', 'D' );

// Use foreach loop
foreach ($arr1 as $a) {
    echo "$a ";

    // Ue nested loop
    foreach ($arr2 as $b) {
        if ($a != $b )
            echo "$b ";
        else
            break 2; 
    }
    echo "\n";
}

echo "\nLoop Terminated";
?>
```

**Output:**

```php
A C 
Loop Terminated

```