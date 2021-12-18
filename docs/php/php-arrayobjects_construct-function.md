# PHP | ArrayObjects::_ construct()函数

> 原文:[https://www . geesforgeks . org/PHP-arrayobjects _ construct-function/](https://www.geeksforgeeks.org/php-arrayobjects_construct-function/)

ArrayObjects 类允许对象作为数组工作。ArrayObjects::_construct()是一个内置的 PHP 函数，用于构造一个新的数组对象。

**语法:**

```
public ArrayObject::__construct ($input = array(), int $flags = 0, 
string $iterator_class = "ArrayIterator")

```

**参数:**该函数接受三个参数，如上面的语法所示，描述如下:

1.  **$input:** 该参数用于接受输入为**数组**或**对象**。
2.  **$flags:** Flags 用于控制**数组对象的行为。**
3.  **$iterator_class:** 用于指定将用于**数组对象**对象迭代的类。

**返回值:**该函数在编译成功时返回一个**数组对象**。

**错误和异常:**

1.  如果$input 不是数组或对象，编译器将显示错误。
2.  如果$flags 集没有整数值，那么编译器将显示一条错误消息。

下面的程序说明了 ArrayObjects::_construct()函数:

**程序 1:**

```
<?php
$array = array('1' => 'one',
               '2' => 'two',
               '3' => 'three');

$arrayobject = new ArrayObject($array);

var_dump($arrayobject);
?>
```

**输出:**

```
object(ArrayObject)#1 (1) {
  ["storage":"ArrayObject":private]=>
  array(3) {
    [1]=>
    string(3) "one"
    [2]=>
    string(3) "two"
    [3]=>
    string(5) "three"
  }
}

```

**程序 2:**

```
<?php
$array = array('1' => 'Geeks',
               '2' => 'for',
               '3' => 'Geeks');

$arrayobject = new ArrayObject($array);

var_dump($arrayobject);
?>
```

**输出:**

```
object(ArrayObject)#1 (1) {
  ["storage":"ArrayObject":private]=>
  array(3) {
    [1]=>
    string(5) "Geeks"
    [2]=>
    string(3) "for"
    [3]=>
    string(5) "Geeks"
  }
}

```

**参考:**T2[http://php.net/manual/en/arrayobject.construct.php](http://php.net/manual/en/arrayobject.construct.php)