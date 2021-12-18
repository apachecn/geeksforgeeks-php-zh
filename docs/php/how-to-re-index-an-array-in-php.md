# 如何在 PHP 中对数组进行重新索引？

> 原文:[https://www . geesforgeks . org/如何重新索引 php 数组/](https://www.geeksforgeeks.org/how-to-re-index-an-array-in-php/)

数组的重新索引可以通过一起使用一些内置函数来完成。这些功能是:

*   **[array_combine()函数](https://www.geeksforgeeks.org/php-array_combine-function/):**array _ combine()函数是 PHP 中的一个内置函数，用于组合两个数组，并通过使用一个数组作为键，另一个数组作为值来创建一个新数组。也就是说，一个数组的所有元素将是新数组的键，第二个数组的所有元素将是这个新数组的值。
*   **[range()函数](https://www.geeksforgeeks.org/php-range-function/):**range()函数是 PHP 中的一个内置函数，用于在给定的范围内(从低到高)创建任何类型的元素数组，如整数、字母，即列表的第一个元素被认为是低的，最后一个元素被认为是高的。
*   **[count()函数](https://www.geeksforgeeks.org/php-count-function/):**count()函数用于对数组中的当前元素进行计数。对于已设置为空数组的变量，该函数可能返回 0。对于未设置的变量，函数也返回 0。
*   **[array_values()函数](https://www.geeksforgeeks.org/php-array_values-function/) :** 该函数用于从另一个可能包含键值对或仅包含值的数组中获取一个值数组。该函数创建另一个数组，存储所有值，并默认为这些值分配数字键。

我们将使用 array_values()函数获取数组的所有值，并使用 range()函数创建一个元素数组，我们希望将其用作数组的新键或新索引(重新索引)。然后，array_combine()函数将把数组组合成键和值。

**例 1:**

```php
<?php

// Declare an associative array
$arr = array (
    0 => 'Tony',
    1 => 'Stark',
    2 => 'Iron', 
    3 => 'Man' 
);

echo "Array before re-indexing\n";

// Using foreach loop to print array elements
foreach( $arr as $key => $value) { 
    echo "Index: " . $key . " Value: " . $value . "\n"; 
}

// Set the index number from three
$New_start_index = 3;

$arr = array_combine(range($New_start_index, 
                count($arr) + ($New_start_index-1)),
                array_values($arr));

echo "\nArray after re-indexing\n";

// Using foreach loop to print array elements
foreach( $arr as $key => $value) { 
    echo "Index: ".$key." Value: ".$value."\n"; 
}

?>
```

**Output:**

```php
Array before re-indexing
Index: 0 Value: Tony
Index: 1 Value: Stark
Index: 2 Value: Iron
Index: 3 Value: Man

Array after re-indexing
Index: 3 Value: Tony
Index: 4 Value: Stark
Index: 5 Value: Iron
Index: 6 Value: Man

```

**示例 2:** 在数组的开头添加一些数据，然后从索引中对数组进行切片。

```php
<?php

// Declare an associative array
$arr = array (
    0 => 'Tony',
    1 => 'Stark',
    2 => 'Iron', 
    3 => 'Man'
);

echo "Array before re-indexing\n";

// Using foreach loop to print array elements
foreach( $arr as $key => $value) { 
    echo "Index: " . $key . " Value: " . $value . "\n"; 
}

// Set the index number from three
$New_start_index = 3;

$raw_data = range( 0, $New_start_index-1 );

// Add data to the start of the array
foreach( $raw_data as $key => $value) {
    array_unshift($arr, $value);
}

$arr = array_values($arr);

// Remove the unnecessary index so we start at 10
$arr = array_slice($arr, $New_start_index, count($arr), true);
echo "\nArray after re indexing\n";

// Using foreach loop to print array 
foreach( $arr as $key => $value) { 
    echo "Index: ".$key." Value: ".$value."\n"; 
}

?>
```

**Output:**

```php
Array before re-indexing
Index: 0 Value: Tony
Index: 1 Value: Stark
Index: 2 Value: Iron
Index: 3 Value: Man

Array after re indexing
Index: 3 Value: Tony
Index: 4 Value: Stark
Index: 5 Value: Iron
Index: 6 Value: Man

```

在本例中，首先向数组中添加一些数据，为此，我们再次在循环的帮助下这样做，然后删除我们添加的数据，因此重新索引数组也不是一个好的选择。这种方法不适合重新索引字母键。

**示例 3:** 本示例从字母“p”重新索引数组。两个额外的功能用于重新索引字母，它们是:

*   **[order()](https://www.geeksforgeeks.org/php-ord-function/)函数:**order()函数是 PHP 中的一个内置函数，返回字符串第一个字符的 ASCII 值。
*   **[chr()](https://www.geeksforgeeks.org/php-chr-fucntion/) 函数:**chr()函数是 PHP 中的内置函数，用于将 ASCII 值转换为字符。

```php
<?php

// Declare an associative array
$arr = array( 
    'a' => 'India',
    'b' => 'America',
    'c' => 'Russia',
    'd' => 'China'
);

echo "Array before re-indexing\n";

// Using foreach loop to print array elements
foreach( $arr as $key => $value) { 
    echo "Index: " . $key . " Value: " . $value . "\n"; 
}

// Set the index from 'p'
$New_start_index = 'p';

// The ord() function is used to get ascii value
// The chr() function to convert number to ASCII char
$arr = array_combine(range($New_start_index, 
            chr(count($arr) + (ord($New_start_index)-1))),
            array_values($arr));

echo "\nArray after re indexing\n";

// Using foreach loop to print array 
foreach( $arr as $key => $value) { 
    echo "Index: " . $key . " Value: " . $value . "\n"; 
}

?>
```

**Output:**

```php
Array before re-indexing
Index: a Value: India
Index: b Value: America
Index: c Value: Russia
Index: d Value: China

Array after re indexing
Index: p Value: India
Index: q Value: America
Index: r Value: Russia
Index: s Value: China

```