# 如何合并两个 PHP 对象？

> 原文:[https://www.geeksforgeeks.org/how-to-merge-two-php-objects/](https://www.geeksforgeeks.org/how-to-merge-two-php-objects/)

给定两个相同类的对象，任务是将这两个对象合并成一个对象。
**方法 1:** 将对象转换为数据数组，并使用 [array_merge()](https://www.geeksforgeeks.org/php-merging-two-arrays-using-array_merge/) 函数将其合并，并将此合并数组转换回类 *stdClass* 的对象。
**注意:**使用 array_merge()合并对象时，argument1 中数组的元素会被 argument2 中数组的元素覆盖。如果 argument2 中的数组具有空值，这可能会使最终对象中的结果元素无效。
**注意:**使用这种方法不会复制功能。只有当类只包含变量时，才使用这种方法。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to merge two objects

class Geeks {
    // Empty class
}

$objectA = new Geeks();
$objectA->a = 1;
$objectA->b = 2;
$objectA->d = 3;

$objectB = new Geeks();
$objectB->d = 4;
$objectB->e = 5;
$objectB->f = 6;

$obj_merged = (object) array_merge(
        (array) $objectA, (array) $objectB);

print_r($obj_merged);

?>
```

**Output:** 

```
stdClass Object
(
    [a] => 1
    [b] => 2
    [d] => 4
    [e] => 5
    [f] => 6
)
```

**方法 2:** 使用 array_merge()方法合并对象，并使用 convertObjectClass 函数将此合并的数组转换为对象。此函数用于使用 [serialize()](https://www.geeksforgeeks.org/php-serializing-data/) 方法将初始类的对象转换为序列化数据。使用 [unserialize()](https://www.geeksforgeeks.org/php-serializing-data/) 方法将序列化数据非序列化为最终类的实例。使用这种方法获得用户定义类*极客*的对象，而不是标准类*标准类*。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to merge two objects

class Geeks {
    // Empty class
}

$objectA = new Geeks();
$objectA->a = 1;
$objectA->b = 2;
$objectA->d = 3;

$objectB = new Geeks();
$objectB->d = 4;
$objectB->e = 5;
$objectB->f = 6;

// Function to convert class of given object
function convertObjectClass($array, $final_class) {
    return unserialize(sprintf(
        'O:%d:"%s"%s',
        strlen($final_class),
        $final_class,
        strstr(serialize($array), ':')
    ));
}

$obj_merged = convertObjectClass(array_merge(
        (array) $objectA, (array) $objectB), 'Geeks');

print_r($obj_merged);

?>
```

**Output:** 

```
Geeks Object
(
    [a] => 1
    [b] => 2
    [d] => 4
    [e] => 5
    [f] => 6
)
```

**方法 3:** 创建一个原始类的新对象，并使用 foreach 循环将两个对象的所有属性分配给这个新对象。这是一种简单明了的合并两个对象的方法。
**例:**

## 服务器端编程语言（Professional Hypertext Preprocessor 的缩写）

```
<?php
// PHP program to merge two objects

class Geeks {
    // Empty class
}

$objectA = new Geeks();
$objectA->a = 1;
$objectA->b = 2;
$objectA->d = 3;

$objectB = new Geeks();
$objectB->e = 4;
$objectB->f = 5;
$objectB->g = 6;

// Function to convert class of given object
function convertObjectClass($objectA,
                $objectB, $final_class) {

    $new_object = new $final_class();

    // Initializing class properties
    foreach($objectA as $property => $value) {
        $new_object->$property = $value;
    }

    foreach($objectB as $property => $value) {
        $new_object->$property = $value;
    }

    return $new_object;
}

$obj_merged = convertObjectClass($objectA,
                        $objectB, 'Geeks');

print_r($obj_merged);

?>
```

**Output:** 

```
Geeks Object
(
    [a] => 1
    [b] => 2
    [d] => 3
    [e] => 4
    [f] => 5
    [g] => 6
)
```