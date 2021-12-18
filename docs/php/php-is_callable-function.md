# PHP|is_callable()函数

> Original: [https://www.geeksforgeeks.org/php-is_callable-function/](https://www.geeksforgeeks.org/php-is_callable-function/)

Is_callable()函数是 PHP 中的一个内置函数，用于验证变量的内容是否可以作为函数调用。 它可以检查简单变量是否包含有效函数的名称，或者数组是否包含正确编码的对象和函数名称。

**语法：**

```php
bool is_callable ( $variable_name, $syntax_only, $callable_name )
```

**参数：**is_callable()函数接受上述语法中所示的三个参数，如下所述。 这取决于用户使用多少个参数一、二或三。

*   **$VARIABLE_NAME：**存储在字符串变量$VARIABLE_NAME 中的函数的名称，或对象和对象内的方法的名称。
*   **$SYNTAX_ONLY：**如果设置为 TRUE，则该函数仅验证名称可能是函数或方法。 它将拒绝不是字符串的简单变量，或者拒绝没有有效结构用作回调的数组。 有效的条目应该只有 2 个条目，第一个条目是对象或字符串，第二个条目是字符串。
*   **$CALLABLE_NAME：**接收可调用名称。 此选项仅对类实现。

**返回值：**此函数返回布尔类型值。 如果$VARIABLE_NAME 可调用，则返回 TRUE，否则返回 FALSE。

下面的程序说明 PHP 中的 is_callable()函数：
**程序 1：**简单变量包含一个函数

```php
<?php
// To check a variable if it can be called
// as a function.

// Declare the function
function Function_xyz() 
{
}

$variable_name = "Function_xyz";
var_dump(is_callable($variable_name, false, $callable_name));
echo $callable_name, "\n";

// using only-one parameter
var_dump(is_callable($variable_name));
?>
```

**Output:**

```php
bool(true)
Function_xyz
bool(true)

```

**程序 2：**数组包含一个方法

```php
<?php
// To check a variable if it can be called
// as a function.

// Define class
class ClassA {
   // Define method
  function Method_xyz() 
  {
  }

}

// Object instance
$obj = new ClassA();

$variable_name = array($obj, 'Method_xyz');

var_dump(is_callable($variable_name, true, $callable_name));  
echo $callable_name, "\n";  
?>
```

**Output:**

```php
bool(true)
ClassA::Method_xyz

```

**引用：**[http://php.net/manual/en/function.is-callable.php](http://php.net/manual/en/function.is-callable.php)