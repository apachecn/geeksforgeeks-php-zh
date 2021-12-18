# 在 PHP 中将对象转换为关联数组

> 原文:[https://www . geesforgeks . org/convert-a-object-to-associative-array-in-PHP/](https://www.geeksforgeeks.org/convert-an-object-to-associative-array-in-php/)

对象是类的实例。它只是一个类的样本，并且分配了内存。数组是以单一名称存储一个或多个相似类型的值的数据结构，但关联数组不同于简单的 PHP 数组。包含字符串索引的数组称为关联数组。它将元素值与键值关联存储，而不是以线性索引顺序存储。
**方法 1:使用 json_decode 和 json_encode 方法:**json _ decode 函数接受 json 编码的字符串，并将其转换为 PHP 变量，另一方面 json_encode 返回给定值的 JSON 编码字符串。
**语法:**

```
$myArray = json_decode(json_encode($object), true);
```

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
class sample {

    /* Member variables */
    var $var1;
    var $var2;

    function __construct( $par1, $par2 ) 
    {
        $this->var1 = $par1;
        $this->var2 = $par2;
    }
}

// Creating the object
$myObj = new sample(1000, "second");
echo "Before conversion: \n";
var_dump($myObj);

// Converting object to associative array
$myArray = json_decode(json_encode($myObj), true);
echo "After conversion: \n";
var_dump($myArray);
?>
```

**Output:** 

```
Before conversion: 
object(sample)#1 (2) {
  ["var1"]=>
  int(1000)
  ["var2"]=>
  string(6) "second"
}
After conversion: 
array(2) {
  ["var1"]=>
  int(1000)
  ["var2"]=>
  string(6) "second"
}
```

**方法 2:将对象类型转换为数组:**类型转换是将一个数据类型变量转换为不同数据类型的方法，它只是数据类型的显式转换。它可以通过使用 PHP 中支持的类型转换规则将 PHP 对象转换为数组。
**语法:**

```
$myArray = (array) $myObj;
```

**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
class bag {

    /* Member variables */
    var $item1;
    var $item2;
    var $item3;

    function __construct( $par1, $par2, $par3) 
    {
        $this->item1 = $par1;
        $this->item2 = $par2;
        $this->item3 = $par3;
    }
}

// Create myBag object
$myBag = new bag("Mobile", "Charger", "Cable");
echo "Before conversion : \n";
var_dump($myBag);

// Converting object to an array
$myBagArray = (array)$myBag;
echo "After conversion : \n";
var_dump($myBagArray);
?>
```

**Output:** 

```
Before conversion : 
object(bag)#1 (3) {
  ["item1"]=>
  string(6) "Mobile"
  ["item2"]=>
  string(7) "Charger"
  ["item3"]=>
  string(5) "Cable"
}
After conversion : 
array(3) {
  ["item1"]=>
  string(6) "Mobile"
  ["item2"]=>
  string(7) "Charger"
  ["item3"]=>
  string(5) "Cable"
}
```

PHP 是一种专门为 web 开发设计的服务器端脚本语言。您可以通过以下 [PHP 教程](https://www.geeksforgeeks.org/php-tutorials/)和 [PHP 示例](https://www.geeksforgeeks.org/php-examples/)从头开始学习 PHP。