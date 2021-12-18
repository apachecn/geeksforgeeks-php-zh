# 如何在 PHP 中找到 foreach 循环的索引？

> 原文:[https://www . geeksforgeeks . org/如何找到 php 中 foreach 循环的索引/](https://www.geeksforgeeks.org/how-to-find-the-index-of-foreach-loop-in-php/)

foreach 构造提供了迭代数组元素的最简单方法。它适用于数组和对象。foreach 循环虽然迭代了一个元素数组，但执行过程得到了简化，完成循环的时间相对较短。它为索引迭代分配临时内存，这使得整个系统在内存分配方面的性能冗余。如果我们试图对未初始化的变量或具有不同数据类型的变量使用 foreach 循环，将会出现错误。

**语法:**

```
foreach( $array as $element ) {
    // PHP Code to be executed
}
```

或者

```
foreach( $array as $key =>> $element) {
    // PHP Code to be executed
}
```

**返回值:**

*   **$key:** 该变量保存当前元素的键索引/
*   **$value:** 在每次迭代中，数组元素的当前值被赋给$value 变量。

**程序 1:**

```
<?php

// Declare an array
$arr = array(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);

// Iterate through the array using foreach
// construct and store the key and its value

// Use foreach loop to display the
// key of allelements
foreach ($arr as $key => $value) {
    echo "key = " . $key . ", value = "
        . $value . "\n";
}

?>
```

**输出:**

```
key = 0, value = 1
key = 1, value = 2
key = 2, value = 3
key = 3, value = 4
key = 4, value = 5
key = 5, value = 6
key = 6, value = 7
key = 7, value = 8
key = 8, value = 9
key = 9, value = 10

```

**程序 2:**

```
<?php

// Declare an array
$arr = array(
    "a" => "Welcome",
    "b" => "to",
    "d" => "GeeksforGeeks"
);

// Iterate through the array using foreach
// construct and store the key and its value

// Use foreach loop to display the
// key of allelements
foreach ($arr as $key => $value) {
    echo "key = " . $key . ", value = "
        . $value . "\n";
}

?>
```

**输出:**

```
key = a, value = 1
key = b, value = 2
key = c, value = 3
key = d, value = 4

```

**程序 3:**

```
<?php

// Declare a multi-dimensional array
$arr = array(
    array(1, 2, 3), 
    array(4, 5, 6),
    array(7, 8, 9)
);

// Iterate through the array using foreach
// construct and store the key and its value

// Use foreach loop to display the
// key of allelements
foreach ($arr as $keyOut => $out) {
    foreach($out as $keyIn => $value) {
        echo "key = (" . $keyOut . ", " . $keyIn
             . "), value = " . $value . "\n";    
    }
}

?>
```

**输出:**

```
key = (0, 0), value = 1
key = (0, 1), value = 2
key = (0, 2), value = 3
key = (1, 0), value = 4
key = (1, 1), value = 5
key = (1, 2), value = 6
key = (2, 0), value = 7
key = (2, 1), value = 8
key = (2, 2), value = 9

```