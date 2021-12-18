# 如何用 PHP 打破一个外环？

> 原文:[https://www . geesforgeks . org/如何用 php 打破外环/](https://www.geeksforgeeks.org/how-to-break-an-outer-loop-with-php/)

**使用 break 关键字:**break 关键字用于立即终止循环，程序控制在循环后的下一条语句处恢复。要从任何循环中终止控件，我们需要使用 break 关键字。break 关键字用于结束当前**对于、foreach、while、do-while** 或**开关**结构的执行。但是在嵌套循环中，要退出所有或部分外部循环，我们需要传递一个数字参数，告诉它要终止多少嵌套的封闭结构。

**语法:**

```
break number_of_nested_loop_to_terminate;
```

**参数:**break 关键字后跟一个数字参数，默认为 1。不允许将变量和 0 作为数值参数传递。

**示例:**

```
break 2; // It terminates second outer loop
break 3; // It terminates third outer loop
break $num; // Variable cannot be used as numeric argument since version 5.4.0
break 0; // 0 is not a valid argument to pass

```

下面的程序说明了如何在 PHP 中打破外部循环:

**程序 1:** PHP 程序，在不终止内部循环的情况下显示数字。

```
<?php

// Initialize a number
$num = 10;

// Outer loop to iterate $num times
for( $i = 0; $i < 10; $i++ ) {

    // Initialize a variable $j
    $j = 1;

    // Inner loop
    while( $j <= 3 ) {

        if( $i >= 1 )

            // Breaking the outer loop
            break 2;

        echo $j . " ";
        $j++;
    } 
}

?>
```

**Output:**

```
1 2 3

```

**程序 2:** PHP 程序，在数组中搜索一个数字，找到后打破外循环。

```
<?php

// Create a 2D array
$arr = array(
    array (105, 96, 112), 
    array(96, 45, 63) 
);

// Initialize a number which
// need to fine in the array
$num = 45;

// Declare a boolean variable and
// initialize it with false
$found = FALSE;

// Outer loop
for($i = 0; $i < 2; $i++) {

    // Inner loop
    for($j = 0; $j < 3; $j++) {

        if($num == $arr[$i][$j]) {
            $found = TRUE;

            // Terminate the outer loop
            break 2;
        }
    } 
}

// Check number is found or not
if( $found )
    echo $num . " is found in the array";
else
    echo $num . " is not found in the given array";

?>
```

**Output:**

```
45 is found in the array

```

**使用 goto 关键字:**goto 关键字用于跳转程序的章节。它会跳到目标标签。

**程序 3:** PHP 程序使用 goto 关键字打破外循环。

```
<?php

// Create a 2D array
$arr = array(
    array (105, 96, 112), 
    array(96, 45, 63) 
);

// Initialize a number which
// need to fine in the array
$num = 45;

// Declare a boolean variable and
// initialize it with false
$found = FALSE;

// Outer loop
for($i = 0; $i < 2; $i++) {

    // Inner loop
    for($j = 0; $j < 3; $j++) {

        if($num == $arr[$i][$j]) {
            $found = TRUE;

            // Terminate the outer loop
            // using goto keyword
            goto terminateLoop;
        }
    } 
}

// target label
terminateLoop:

// Check number is found or not
if( $found )
    echo $num . " is found in the array";
else
    echo $num . " is not found in the given array";

?>
```

**Output:**

```
45 is found in the array

```