# 如何用 PHP 创建一个对象的副本？

> 原文:[https://www . geesforgeks . org/如何用 php 创建对象副本/](https://www.geeksforgeeks.org/how-to-create-a-copy-of-an-object-in-php/)

使用**克隆**关键字(如果可能，调用对象的 __clone()方法)创建对象副本。不能直接调用对象的 __clone()方法。当一个对象被克隆时，PHP 将对该对象的所有属性执行一个浅拷贝。任何引用其他变量的属性都将保持引用状态。
**语法:**

```
$copy_object_name = clone $object_to_be_copied
```

**程序 1:** 创建对象副本的程序。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Program to create copy of an object

// Creating class
class GFG {
    public $data1;
    public $data2;
    public $data3;
}

// Creating object
$obj = new GFG();

// Creating clone or copy of object
$copy = clone $obj;

// Set values of $obj object
$obj->data1 = "Geeks";
$obj->data2 = "for";
$obj->data3 = "Geeks";

// Set values of copied object
$copy->data1 = "Computer ";
$copy->data2 = "science ";
$copy->data3 = "portal";

// Print values of $obj object
echo "$obj->data1$obj->data2$obj->data3\n";

// Print values of $copy object
echo "$copy->data1$copy->data2$copy->data3\n";

?>
```

**Output:** 

```
GeeksforGeeks
Computer science portal
```

**示例 2:** 下面的程序将克隆与赋值(=)运算符区分开来。

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php

// Program to create copy of an object

// Creating class
class GFG {
    public $data1;
    public $data2;
    public $data3;

}

// Creating object
$obj = new GFG();

// Creating clone or copy of object
$copy = clone $obj;

// Creating object without clone keyword
$obj_ref = $obj;

// Set values of $obj object
$obj->data1 = "Geeks";
$obj->data2 = "for";
$obj->data3 = "Geeks";

// Set values of copied object
$copy->data1 = "Python ";
$copy->data2 = "for ";
$copy->data3 = "Machine learning";

// Print values of $obj object
echo "$obj->data1$obj->data2$obj->data3\n";

// Print values of $copy object
echo "$copy->data1$copy->data2$copy->data3\n";

// Print values of without clone object
echo "$obj_ref->data1$obj_ref->data2$obj_ref->data3\n";

?>
```

**Output:** 

```
GeeksforGeeks
Python for Machine learning
GeeksforGeeks
```

**注意:**很明显克隆对象的值与原始对象不同，但是使用“=”运算符创建的原始对象和引用对象具有相同的值。
**参考文献:**[https://www.php.net/manual/en/language.oop5.cloning.php](https://www.php.net/manual/en/language.oop5.cloning.php)