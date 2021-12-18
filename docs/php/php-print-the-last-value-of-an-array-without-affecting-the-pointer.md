# PHP|打印数组的最后一个值，不影响指针

> Original: [https://www.geeksforgeeks.org/php-print-the-last-value-of-an-array-without-affecting-the-pointer/](https://www.geeksforgeeks.org/php-print-the-last-value-of-an-array-without-affecting-the-pointer/)

我们得到一个具有键-值对的数组，我们需要在不影响数组指针的情况下找到数组的最后一个值。

示例：

```
Input : $arr = array('c1' => 'Red', 'c2' => 'Green', 
                          'c3' => 'Blue', 'c4' => 'Black')
Output : Black

Input : $arr = array('p1' => 'New York', 'p2' => 'Germany', 
                        'p3' => 'England', 'p4' => 'France')
Output : France

```

使用 PHP 可以很容易地解决上述问题。 其思想是创建原始数组的副本，然后使用**ARRAY_POP()**内置函数获取数组的最后一个值。 因为我们在复制数组上使用 array_op()函数，所以原始数组的指针保持不变。

**内置函数使用**：

*   *[ARRAY_POP ()](https://www.geeksforgeeks.org/php-array_pop-function/)* : this function is used to delete or pop the last element of the array.

以下是上述方法的实现：

```
<?php

    // Input Array
    $array = array('c1' => 'Delhi', 'c2' => 'Kolkata', 
                    'c3' => 'Mumbai', 'c4' => 'Bangalore');

    // Copied Array
    $copyArray = $array;

    // getting last element from Copied array    
    $lastElement = array_pop($copyArray);

    // displaying the last element of the array 
    print_r($lastElement."\n");

    // displaying the original array
    print_r($array);

?>    
```

帖子主题：Re：Колибри