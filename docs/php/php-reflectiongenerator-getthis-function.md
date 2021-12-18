# PHP|ReflectionGenerator getThis()函数

> Original: [https://www.geeksforgeeks.org/php-reflectiongenerator-getthis-function/](https://www.geeksforgeeks.org/php-reflectiongenerator-getthis-function/)

**ReflectionGenerator：：getThis()函数**是 PHP 中的一个内置函数，用于返回指定生成器的**$this**值。

**语法：**

```php
*object* ReflectionGenerator::getThis ( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定生成器的**$this**值。

以下程序说明 PHP：
**Program_1：**中的 ReflectionGenerator：：getThis()函数

```php
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

// Calling the getThis() function
$C = $B->getThis();

// Getting the $this value of the
// specified generator 'A'
var_dump($C);
?>
```

发帖主题：Re：Колибри0.7.0

```php
object(Company)#1 (0) {
}

```

**程序 _2：**

```php
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

// Calling the getThis() function
// and getting the $this value of the
// specified generators
var_dump($D->getThis());
echo "\n";
var_dump($E->getThis());
echo "\n";
var_dump($F->getThis());
?>
```

发帖主题：Re：Колибри0.7.0

```php
object(Departments)#1 (0) {
}

object(Departments)#3 (0) {
}

object(Departments)#5 (0) {
}

```

**引用：**[https://www.php.net/manual/en/reflectiongenerator.getthis.php](https://www.php.net/manual/en/reflectiongenerator.getthis.php)