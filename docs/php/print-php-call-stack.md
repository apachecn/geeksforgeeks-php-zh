# 打印 PHP 调用堆栈

> Original: [https://www.geeksforgeeks.org/print-php-call-stack/](https://www.geeksforgeeks.org/print-php-call-stack/)

给定一个 PHP 代码，任务是打印此 PHP 代码的调用堆栈。 在给定的 PHP 代码中，Child_func()函数调用 parent_func()函数，后者进一步调用导致调用堆栈的 GRAGPARENT_FUNC()函数。

**方法 1：**使用[debug_print_backtrace()](http://php.net/manual/en/function.debug-print-backtrace.php)函数打印调用堆栈。

**示例：**

```php
<?php
// PHP program to print PHP call stack

// Function to call parent_func 
function child_func() {
    parent_func();
}

// Function to call grandparent_func
function parent_func() {
    grandparent_func();
}

// Function to print call stack
function grandparent_func() {
    debug_print_backtrace();
}

// Main function call
child_func();

?>
```

**Output:**

```php
#0  grandparent_func() called at [/home/905a3b4d90f10b30521fedcb56c99fba.php:12]
#1  parent_func() called at [/home/905a3b4d90f10b30521fedcb56c99fba.php:7]
#2  child_func() called at [/home/905a3b4d90f10b30521fedcb56c99fba.php:21]

```

**方法 2：**使用[debug_backtrace()](http://php.net/manual/en/function.debug-backtrace.php)函数打印调用堆栈。
**示例：**

```php
<?php
// PHP program to print PHP call stack

// Function to call parent_func 
function child_func() {
    parent_func();
}

// Function to call grandparent_func
function parent_func() {
    grandparent_func();
}

// Function to print call stack
function grandparent_func() {
    var_dump(debug_backtrace());
}

// Main function call
child_func();

?>
```

**Output:**

```php
array(3) {
  [0]=>
  array(4) {
    ["file"]=>
    string(42) "/home/2b81f040639170c49a6a58adb23d5154.php"
    ["line"]=>
    int(12)
    ["function"]=>
    string(16) "grandparent_func"
    ["args"]=>
    array(0) {
    }
  }
  [1]=>
  array(4) {
    ["file"]=>
    string(42) "/home/2b81f040639170c49a6a58adb23d5154.php"
    ["line"]=>
    int(7)
    ["function"]=>
    string(11) "parent_func"
    ["args"]=>
    array(0) {
    }
  }
  [2]=>
  array(4) {
    ["file"]=>
    string(42) "/home/2b81f040639170c49a6a58adb23d5154.php"
    ["line"]=>
    int(21)
    ["function"]=>
    string(10) "child_func"
    ["args"]=>
    array(0) {
    }
  }
}

```

**方法 3：**异常类的[getTraceAsString()](http://php.net/manual/en/exception.gettraceasstring.php)成员函数返回调用堆栈。

**示例：**

```php
<?php
// PHP program to print PHP call stack

// Function to call parent_func 
function child_func() {
    parent_func();
}

// Function to call grandparent_func
function parent_func() {
    grandparent_func();
}

// Function to print call stack
function grandparent_func() {
    $e = new Exception;
    var_dump($e->getTraceAsString());
}

// Main function call
child_func();

?>
```

**Output:**

```php
string(207) "#0 /home/8d8303d43667a4915d43dab7d63de26d.php(12): grandparent_func()
#1 /home/8d8303d43667a4915d43dab7d63de26d.php(7): parent_func()
#2 /home/8d8303d43667a4915d43dab7d63de26d.php(22): child_func()
#3 {main}"

```