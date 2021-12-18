# 如何在 PHP 中循环通过一个关联数组并获取密钥？

> 原文:[https://www . geesforgeks . org/如何通过关联数组循环并在 php 中获取密钥/](https://www.geeksforgeeks.org/how-to-loop-through-an-associative-array-and-get-the-key-in-php/)

**[关联数组](https://www.geeksforgeeks.org/associative-arrays-in-php/) :** 关联数组用于存储键值对。例如，要将学生不同科目的分数存储在数组中，数字索引数组不是最佳选择。相反，我们可以使用各自主题的名称作为关联数组中的键，值将是它们各自获得的分数。在关联数组中，键值对与= >符号相关联。

**方法 1:** 在该方法中，使用 foreach 循环遍历整个关联数组并显示关键元素。
**程序:**程序循环通过关联数组和打印键。

```php
<?php
// Loop through associative array and get
// the key of associative array

// Associative array
$person_weight = array(
    "Rajnish" => 58, 
    "Sanjeev" => 55, 
    "Ravi" => 60, 
    "Yash" => 60,
    "Suraj" => 48
); 

// Use for-each loop and display the
// key of associative array
foreach($person_weight as $key => $value) { 
    echo "Key: " . $key . "\n"; 
}

?>
```

**Output:**

```php
Key: Rajnish
Key: Sanjeev
Key: Ravi
Key: Yash
Key: Suraj

```

**方法二:使用 [array_keys()函数:](https://www.geeksforgeeks.org/php-array_keys-function/)**array _ keys()是 PHP 中的一个内置函数，用于返回数组的所有键或键的子集。

**语法:**

```php
array array_keys( $input_array, $search_value, $strict )
```

**程序:**下面的程序说明了如何使用 array_keys()函数来访问关联数组的键。

```php
<?php
// Use array_keys() function to display
// the key of associative array

// Associative array
$assoc_array = array(
    "Geeks" => 30,
    "for" => 20,
    "geeks" => 10
); 

// Using array_keys() function
$key = array_keys($assoc_array);

// Calculate the size of array
$size = sizeof($key);

// Using loop to access keys
for( $i = 0; $i < $size; $i++) {
    echo "key: ${key[$i]}\n";
}

?>
```

**Output:**

```php
key: Geeks
key: for
key: geeks

```