# PHP|ReflectionGenerator getExecutingLine()函数

> Original: [https://www.geeksforgeeks.org/php-reflectiongenerator-getexecutingline-function/](https://www.geeksforgeeks.org/php-reflectiongenerator-getexecutingline-function/)

**ReflectionGenerator：：getExecutingLine()函数**是 PHP 中的内置函数，用于返回生成器中指定的当前正在执行的语句的行号。

**语法：**

```
*int* ReflectionGenerator::getExecutingLine( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回生成器中指定的当前正在执行的语句的行号。

下面的程序演示了 PHP 中的 ReflectionGenerator：：getExecutingLine()函数：

**程序 1：**

```
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

// Calling the getExecutingLine() function
$C = $B->getExecutingLine();

// Getting the line number of the specified
// currently executing statement in 
// the generator 'A'
echo $C;
?>
```

**输出：**

```
8

```

**程序 2：**

```
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

// Calling the getExecutingLine() function
// and getting the line number of the specified
// currently executing statement in 
// the generators
echo $D->getExecutingLine();
echo "\n";
echo $E->getExecutingLine();
echo "\n";
echo $F->getExecutingLine();
?>
```

**输出：**

```
8
12
16

```

**引用：**[https://www.php.net/manual/en/reflectiongenerator.getexecutingline.php](https://www.php.net/manual/en/reflectiongenerator.getexecutingline.php)