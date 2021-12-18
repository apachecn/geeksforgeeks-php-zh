# PHP | ArrayObject setIteratorClass()函数

> 原文:[https://www . geesforgeks . org/PHP-arrayobject-setiteratorclass-function/](https://www.geeksforgeeks.org/php-arrayobject-setiteratorclass-function/)

**ArrayObject::SetIteratorClass()函数**是 PHP 中的一个内置函数，用于设置 Arrayobject 的迭代器类名。

**语法:**

```php
*void* ArrayObject::setIteratorClass( *string* $iterator_class )
```

**参数:**这个函数接受单个参数 **$iterator_class** ，它保存数组迭代器的类名。当它在这个对象上迭代时使用。

**返回值:**该函数不返回值。

下面的程序说明了 PHP 中的 ArrayObject::setIteratorClass()函数:

**程序 1:**

```php
<?php 
// PHP program to illustrate the 
// ArrayObject::setIteratorClass() function 

// Custom ArrayIterator (inherits from ArrayIterator)
class iteratorClass extends ArrayIterator {

}

// Create array object 
$arrayObjectElement = new ArrayObject(
    array('Geeks', 'for', 'Geeks')
); 

// Use ArrayObject::setIteratorClass() function
// to set the iterator classname for the ArrayObject
$arrayObjectElement->setIteratorClass('iteratorClass');

print_r($arrayObjectElement->getIterator());

?>
```

**输出:**

```php
iteratorClass Object
(
    [storage:ArrayIterator:private] => ArrayObject Object
        (
            [storage:ArrayObject:private] => Array
                (
                    [0] => Geeks
                    [1] => for
                    [2] => Geeks
                )

        )

)

```

**程序二:**

```php
<?php 
// PHP program to illustrate the 
// ArrayObject::setIteratorClass() function 

// Custom ArrayIterator (inherits from ArrayIterator)
class iteratorClass extends ArrayIterator {

}

// Declare an associative array
$arr = array(
    "a" => "Welcome",
    "b" => "to", 
    "d" => "GeeksforGeeks"
); 

// Create array object 
$arrayObjectElement = new ArrayObject($arr); 

// Use ArrayObject::setIteratorClass() function
// to set the iterator classname for the ArrayObject
$arrayObjectElement->setIteratorClass('iteratorClass');

print_r($arrayObjectElement->getIterator());

?>
```

**输出:**

```php
iteratorClass Object
(
    [storage:ArrayIterator:private] => ArrayObject Object
        (
            [storage:ArrayObject:private] => Array
                (
                    [a] => Welcome
                    [b] => to
                    [d] => GeeksforGeeks
                )

        )

)

```

**参考:**[https://www . PHP . net/manual/en/arrayobject . setiteratorclass . PHP](https://www.php.net/manual/en/arrayobject.setiteratorclass.php)