# PHP | array_column()函数

> 原文:[https://www.geeksforgeeks.org/php-array_column-function/](https://www.geeksforgeeks.org/php-array_column-function/)

array_column()是 PHP 中的一个内置函数，用于返回输入数组中单个列的值。

**语法:**

```php
*array* array_column($input_array, $column_number, $index_key);
```

**参数** :
三个参数中，两个是强制的，一个是可选的。让我们看看参数。

1.  **$input_array(必选):**这个参数指的是我们想要从中提取特定列的所有值的原始多维数组。
2.  **$column_number(必选):**此参数是指需要返回的值的列。该值可以是列的整数键，也可以是关联数组或属性名的字符串键名。返回完整的数组或对象也可以为空。
3.  **$index_key(可选):**这是一个可选参数，指的是在输出中用作返回数组的索引/键的列。该值可能是列的整数键，也可能是字符串键名称。

**返回类型**:如语法所示，array_column()函数的返回类型为 array。也就是说，该函数返回一个数组，该数组包含输入数组中单个列的值，由 column_number 标识。可选地，还可以提供 index_key，以通过来自输入数组的 index_key 列的值来索引返回数组中的值。

示例:

```php
Input : 
      array(
        array(
            'roll' => 5,
            'name' => 'Akash',
            'hobby' => 'Cricket',
        ),
        array(
            'roll' => 1,
            'name' => 'Rishav',
            'hobby' => 'Football',
        ),
        array(
            'roll' => 3,
            'name' => 'Anand',
            'hobby' => 'Chess',
        ),
      )

      $column_number = 'hobby'  ,   $index_key = 'roll'
Output : 
      Array
      (
         [5] => Cricket
         [1] => Football
         [3] => Chess
         [4] => Cards
         [2] => Basketball
      )
```

在上面的例子中，array_column()函数用于获取关键字为“name”的列的值，输出数组中的这些值与关键字一起存储，这些关键字取自原始数组中关键字“roll”的值。

下面的程序用所有三个参数说明了 array_column():

## C++

```php
<?php
// PHP code to illustrate the working of array_column
function Column($details){
    $rec = array_column($details, 'name', 'roll');
    return $rec;
}

// Driver Code
$details = array(
    array(
        'roll' => 5,
        'name' => 'Akash',
        'hobby' => 'Cricket',
    ),
    array(
        'roll' => 1,
        'name' => 'Rishav',
        'hobby' => 'Football',
    ),
    array(
        'roll' => 3,
        'name' => 'Anand',
        'hobby' => 'Chess',
    ),
    array(
        'roll' => 4,
        'name' => 'Gaurav',
        'hobby' => 'Cards',
    ),
    array(
        'roll' => 2,
        'name' => 'Rahim',
        'hobby' => 'Basketball',
    ),
);
print_r(Column($details));
?>
```

输出:

```php
Array
(
    [5] => Akash
    [1] => Rishav
    [3] => Anand
    [4] => Gaurav
    [2] => Rahim
)
```

我们也可以忽略第三个参数，即 index_key。然后，在这种情况下，输出数组中的列将以数组中给出的线性方式被索引。下面是 PHP 程序来说明这一点:

## C++

```php
<?php
// PHP code to illustrate the working of array_column
function Column($details){
    $rec = array_column($details, 'hobby');
    return $rec;
}

// Driver Code
$details = array(
    array(
        'roll' => 5,
        'name' => 'Akash',
        'hobby' => 'Cricket',
    ),
    array(
        'roll' => 1,
        'name' => 'Rishav',
        'hobby' => 'Football',
    ),
    array(
        'roll' => 3,
        'name' => 'Anand',
        'hobby' => 'Chess',
    ),
    array(
        'roll' => 4,
        'name' => 'Gaurav',
        'hobby' => 'Cards',
    ),
    array(
        'roll' => 2,
        'name' => 'Rahim',
        'hobby' => 'Basketball',
    ),
);
print_r(Column($details));
?>
```

输出:

```php
Array
(
    [0] => Cricket
    [1] => Football
    [2] => Chess
    [3] => Cards
    [4] => Basketball
)
```