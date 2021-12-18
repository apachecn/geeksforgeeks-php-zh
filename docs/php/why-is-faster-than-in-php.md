# PHP 中为什么===比==快？

> 原文:[https://www.geeksforgeeks.org/why-is-faster-than-in-php/](https://www.geeksforgeeks.org/why-is-faster-than-in-php/)

比较运算符 **=(等式运算符)**和 **===(等式运算符)**用于比较两个值。它们也被称为**宽松相等(==)** 运算符和**严格相同(===)** 运算符。

<figure class="table">T33】=T33

| symbol | name | example | output |
| = | equation | $a = $b | If TRUE $ a is equal to $ b, it is in type juggling. |
| identity |

</figure>

[**PHP 运算符:**](https://www.geeksforgeeks.org/php-operators/)PHP 中有很多运算符，但是==和= = = =运算符严格或随意地执行类似的任务。

*   如果操作数的类型不同，那么==和===将产生不同的结果**。在这种情况下，运算符的速度会有所不同，因为==将执行类型转换，然后进行比较。**
*   **如果操作数类型相同，那么==和===将产生相同的结果**。在这种情况下，两个运算符的速度几乎相同，因为任何运算符都不执行类型转换。****

****等式运算符==临时转换数据类型，以查看其值是否等于另一个操作数，而===(标识运算符)不需要进行任何类型转换，因此完成的工作更少，这使得它比= = =更快。
**例 1:****** 

## ****服务器端编程语言（Professional Hypertext Preprocessor 的缩写）****

```
**<?php

// 0 == 0 -> true as first type
// conversion is done and then
// checked if it is equal or not
var_dump(0 == "a");

// 1 == 1 -> true
var_dump("1" == "01");

// 10 == 10 -> true
var_dump("10" == "1e1");

// 100 == 100 -> true
var_dump(100 == "1e2");

// 0 === "a" -> false in this type
// conversion is not done only
// checking is there if they are
// equal or not
var_dump(0 === "a");

// "1" === "01" -> false
var_dump("1" === "01");

// "10" === "1e1" -> false
var_dump("10" === "1e1");

// 100 == "1e2" -> false
var_dump(100 === "1e2");

switch ("a") {
case 0:
    echo "In first case";
    break;

// Never reached because "a" is already
// matched with 0 as in switch == is used
case "a": 
    echo "In second case";
    break;
}
?>**
```

******输出:****** 

```
**bool(true)
bool(true)
bool(true)
bool(true)
bool(false)
bool(false)
bool(false)
bool(false)
In first case**
```

******例 2:****** 

## ****服务器端编程语言（Professional Hypertext Preprocessor 的缩写）****

```
**<?php

// TRUE - same as (bool)1 == TRUE
var_dump(1 == TRUE);

// TRUE - same as (bool)0 == FALSE
var_dump(0 == FALSE);

// FALSE - not same 1 and TRUE as
// 1 is integer and TRUE is boolean
var_dump(1 === TRUE);

// FALSE - not same 0 and FALSE as 0
// is integer and FALSE is boolean
var_dump(0 === FALSE);
?>**
```

******输出:****** 

```
**bool(true)
bool(true)
bool(false)
bool(false)**
```

******注意:**运算符===执行“typesafe 比较”，只有当两个操作数具有相同的类型和值时，它才会返回 true，而如果只比较值，则使用==。****