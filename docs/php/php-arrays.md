# PHP |数组

> 原文:[https://www.geeksforgeeks.org/php-arrays/](https://www.geeksforgeeks.org/php-arrays/)

PHP 中的数组是一种数据结构，它允许我们在一个变量下存储多个相似数据类型的元素，从而节省了我们为每个数据创建不同变量的工作量。数组有助于创建相似类型的元素列表，可以使用它们的索引或键来访问这些元素。假设我们想存储五个名字并相应地打印出来。这可以通过使用五个不同的字符串变量来轻松实现。但是，如果不是五个，而是一百个，那么用户或开发人员将很难创建这么多不同的变量。在这里，数组开始发挥作用，帮助我们将每个元素存储在一个变量中，并允许使用索引或键轻松访问。一个数组是用 PHP 中的**数组()**函数创建的。

PHP 中基本上有三种类型的数组:

*   **索引数组或数值数组:**带有数值索引的数组，其中的值是线性存储的。
*   **关联数组:**具有字符串索引的数组，其中每个值都可以被分配一个特定的键，而不是线性存储。
*   **多维数组:**包含单个或多个数组并可通过多个索引访问的数组。

**索引或数字数组**

这些类型的数组可以用来存储任何类型的元素，但是索引总是一个数字。默认情况下，索引从零开始。这些阵列可以通过两种不同的方式创建，如下例所示:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// One way to create an indexed array
$name_one = array("Zack", "Anthony", "Ram", "Salim", "Raghav");

// Accessing the elements directly
echo "Accessing the 1st array elements directly:\n";
echo $name_one[2], "\n";
echo $name_one[0], "\n";
echo $name_one[4], "\n";

// Second way to create an indexed array
$name_two[0] = "ZACK";
$name_two[1] = "ANTHONY";
$name_two[2] = "RAM";
$name_two[3] = "SALIM";
$name_two[4] = "RAGHAV";

// Accessing the elements directly
echo "Accessing the 2nd array elements directly:\n";
echo $name_two[2], "\n";
echo $name_two[0], "\n";
echo $name_two[4], "\n";

?>
```

输出:

```
Accessing the 1st array elements directly:
Ram
Zack
Raghav
Accessing the 2nd array elements directly:
RAM
ZACK
RAGHAV
```

**遍历**:我们可以使用 PHP 中的循环遍历索引数组。我们可以通过两种方式循环索引数组。首先使用 for 循环，其次使用 foreach。语法和基本用法可以参考 [PHP | Loops](https://www.geeksforgeeks.org/php-loops/) 。

示例:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Creating an indexed array
$name_one = array("Zack", "Anthony", "Ram", "Salim", "Raghav");

// One way of Looping through an array using foreach
echo "Looping using foreach: \n";
foreach ($name_one as $val){
    echo $val. "\n";
}

// count() function is used to count
// the number of elements in an array
$round = count($name_one);
echo "\nThe number of elements are $round \n";

// Another way to loop through the array using for
echo "Looping using for: \n";
for($n = 0; $n < $round; $n++){
    echo $name_one[$n], "\n";
}

?>
```

输出:

```
Looping using foreach: 
Zack
Anthony
Ram
Salim
Raghav

The number of elements is 5 
Looping using for: 
ZACK
ANTHONY
RAM
SALIM
RAGHAV
```

**关联数组**

这些类型的数组类似于索引数组，但不是线性存储，每个值都可以用用户定义的字符串类型的键来赋值。

示例:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// One way to create an associative array
$name_one = array("Zack"=>"Zara", "Anthony"=>"Any",
                  "Ram"=>"Rani", "Salim"=>"Sara",
                  "Raghav"=>"Ravina");

// Second way to create an associative array
$name_two["zack"] = "zara";
$name_two["anthony"] = "any";
$name_two["ram"] = "rani";
$name_two["salim"] = "sara";
$name_two["raghav"] = "ravina";

// Accessing the elements directly
echo "Accessing the elements directly:\n";
echo $name_two["zack"], "\n";
echo $name_two["salim"], "\n";
echo $name_two["anthony"], "\n";
echo $name_one["Ram"], "\n";
echo $name_one["Raghav"], "\n";

?>
```

输出:

```
Accessing the elements directly:
zara
sara
any
Rani
Ravina
```

**遍历关联数组**:我们可以使用循环以类似于数值数组的方式遍历关联数组。我们可以通过两种方式循环访问关联数组。首先使用 for 循环，其次使用 foreach。语法和基本用法可以参考 [PHP | Loops](https://www.geeksforgeeks.org/php-loops/) 。

示例:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Creating an associative array
$name_one = array("Zack"=>"Zara", "Anthony"=>"Any",
                    "Ram"=>"Rani", "Salim"=>"Sara",
                    "Raghav"=>"Ravina");

// Looping through an array using foreach
echo "Looping using foreach: \n";
foreach ($name_one as $val => $val_value){
    echo "Husband is ".$val." and Wife is ".$val_value."\n";
}

// Looping through an array using for
echo "\nLooping using for: \n";
$keys = array_keys($name_two);
$round = count($name_two);

for($i=0; $i < $round; ++$i) {
    echo $keys[$i] . ' ' . $name_two[$keys[$i]] . "\n";
}

?>
```

输出:

```
Looping using foreach: 
Husband is Zack and Wife is Zara
Husband is Anthony and Wife is Any
Husband is Ram and Wife is Rani
Husband is Salim and Wife is Sara
Husband is Raghav and Wife is Ravina

Looping using for: 
zack zara
anthony any
ram rani
salim sara
raghav ravina
```

**多维数组**

多维数组是在每个索引处存储另一个数组而不是单个元素的数组。换句话说，我们可以将多维数组定义为数组的数组。顾名思义，这个数组中的每个元素都可以是一个数组，它们还可以包含其他子数组。多维数组中的数组或子数组可以使用多维来访问。

示例:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Defining a multidimensional array
$favorites = array(
    array(
        "name" => "Dave Punk",
        "mob" => "5689741523",
        "email" => "davepunk@gmail.com",
    ),
    array(
        "name" => "Monty Smith",
        "mob" => "2584369721",
        "email" => "montysmith@gmail.com",
    ),
    array(
        "name" => "John Flinch",
        "mob" => "9875147536",
        "email" => "johnflinch@gmail.com",
    )
);

// Accessing elements
echo "Dave Punk email-id is: " . $favorites[0]["email"], "\n";
echo "John Flinch mobile number is: " . $favorites[2]["mob"];

?>
```

输出:

```
Dave Punk email-id is: davepunk@gmail.com
John Flinch mobile number is: 9875147536
```

**遍历多维数组**:我们可以使用 for 和 foreach 循环以嵌套的方式遍历多维数组。也就是说，一个用于外部数组的循环，一个用于内部数组的循环。

示例:

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// Defining a multidimensional array
$favorites = array(
    "Dave Punk" => array(
        "mob" => "5689741523",
        "email" => "davepunk@gmail.com",
    ),
    "Dave Punk" => array(
        "mob" => "2584369721",
        "email" => "montysmith@gmail.com",
    ),
    "John Flinch" => array(
        "mob" => "9875147536",
        "email" => "johnflinch@gmail.com",
    )
);

// Using for and foreach in nested form
$keys = array_keys($favorites);
for($i = 0; $i < count($favorites); $i++) {
    echo $keys[$i] . "\n";
    foreach($favorites[$keys[$i]] as $key => $value) {
        echo $key . " : " . $value . "\n";
    }
    echo "\n";
}

?>
```

输出:

```
Dave Punk
mob : 2584369721
email : montysmith@gmail.com

John Flinch
mob : 9875147536
email : johnflinch@gmail.com
```

本文由 [**【钦莫伊蕾恩卡】**](https://auth.geeksforgeeks.org/user/Chinmoy%20Lenka/articles) 供稿。如果你喜欢 GeeksforGeeks 并想投稿，你也可以使用[write.geeksforgeeks.org](https://write.geeksforgeeks.org)写一篇文章或者把你的文章邮寄到 review-team@geeksforgeeks.org。看到你的文章出现在极客博客主页上，帮助其他极客。
如果发现有不正确的地方，或者想分享更多关于上述话题的信息，请写评论。

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。