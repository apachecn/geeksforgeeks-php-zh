# PHP | array_fill_keys()函数

> 原文:[https://www.geeksforgeeks.org/php-array_fill_keys-function/](https://www.geeksforgeeks.org/php-array_fill_keys-function/)

array_fill_keys()函数是 PHP 中的一个内置函数，用于创建一个新的数组，该数组由作为数组提供给函数的给定键和值填充。

**语法**:

```
*array* array_fill_keys ( $keys, $value )

```

**参数**:这个函数接受两个参数，键和它们的值出现在新数组中。这两个参数描述如下:

1.  **$keys** :该参数是一个由用于创建新数组的键组成的数组。如果 *$keys* 数组包含任何非法值，那么它将被转换为字符串并使用。
2.  **$value** :该参数可以是单个值，也可以是一列值。此参数表示要插入数组的键的值。如果这个参数是一个数组，那么创建的新数组将是一个二维数组，其中$keys 数组的每个元素都是一个键，并且这个新数组中的每个键都将$value 数组作为一个值。

**返回值**:该函数返回一个由键值对组成的数组，键值对作为参数提供给函数。

示例:

```
Input : $keys = array('golden', 25, 560, 'age')
        array_fill_keys($keys, 'majestic')
Output : Array
        (
           [golden] => majestic
           [25] => majestic
           [560] => majestic
           [age] => majestic
        )

Input :$keys = array('tumult', '25', 560, 'cater')
       array_fill_keys($keys, 'limited')
Output : Array
        (
           [tumult] => limited
           [25] => limited
           [560] => limited
           [cater] => limited
        )

```

在这两个示例中，要与新数组一起使用的键作为函数的数组提供，要使用的值作为第二个参数提供。

下面的程序说明了 PHP 中的 array_fill_keys()函数:

**程序 1** :

```
<?php

$keys = array('golden', 25, 560, 'age');

// Creating new array with specified keys
$a = array_fill_keys($keys, 'majestic');

print_r($a);

?>
```

输出:

```
Array
(
    [golden] => majestic
    [25] => majestic
    [560] => majestic
    [age] => majestic
)

```

**程序 2** :

```
<?php

$keys = array('tumult', '25', 560, 'cater');

// Creating new array
$a = array_fill_keys($keys, 'limited');

print_r($a);

?>
```

输出:

```
Array
(
    [tumult] => limited
    [25] => limited
    [560] => limited
    [cater] => limited
)

```

**程序 3** :

```
<?php

$keys = array('tumult', '25', 560, 'cater');
$value = array(5,10);

// Creating new array
$a = array_fill_keys($keys, $value);

print_r($a);

?>
```

输出:

```
Array
(
    [tumult] => Array
        (
            [0] => 5
            [1] => 10
        )

    [25] => Array
        (
            [0] => 5
            [1] => 10
        )

    [560] => Array
        (
            [0] => 5
            [1] => 10
        )

    [cater] => Array
        (
            [0] => 5
            [1] => 10
        )
)

```

**参考**:
T3】http://php.net/manual/en/function.array-fill-keys.php