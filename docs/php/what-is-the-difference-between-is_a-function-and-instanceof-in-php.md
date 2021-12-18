# PHP 中 is_a()函数和 instanceof 有什么区别？

> 原文:[https://www . geesforgeks . org/is-a-function-instance of-in-PHP/](https://www.geeksforgeeks.org/what-is-the-difference-between-is_a-function-and-instanceof-in-php/)的区别是什么

<center>**[is_a() Function](https://www.geeksforgeeks.org/php-is_a-function/)**</center>

The is_a() is a built-in function in PHP which is used to check whether a given object is of a given class or not. It also checks if the given class is one of the parents of the given object or not.

**语法:**

```php
bool is_a( $object, $class_name, $allow_string )
```

**参数:**该功能接受三个参数，如上所述，描述如下:

*   **对象:**此参数用于容纳被测对象。
*   **类名:**此参数用于保存类名。
*   **allow_string:** 如果该参数设置为 False，则不允许字符串类名作为对象。

**返回值:**如果对象属于这个类或者这个类是它的父类，这个函数返回真，否则它将返回假值。

下面的程序说明 is_a()函数:

```php
<?php 
// PHP program to illustrate the  
// is_a() function 

// sample class 
class GeeksforGeeks { 
    var $store = 'Hello geeks!'; 
} 

// create a new object 
$geek = new GeeksforGeeks(); 

// checks if $geek is an object 
// of class GeeksforGeeks 
if (is_a($geek, 'GeeksforGeeks')) { 
    echo "Yes"; 
} 

?>
```

**Output:**

```php
Yes

```

<center>**instanceof operator**</center>

The instanceof operator is used in PHP to find out if an object is an instantiated instance of a class.

**语法:**

```php
$a instanceof MyClass
```

**操作数:**该运算符包含两个操作数，如下所示:

*   **$a:** 这个用作宾语。
*   **MyClass:** 是类名。

**返回值:**如果对象属于这个类或者这个类是它的父类，它将返回真，否则它将返回假。

下面的程序说明了 PHP 中的 instanceof 运算符:

```php
<?php
// PHP program to illustrate instanceof
// operator

// sample class 
class GeeksforGeeks { 
    var $store = 'Hello geeks!'; 
} 

// create a new object 
$geek = new GeeksforGeeks(); 

// Checks if $geek is an object of 
// class GeeksforGeeks 
if ($geek instanceof GeeksforGeeks) {
    echo "Yes";
}

?>
```

**Output:**

```php
Yes

```

**is _ a()函数和 instanceof 运算符的区别:**

*   is_a()是一个函数，而 instanceof 是一个语言构造。is_a()函数将明显慢一些，因为它有执行函数调用的所有开销。
*   如果函数中的回调(如 array_map) instanceof 不是函数，它是一个语言构造，因此不能用作回调。另一方面回调可以用在 is_a()函数中。
*   instanceof 使用的直接类名比 is_a()函数短。
    **例:**

    ```php
    // Short syntax (comparatively)
    $a instanceof MyClass

    is_a( $a, MyClass::class )

    ```

*   The is_a() being a function takes an object as parameter one, and a string as parameter two, whereas **instanceof** takes an object as parameter one, and can take a class name, object instance, or class identifier (class name written without quotes) as parameter two.

    **is _ a()示例:**

    ```php
    // Only way to call it
    is_a( $object, $string );

    ```

    **实例示例:**

    ```php
    // Object instance      
    $object instanceof $otherObject; 

    // String class name
    $object instanceof $string;

    // Identifier for the class
    $object instanceof ClassName;    

    ```