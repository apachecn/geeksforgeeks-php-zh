# PHP|对象到其他类的对象的类型转换和转换

> Original: [https://www.geeksforgeeks.org/php-type-casting-and-conversion-of-an-object-to-an-object-of-other-class/](https://www.geeksforgeeks.org/php-type-casting-and-conversion-of-an-object-to-an-object-of-other-class/)

给定一个 PHP 类对象，任务是将该对象转换或强制转换为另一个类的对象。

**方法 1：**作为标准预定义类实例的对象可以转换为另一个标准类的对象。

**示例：**

```php
<?php
// PHP program to show 
// standard type casting

$a = 1;
var_dump($a);

// int to float
$a = (float) $a;
var_dump($a);

// float to double
$a = (double) $a;
var_dump($a);

// double to real
$a = (real) $a;
var_dump($a);

// real to int
$a = (int) $a;
var_dump($a);

// int to integer
$a = (integer) $a;
var_dump($a);

// integer to bool
$a = (bool) $a;
var_dump($a);

// bool to boolean
$a = (boolean) $a;
var_dump($a);

// boolean to string
$a = (string) $a;
var_dump($a);

// string to array
$a = (array) $a;
var_dump($a);

// array to object
$a = (object) $a;
var_dump($a);

// object to unset/NULL
$a = (unset) $a;
var_dump($a);

?>
```

**Output:**

```php
int(1)
float(1)
float(1)
float(1)
int(1)
int(1)
bool(true)
bool(true)
string(1) "1"
array(1) {
  [0]=>
  string(1) "1"
}
object(stdClass)#1 (1) {
  [0]=>
  string(1) "1"
}
NULL

```

**方法 2：**为最终类创建一个构造函数，并添加一个 foreach 循环，用于将初始类的所有属性赋给最终类的实例。

**示例：**

```php
<?php
// PHP program to convert an class object
// to object of another class

// Original class
class Geeks1 {

    var $a = 'geeksforgeeks';

    function print_geeksforgeeks() {
        print('geeksforgeeks');
    }
}

// Final class
class Geeks2 {

    // Constructor function of class Geeks2
    public function __construct($object) {

        // Initializing class properties
        foreach($object as $property => $value) {
            $this->$property = $value;
        }
    }
}

// Initializing an object of class Geeks1
$object1 = new Geeks1();

// Printing original object of class Geeks1
print_r($object1);

// Initializing an object of class Geeks2
// using an object of class Geeks1
$object1 = new Geeks2($object1);

// Printing object of class Geeks2
print_r($object1);

?>
```

**Output:**

```php
Geeks1 Object
(
    [a] => geeksforgeeks
)
Geeks2 Object
(
    [a] => geeksforgeeks
)

```

**方法 3：**编写一个函数，使用 Serialize()方法将初始类的对象转换为序列化数据。 使用 unSerialize()方法将此序列化数据反序列化为最终类的实例。
**注意：不能使用此方法调用**成员函数。 只有在初始类仅包含变量作为成员时，才能使用此方法。

**示例：**

```php
<?php
// PHP program to convert an class object 
// to object of another class

// Original class
class Geeks1 {

    var $a = 'geeksforgeeks';

    function print_geeksforgeeks() {
        print('geeksforgeeks');
    }
}

// Final class
class Geeks2 {

    /* Empty abstract class */
}

// Function to convert class of given object
function convertObjectClass($object, $final_class) {
    return unserialize(sprintf(
        'O:%d:"%s"%s',
        strlen($final_class),
        $final_class,
        strstr(strstr(serialize($object), '"'), ':')
    ));
}

// Initializing an object of class Geeks2
$object1 = new Geeks1();

// Printing original object of class Geeks1
print_r($object1);

// Converting an object of class Geeks1
// into an object of class Geeks2
$object1 = convertObjectClass($object1, 'Geeks2');

// Printing object of class Geeks2
print_r($object1);

?>
```

**Output:**

```php
Geeks1 Object
(
    [a] => geeksforgeeks
)
Geeks2 Object
(
    [a] => geeksforgeeks
)

```

**注意：**一般来说，PHP 不允许对用户定义的类进行类型转换，而转换/转换可以通过上面介绍的方法间接实现。