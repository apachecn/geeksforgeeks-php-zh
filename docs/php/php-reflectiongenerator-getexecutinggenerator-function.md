# PHP|ReflectionGenerator getExecutingGenerator()函数

> Original: [https://www.geeksforgeeks.org/php-reflectiongenerator-getexecutinggenerator-function/](https://www.geeksforgeeks.org/php-reflectiongenerator-getexecutinggenerator-function/)

**ReflectionGenerator：：getExecutingGenerator()函数**是 PHP 中的内置函数，用于返回当前正在执行的 Generator 对象。

**语法：**

```php
*Generator* ReflectionGenerator::getExecutingGenerator( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回当前正在执行的 Generator 对象。

下面的程序演示了 PHP 中的 ReflectionGenerator：：getExecutingGenerator()函数：

**程序 1：**

```php
<?php

// Initializing a user-defined class Company
class Company {
    public function GFG() {
        yield 0;
    }
}

// Creating a generator 'A' on the above
// class Company
$A = (new Company)->GFG();

// Using ReflectionGenerator over the 
// above generator 'A'
$B = new ReflectionGenerator($A);

// Calling the getExecutingGenerator() function
$C = $B->getExecutingGenerator();

// Getting the currently executing
// Generator object
var_dump($C->current());
?>
```

**输出：**

```php
int(0)

```

**程序 2：**

```php
<?php

// Initializing a user-defined class Departments
class Departments {
    public function Coding_Department() {
        yield 0;
    }
    public function HR_Department() {
        yield 1;
    }
    public function Marketing_Department() {
        yield 2;
    }
}

// Creating some generators on the above
// class Departments
$A = (new Departments)->Coding_Department();
$B = (new Departments)->HR_Department();
$C = (new Departments)->Marketing_Department();

// Using ReflectionGenerator over the 
// above generators
$D = new ReflectionGenerator($A);
$E = new ReflectionGenerator($B);
$F = new ReflectionGenerator($C);

// Calling the getExecutingGenerator() function
// and getting the currently executing
// Generator object
var_dump($D->getExecutingGenerator()->current());
var_dump($E->getExecutingGenerator()->current());
var_dump($F->getExecutingGenerator()->current());
?>
```

**输出：**

```php
int(0)
int(1)
int(2)

```

**引用：**[https://www.php.net/manual/en/reflectiongenerator.getexecutinggenerator.php](https://www.php.net/manual/en/reflectiongenerator.getexecutinggenerator.php)