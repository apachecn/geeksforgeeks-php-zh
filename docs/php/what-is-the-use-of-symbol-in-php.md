# PHP 中“= >”符号有什么用？

> 原文:[https://www . geesforgeks . org/PHP 中符号的用途是什么/](https://www.geeksforgeeks.org/what-is-the-use-of-symbol-in-php/)

“= >”符号用于分配数组中的键值对。左侧的值称为键，右侧的值称为键的值。它主要用于关联数组。

**语法:**

```php
key => value
```

**示例 1:** 使用“= >”符号创建关联数组的 PHP 程序。

```php
<?php 
// PHP program to use '=>' symbol
$subject = array( "Maths" => 95,
                  "Physics" => 90, 
                  "Chemistry" => 96,
                  "English" => 93, 
                  "Computer" => 98
            ); 

// Accessing the array elements
echo "Marks for students:\n"; 
echo "Maths:" . $subject["Maths"], "\n"; 
echo "Physics:" . $subject["Physics"], "\n"; 
echo "Chemistry:" . $subject["Chemistry"], "\n"; 
echo "English:" . $subject["English"], "\n"; 
echo "Computer:" . $subject["Computer"], "\n"; 

?> 
```

**Output:**

```php
Marks for students:
Maths:95
Physics:90
Chemistry:96
English:93
Computer:98

```

**示例 2:** 使用“= >”符号创建数字索引数组的 PHP 程序。

```php
<?php
// PHP program to create numeric
// indexed array
$arr = array( "0" => 7,
              "1" => 10,
              "2" => 8,
              "3" => 5
        );

// Display array elements
foreach($arr as $key => $value) {
    echo $key . " => " . $value . "\n";
}

?>
```

**Output:**

```php
0 => 7
1 => 10
2 => 8
3 => 5

```

**示例 3:** PHP 程序在不使用“= >”符号的情况下分配数值索引。

```php
<?php 
// PHP program to create indexed array
// without using '=>' symbols
$name = array("Zack", "Anthony", 
        "Ram", "Salim", "Raghav"); 

// Display array elements
foreach($name as $key => $value) {
    echo $key . " => " . $value . "\n";
}

?> 
```

**Output:**

```php
0 => Zack
1 => Anthony
2 => Ram
3 => Salim
4 => Raghav

```