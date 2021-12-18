# PHP 中静态和实例方法的比较

> 原文:[https://www . geesforgeks . org/PHP 中静态方法和实例方法的比较/](https://www.geeksforgeeks.org/comparison-between-static-and-instance-method-in-php/)

<center>**Static methods**</center>

The static method in PHP is same as other OOP languages. Static method should be used only when particular data remains constant for the whole class. As an example, consider that some programmer is making the data of a college and in that every object needs getCollegeName function that returns the same college name for all objects as name of college then this function should be made static. Basically static methods are used when to access that method without the object of that class. Static method are used when there is a chance to use method without help of class objects.

**示例:**

```php
<?php

// PHP code for static method 
class College
{
    // Static function
    static function getCollegeName()
    {
            return "MNNIT Allahabad";
    }
}

// Calling function without its object
echo (College::getCollegeName());
?>
```

**Output:**

```php
MNNIT Allahabad

```

<center>**Instance Methods**</center>

Instance method is used when there is no chance to call the method without existing of object. For example consider a College class in which getPersonName() method which returns the name of person. This method should exist only when there is a particular type of person object.

**示例:**

```php
<?php
// Program for instance methods

class College
{
    // This data can not be accessed
    // from outside of the class
    private $name;

    // This function sets the name
    function setName($name) {
        $this -> name = $name;
    }

    // This function return name
    function getName() {
        return $this -> name;
    }
}

// Creating an object of type College
$obj = new College;

// Setting name
$obj -> setName("Geeks");

// Getting name
echo ($obj -> getName());
?>
```

**Output:**

```php
Geeks

```

**实例和静态方法的比较:**

*   静态方法可以在没有对象的情况下调用，而实例方法不能在没有对象的情况下调用。
*   实例方法的执行时间比静态方法快，但是在 PHP 5.3 版中有一个错误，它说静态方法更快，因为它们引入了后期绑定。

**示例:**

```php
<?php

// Program to compare execution time 
// of static and instance methods
set_time_limit(0);

// Checking php version
echo 'Current PHP version: ' . phpversion();

// Creating class for static
Class St {

    public static $count = 0;

    // function that will print nothing
    public static function getResult()
    {
        self::$count = self::$count + 1;
    }
}

// For calculating time
$time_start_static = microtime(true);

// This loop will run 100000 times
for($i = 0; $i < 100000; $i++) {
    St::getResult();
}

// Execution time for static method ends here
$time_end_static = microtime(true);

// Execution time is end -start time
$time_static = $time_end_static - $time_start_static;

// Printing the result
echo "\nTotal execution time is for static method is: '$time_static'";

// Demo class for instance method
class Ins {
    private $count = 0;

    // Function that will not print anything
    public function getResult() {
        $this -> count = $this -> count + 2;
    }
}

// Creating an instance object
$ob = new Ins;

// Starting time is insitialize
$time_start_instance = microtime(true);

// For time loop is run
for($i = 0; $i < 100000; $i++)
{
    $ob -> getResult();
}

// Execution end for instance method
$time_end_instance = microtime(true);

// Total time is end-start time
$time_instance = $time_end_instance - $time_start_instance;

// Result is printed
echo "\nTotal execution time for instance method is: '$time_instance'";
?>
```

**Output:**

```php
Current PHP version: 7.0.32-0ubuntu0.16.04.1
Total execution time is for static method is: '0.0056149959564209'
Total execution time for instance method is: '0.004885196685791'

```