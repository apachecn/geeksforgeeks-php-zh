# PHP|ReflectionGenerator getFunction()函数

> Original: [https://www.geeksforgeeks.org/php-reflectiongenerator-getfunction-function/](https://www.geeksforgeeks.org/php-reflectiongenerator-getfunction-function/)

**ReflectionGenerator：：getFunction()函数**是 PHP 中的内置函数，用于返回指定生成器的函数名。

**语法：**

```
*ReflectionFunctionAbstract* ReflectionGenerator::getFunction ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定生成器的函数名。

以下程序说明 PHP：
**Program_1：**中的**ReflectionGenerator：：getFunction()函数**

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

// Calling the getFunction() function
$C = $B->getFunction();

// Getting the function name of the
// specified generator 'A'
var_dump($C);
?>
```

发帖主题：Re：Колибри0.7.0

```
object(ReflectionMethod)#4 (2) {
  ["name"]=>
  string(3) "GFG"
  ["class"]=>
  string(7) "Company"
}

```

**程序 _2：**

```
<?php

// Initializing a user-defined class Departments
class Departments
{
    public function Coding_Department()
    {
        yield 0;
    }
    public function HR_Department()
    {
        yield 1;
    }
    public function Marketing_Department()
    {
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

// Calling the getFunction() function
// and getting the function name of the
// specified generators
var_dump($D->getFunction());
echo "\n";
var_dump($E->getFunction());
echo "\n";
var_dump($F->getFunction());
?>
```

发帖主题：Re：Колибри0.7.0

```
object(ReflectionMethod)#10 (2) {
  ["name"]=>
  string(17) "Coding_Department"
  ["class"]=>
  string(11) "Departments"
}

object(ReflectionMethod)#10 (2) {
  ["name"]=>
  string(13) "HR_Department"
  ["class"]=>
  string(11) "Departments"
}

object(ReflectionMethod)#10 (2) {
  ["name"]=>
  string(20) "Marketing_Department"
  ["class"]=>
  string(11) "Departments"
}

```

**引用：**[https://www.php.net/manual/en/reflectiongenerator.getfunction.php](https://www.php.net/manual/en/reflectiongenerator.getfunction.php)