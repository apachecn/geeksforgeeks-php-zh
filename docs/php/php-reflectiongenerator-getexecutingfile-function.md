# PHP|ReflectionGenerator getExecutingFile()函数

> Original: [https://www.geeksforgeeks.org/php-reflectiongenerator-getexecutingfile-function/](https://www.geeksforgeeks.org/php-reflectiongenerator-getexecutingfile-function/)

**ReflectionGenerator：：getExecutingFile()函数**是 PHP 中的内置函数，用于返回指定的当前正在执行的生成器的完整路径和文件名。

**语法：**

```php
*string* ReflectionGenerator::getExecutingFile( *void* )
```

**参数：**此函数不接受任何参数。

**返回值：**此函数返回指定的当前正在执行的生成器的完整路径和文件名。

下面的程序演示了 PHP 中的 ReflectionGenerator：：getExecutingFile()函数：

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

// Calling the getExecutingFile() function
$C = $B->getExecutingFile();

// Getting the full path and file name
// of the currently
// executing generator 'A'
echo $C;
?>
```

**输出：**

```php
/home/3ce672c0079010c54e57cdedc34d0188.php

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

// Calling the getExecutingFile() function
// and getting the full path and file 
// name of the currently
// executing generators
echo "File: {$D->getExecutingFile()}";
echo "\n";
echo "File: {$E->getExecutingFile()}";
echo "\n";
echo "File: {$F->getExecutingFile()}";
?>
```

**输出：**

```php
File: /home/f12a7584188452b12381b38e3985f9d3.php
File: /home/f12a7584188452b12381b38e3985f9d3.php
File: /home/f12a7584188452b12381b38e3985f9d3.php

```

**引用：**[https://www.php.net/manual/en/reflectiongenerator.getexecutingfile.php](https://www.php.net/manual/en/reflectiongenerator.getexecutingfile.php)