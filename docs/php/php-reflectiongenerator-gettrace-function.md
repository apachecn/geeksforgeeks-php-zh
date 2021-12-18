# PHP|ReflectionGenerator getTrace()函数

> Original: [https://www.geeksforgeeks.org/php-reflectiongenerator-gettrace-function/](https://www.geeksforgeeks.org/php-reflectiongenerator-gettrace-function/)

**ReflectionGenerator：：getTrace()函数**是 PHP 中的内置函数，用于返回指定的当前正在执行的生成器的跟踪。

**语法：**

```
*array* ReflectionGenerator::getTrace ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定的当前正在执行的生成器的跟踪。

以下程序说明 PHP：
**Program_1：**中的**ReflectionGenerator：：getTrace()**函数

```
<?php

// Initializing a user-defined class Company
class Company
{
    public function GFG()
    {
        yield 0;
    }
}

// Creating a generator 'A' on the above
// class Company
$A = (new Company)->GFG();

// Using ReflectionGenerator over the 
// above generator 'A'
$B = new ReflectionGenerator($A);

// Calling the getTrace() function
$C = $B->getTrace();

// Getting the trace of the specified 
// executing generator 'A'
var_dump($C);
?>
```

发帖主题：Re：Колибри0.7.0

```
array(0) {
}

```

**程序 _2：**

```
<?php

// Initializing a user-defined function
function Department1() {
    yield 1;
}

function Department2()
{
    yield from Department1();
}

function Department3()
{
    yield from Department2();
}

// Creating a generator
$A = Department3();

// Starting the generator
$A->valid();

// Using ReflectionGenerator() over the 
// above generator 'A'
$A = new ReflectionGenerator($A);

// Calling the getTrace() function
$B = $A->getTrace();

// Getting the the trace of the 
// executing generator 'A'
var_dump($B);
?>
```

发帖主题：Re：Колибри0.7.0

```
array(2) {
  [0]=>
  array(4) {
    ["file"]=>
    string(42) "/home/5ae62f6794b195f5dfeff893639bead9.php"
    ["line"]=>
    int(10)
    ["function"]=>
    string(11) "Department1"
    ["args"]=>
    array(0) {
    }
  }
  [1]=>
  array(4) {
    ["file"]=>
    string(42) "/home/5ae62f6794b195f5dfeff893639bead9.php"
    ["line"]=>
    int(15)
    ["function"]=>
    string(11) "Department2"
    ["args"]=>
    array(0) {
    }
  }
}

```

**引用：**[https://www.php.net/manual/en/reflectiongenerator.gettrace.php](https://www.php.net/manual/en/reflectiongenerator.gettrace.php)