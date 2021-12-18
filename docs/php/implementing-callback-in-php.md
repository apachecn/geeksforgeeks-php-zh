# 在 PHP 中实现回调

> 原文:[https://www.geeksforgeeks.org/implementing-callback-in-php/](https://www.geeksforgeeks.org/implementing-callback-in-php/)

在 PHP 中，回调是类型为[可调用](https://www.geeksforgeeks.org/php-is_callable-function/)的函数对象/引用。回调/可调用变量可以充当函数、对象方法和静态类方法。实现回调有多种方法。其中一些将在下面讨论:

**标准回调:**在 PHP 中，可以使用 [call_user_func()](https://www.geeksforgeeks.org/php-call_user_func-function/) 函数调用函数，其中参数是要调用的函数的字符串名称。

**示例:**

```
<?php

// PHP program to illustrate working
// of a standard callback

// Function to print a string
function someFunction() {
    echo "Geeksforgeeks \n";
}

// Standard callback
call_user_func('someFunction');
?>
```

**Output:**

```
Geeksforgeeks

```

**静态类方法回调:**静态类方法可以通过使用 [call_user_func()](https://www.geeksforgeeks.org/php-call_user_func-function/) 来调用，这里的参数是一个数组，包含类的字符串名称及其内部要调用的方法。

**示例:**

```
<?php

// PHP program to illustrate working
// of a Static class method callback

// Sample class
class GFG {

    // Function used to print a string
    static function someFunction() {
        echo "Parent Geeksforgeeks \n";
    }
}

class Article extends GFG {

    // Function to print a string
    static function someFunction() {
        echo "Geeksforgeeks Article \n";
    }   
}

// Static class method callback
call_user_func(array('Article', 'someFunction'));

call_user_func('Article::someFunction');

// Relative Static class method callback
call_user_func(array('Article', 'parent::someFunction'));
?>
```

**Output:**

```
Geeksforgeeks Article
Geeksforgeeks Article
Parent Geeksforgeeks

```

**对象方法回调:**可以使用 [call_user_func()](https://www.geeksforgeeks.org/php-call_user_func-function/) 调用对象方法，其中参数是包含对象变量和要调用的方法的字符串名称的数组。如果可以使用 __invoke()函数定义调用对象方法，也可以调用它们。在这种情况下， [call_user_func](https://www.geeksforgeeks.org/php-call_user_func-function/) ()函数的参数就是对象变量本身。

**示例:**

```
<?php

// PHP program to illustrate working
// of a object method callback

// Sample class
class GFG {

    // Function to print a string
    static function someFunction() {
        echo "Geeksforgeeks \n";
    }

    // Function used to print a string
    public function __invoke() {
        echo "invoke Geeksforgeeks \n";
    }
}

// Class object
$obj = new GFG();

// Object method call
call_user_func(array($obj, 'someFunction'));

// Callable __invoke method object 
call_user_func($obj);

?> 
```

**Output:**

```
Geeksforgeeks
invoke Geeksforgeeks

```

**闭包回调:**闭包函数可以通过进行标准调用或使用 [array_map()](https://www.geeksforgeeks.org/php-array_map-function/) 函数将闭包函数映射到给定闭包函数的有效参数数组来调用，其中参数是闭包函数及其有效参数数组。

**示例:**

```
<?php

// PHP program to illustrate working
// of a closure callback

// Closure to print a string
$print_function = function($string) {
    echo $string."\n";
};

// Array of strings
$string_array = array("Geeksforgeeks", "GFG", "Article");

// Callable closure
array_map($print_function, $string_array);

?>
```

**Output:**

```
Geeksforgeeks
GFG
Article

```